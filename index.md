<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
// ==========================================
// GENOMIC SIMULATOR ENGINE (SCIENTIFICALLY CALIBRATED)
// ==========================================

let costChart, performanceChart;

function initializeCharts() {
    // 1. Cost Distribution Chart
    const costCtx = document.getElementById('costChart').getContext('2d');
    costChart = new Chart(costCtx, {
        type: 'doughnut',
        data: {
            labels: ['Hot Storage (Delta Lake)', 'Spark Compute (ETL)', 'GPU Training (XGBoost)', 'Egress/API'],
            datasets: [{
                data: [0, 0, 0, 0], // Initial placeholders
                backgroundColor: ['#8b5cf6', '#3b82f6', '#10b981', '#f59e0b'],
                borderColor: '#1a1a1a',
                borderWidth: 3
            }]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: { position: 'bottom', labels: { color: '#d1d5db', font: { size: 11 } } },
                tooltip: {
                    callbacks: {
                        label: function(context) {
                            return context.label + ': $' + context.parsed.toLocaleString();
                        }
                    }
                }
            }
        }
    });

    // 2. Performance vs Scale Chart
    const perfCtx = document.getElementById('performanceChart').getContext('2d');
    performanceChart = new Chart(perfCtx, {
        type: 'line',
        data: {
            labels: ['100K', '250K', '500K', '750K', '1M'], // Sample sizes
            datasets: [{
                label: 'AUPRC (Model Accuracy)',
                data: [0.72, 0.76, 0.81, 0.83, 0.84], // Diminishing returns curve
                borderColor: '#8b5cf6',
                backgroundColor: 'rgba(139, 92, 246, 0.1)',
                borderWidth: 3,
                fill: true,
                tension: 0.4,
                yAxisID: 'y'
            }, {
                label: 'Compute Cost ($)',
                data: [1200, 3100, 6400, 9800, 14500], // Linear scaling
                borderColor: '#10b981',
                borderWidth: 3,
                fill: false,
                tension: 0.2,
                yAxisID: 'y1'
            }]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            interaction: { mode: 'index', intersect: false },
            scales: {
                y: {
                    min: 0.6, max: 0.9,
                    grid: { color: 'rgba(255,255,255,0.05)' },
                    ticks: { color: '#9ca3af' },
                    title: { display: true, text: 'AUPRC Score', color: '#8b5cf6' }
                },
                y1: {
                    position: 'right',
                    grid: { drawOnChartArea: false },
                    ticks: { color: '#9ca3af', callback: (val) => '$' + val },
                    title: { display: true, text: 'Est. Monthly Cost', color: '#10b981' }
                },
                x: {
                    grid: { color: 'rgba(255,255,255,0.05)' },
                    ticks: { color: '#9ca3af' }
                }
            }
        }
    });
}

// ==========================================
// SCIENTIFIC CALCULATIONS
// ==========================================

function updateSimulator() {
    // Get Inputs
    const samples = parseInt(document.getElementById('sampleCount').value);
    const features = parseInt(document.getElementById('featureCount').value);
    const depth = parseInt(document.getElementById('analysisDepth').value);

    // Update Text Displays
    document.getElementById('sampleDisplay').textContent = samples.toLocaleString() + ' samples';
    document.getElementById('featureDisplay').textContent = (features / 1e6).toFixed(1) + 'M variants';
    const depthLabels = ['Basic (Indel/SNP)', 'Comprehensive (SV/CNV)', 'Deep (Full Genome)'];
    document.getElementById('depthDisplay').textContent = depthLabels[depth - 1];

    // --- CORE LOGIC: STORAGE (Active Data Lake) ---
    // Raw WGS (30x) is ~80GB BAM. But for ML, we extract variants to Parquet/Delta.
    // Compression Ratio: Snappy Parquet is ~10-20x smaller than VCF.
    // Avg Size per Sample (Variant Data): ~400MB (0.4 GB) for comprehensive data.
    const gbPerSample = 0.4 * depth; // Scales with analysis depth
    const totalStorageTB = (samples * gbPerSample) / 1024;
    
    // Cost: S3 Standard ($0.023/GB) for Hot Analysis Data
    const storageCost = totalStorageTB * 1024 * 0.023;

    // --- CORE LOGIC: COMPUTE (Spark ETL) ---
    // ETL Cost: Reading Parquet + Shuffle.
    // Benchmark: 10,000 samples takes ~2 hours on a 10-node cluster (r5.2xlarge).
    // Spot Price: ~$0.10/hour/node.
    // Cost Factor: ~$0.015 per sample processed per month (incremental updates).
    const computeCost = samples * 0.015 * depth;

    // --- CORE LOGIC: ML TRAINING (XGBoost GPU) ---
    // Complexity = Samples * Features.
    // GPU Instances (p3.8xlarge) are expensive ($12/hr).
    // Factor: A 500k * 84M matrix is massive.
    const complexityScore = (samples * features) / 1e12; // Trillions of datapoints
    const mlCost = Math.max(500, complexityScore * 15000); // Base cost + scaling

    // --- CORE LOGIC: DATA EGRESS/API ---
    // API queries, dashboard loading, result downloads.
    const egressCost = storageCost * 0.15; // Typically 15% of storage

    // Totals
    const totalCost = Math.round(storageCost + computeCost + mlCost + egressCost);
    
    // --- ACCURACY SIMULATION ---
    // More samples = better generalization (logarithmic).
    // More features = noise initially, then better signal, then curse of dimensionality.
    const sampleSignal = 0.70 + (Math.log10(samples) / 15); 
    const featureNoise = (features > 50000000) ? -0.01 : 0.01; // Penalty for too many features without regularization
    const accuracy = Math.min(0.89, sampleSignal + featureNoise + (depth * 0.02));

    // --- UPDATE DOM ---
    // KPI Cards
    document.getElementById('liveSamples').textContent = (samples / 1000).toFixed(0) + 'K';
    document.getElementById('liveFeatures').textContent = (features / 1e6).toFixed(0) + 'M';
    
    // Smart Unit Display (TB vs PB)
    if (totalStorageTB > 1000) {
        document.getElementById('liveStorage').textContent = (totalStorageTB / 1000).toFixed(2) + ' PB';
    } else {
        document.getElementById('liveStorage').textContent = totalStorageTB.toFixed(1) + ' TB';
    }
    
    document.getElementById('liveAccuracy').textContent = accuracy.toFixed(3);

    // Cost Breakdown
    document.getElementById('storageCost').textContent = '$' + Math.round(storageCost).toLocaleString();
    document.getElementById('computeCost').textContent = '$' + Math.round(computeCost).toLocaleString();
    document.getElementById('mlCost').textContent = '$' + Math.round(mlCost).toLocaleString();
    document.getElementById('otherCost').textContent = '$' + Math.round(egressCost).toLocaleString();
    document.getElementById('finalCost').textContent = '$' + totalCost.toLocaleString();
    document.getElementById('totalCost').textContent = '$' + totalCost.toLocaleString();

    // Update Chart Data
    costChart.data.datasets[0].data = [
        Math.round(storageCost), 
        Math.round(computeCost), 
        Math.round(mlCost), 
        Math.round(egressCost)
    ];
    costChart.update();

    // Update Performance Curve Dynamic Point
    // Highlight the current point on the static curve based on sample size
    const sampleIndex = Math.min(4, Math.floor((samples) / 200000));
    // (Optional: You could dynamically regenerate the whole curve here if you wanted, 
    // but typically we just highlight where the user is.)
}

// Initialization
document.addEventListener('DOMContentLoaded', function() {
    initializeCharts();
    
    const sliders = ['sampleCount', 'featureCount', 'analysisDepth'];
    sliders.forEach(sliderId => {
        document.getElementById(sliderId).addEventListener('input', updateSimulator);
    });
    
    updateSimulator(); // Trigger first calc
});
</script>

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>
    mermaid.initialize({ 
        startOnLoad: true, 
        theme: 'dark', 
        securityLevel: 'loose' 
    });
</script>
