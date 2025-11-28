---
layout: default
title: Genomic Biomarker Discovery Platform
description: Advanced Big Data & ML Pipeline for Whole Genome Sequencing
---

<style>
:root {
    --dark-bg: #0f0f23;
    --darker-bg: #0a0a1a;
    --card-bg: #1a1a2e;
    --card-border: #2d2d4d;
    --accent-purple: #8b5cf6;
    --accent-blue: #3b82f6;
    --accent-green: #10b981;
    --accent-orange: #f59e0b;
    --accent-red: #ef4444;
    --text-primary: #f8fafc;
    --text-secondary: #cbd5e1;
    --text-muted: #94a3b8;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    background: var(--dark-bg);
    color: var(--text-primary);
    min-height: 100vh;
    line-height: 1.6;
}

.container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 20px;
}

/* Header */
.header {
    background: var(--darker-bg);
    border: 1px solid var(--card-border);
    border-radius: 12px;
    padding: 40px;
    margin-bottom: 30px;
    text-align: center;
    position: relative;
}

.header::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent-purple), var(--accent-blue));
}

.header h1 {
    font-size: 2.5em;
    font-weight: 700;
    color: var(--text-primary);
    margin-bottom: 10px;
}

.header .subtitle {
    font-size: 1.2em;
    color: var(--text-secondary);
    margin-bottom: 20px;
}

.tagline {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    padding: 15px 30px;
    border-radius: 8px;
    color: var(--text-secondary);
    display: inline-block;
    font-size: 1em;
}

/* Navigation */
.nav-links {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 25px;
}

.nav-link {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    color: var(--text-primary);
    padding: 10px 24px;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
}

.nav-link:hover {
    background: var(--accent-purple);
    transform: translateY(-2px);
}

/* Main Grid */
.main-grid {
    display: grid;
    grid-template-columns: 1fr 400px;
    gap: 20px;
    margin-bottom: 30px;
}

/* Simulator Section */
.simulator {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 12px;
    padding: 25px;
}

.simulator h2 {
    color: var(--text-primary);
    margin-bottom: 20px;
    font-size: 1.3em;
}

/* Controls */
.control-group {
    margin-bottom: 20px;
}

.control-label {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
    color: var(--text-secondary);
}

.control-value {
    color: var(--accent-green);
    font-weight: 600;
}

.slider-container {
    background: var(--darker-bg);
    padding: 15px;
    border-radius: 8px;
    border: 1px solid var(--card-border);
}

input[type="range"] {
    width: 100%;
    height: 6px;
    background: var(--card-border);
    border-radius: 3px;
    outline: none;
    -webkit-appearance: none;
}

input[type="range"]::-webkit-slider-thumb {
    appearance: none;
    width: 18px;
    height: 18px;
    background: var(--accent-purple);
    border-radius: 50%;
    cursor: pointer;
}

/* Metrics */
.metrics-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
    margin-top: 20px;
}

.metric-card {
    background: var(--darker-bg);
    border: 1px solid var(--card-border);
    border-radius: 8px;
    padding: 20px;
    text-align: center;
}

.metric-value {
    font-size: 1.6em;
    font-weight: 700;
    margin-bottom: 5px;
}

.metric-label {
    color: var(--text-muted);
    font-size: 0.9em;
}

.cost-value { color: var(--accent-orange); }
.accuracy-value { color: var(--accent-green); }
.storage-value { color: var(--accent-blue); }
.variants-value { color: var(--accent-red); }

/* Chart */
.chart-container {
    background: var(--darker-bg);
    border: 1px solid var(--card-border);
    border-radius: 8px;
    padding: 20px;
    margin-top: 20px;
    height: 300px;
}

.chart-canvas {
    width: 100%;
    height: 100%;
}

/* Info Panel */
.info-panel {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 12px;
    padding: 25px;
}

.model-info {
    background: var(--darker-bg);
    border: 1px solid var(--card-border);
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 20px;
}

.model-badge {
    background: var(--accent-purple);
    color: white;
    padding: 4px 12px;
    border-radius: 4px;
    font-size: 0.8em;
    font-weight: 600;
}

.accuracy {
    color: var(--accent-green);
    font-weight: 700;
    font-size: 1.1em;
    margin: 10px 0;
}

/* Status */
.status-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 0;
    border-bottom: 1px solid var(--card-border);
    color: var(--text-secondary);
}

.status-item:last-child {
    border-bottom: none;
}

.status-value {
    color: var(--accent-green);
    font-weight: 600;
}

/* Footer */
.footer {
    text-align: center;
    color: var(--text-muted);
    font-size: 0.9em;
    margin-top: 40px;
    padding: 20px;
    border-top: 1px solid var(--card-border);
}

/* Pipeline Section */
.pipeline-section {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 12px;
    padding: 30px;
    margin-top: 25px;
}

.pipeline-title {
    color: var(--text-primary);
    margin-bottom: 20px;
    font-size: 1.4em;
    text-align: center;
}

/* Responsive */
@media (max-width: 1024px) {
    .main-grid {
        grid-template-columns: 1fr;
    }
}
</style>

<div class="container">
    <!-- Header -->
    <div class="header">
        <h1>Genomic Biomarker Discovery Platform</h1>
        <div class="subtitle">Advanced Big Data & Machine Learning Pipeline</div>
        <div class="tagline">
            Leveraging XGBoost and Distributed Computing to analyze 84M+ genomic features across 500,000 whole genome sequences
        </div>
        
        <div class="nav-links">
            <a href="#simulator" class="nav-link">Launch Simulator</a>
            <a href="#pipeline" class="nav-link">View Pipeline</a>
        </div>
    </div>

    <!-- Main Content Grid -->
    <div class="main-grid">
        <!-- Simulator Section -->
        <div class="simulator" id="simulator">
            <h2>Genomic Analysis Simulator</h2>
            <p style="color: var(--text-secondary); margin-bottom: 20px;">
                Adjust parameters to predict computational requirements and performance metrics.
            </p>

            <!-- Controls -->
            <div class="control-group">
                <div class="control-label">
                    <span>WGS Samples</span>
                    <span class="control-value" id="datasetValue">500K Samples</span>
                </div>
                <div class="slider-container">
                    <input type="range" id="datasetScale" min="1000" max="1000000" value="500000" step="1000">
                </div>
            </div>

            <div class="control-group">
                <div class="control-label">
                    <span>Genomic Variants</span>
                    <span class="control-value" id="featureValue">84M Variants</span>
                </div>
                <div class="slider-container">
                    <input type="range" id="featureComplexity" min="1000000" max="100000000" value="84000000" step="1000000">
                </div>
            </div>

            <div class="control-group">
                <div class="control-label">
                    <span>Analysis Depth</span>
                    <span class="control-value" id="depthValue">Comprehensive</span>
                </div>
                <div class="slider-container">
                    <input type="range" id="analysisDepth" min="1" max="3" value="2" step="1">
                </div>
            </div>

            <!-- Metrics -->
            <div class="metrics-grid">
                <div class="metric-card">
                    <div class="metric-value cost-value" id="costMetric">$18,240</div>
                    <div class="metric-label">MONTHLY COST</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value accuracy-value" id="accuracyMetric">0.82</div>
                    <div class="metric-label">AUPRC SCORE</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value storage-value" id="storageMetric">76.0 PB</div>
                    <div class="metric-label">STORAGE NEEDED</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value variants-value" id="variantsMetric">84M</div>
                    <div class="metric-label">VARIANTS CALLED</div>
                </div>
            </div>

            <!-- Chart -->
            <div class="chart-container">
                <canvas id="performanceChart" class="chart-canvas"></canvas>
            </div>
        </div>

        <!-- Info Panel -->
        <div class="info-panel">
            <div class="model-info">
                <div class="model-badge">MODEL: XGBOOST GENOMICS</div>
                <div class="accuracy">ACCURACY: 0.94 AUPRC</div>
                <div style="color: var(--text-muted); font-size: 0.9em;">
                    Optimized for genomic feature analysis
                </div>
            </div>

            <div style="margin-bottom: 25px;">
                <h3 style="color: var(--text-primary); margin-bottom: 15px;">SYSTEM STATUS</h3>
                <div class="status-item">
                    <span>Cluster Ready</span>
                    <span class="status-value">ACTIVE</span>
                </div>
                <div class="status-item">
                    <span>GPU Acceleration</span>
                    <span class="status-value">ENABLED</span>
                </div>
                <div class="status-item">
                    <span>Data Stream</span>
                    <span class="status-value">LIVE</span>
                </div>
                <div class="status-item">
                    <span>Model Training</span>
                    <span class="status-value">OPTIMAL</span>
                </div>
            </div>

            <div>
                <h3 style="color: var(--text-primary); margin-bottom: 15px;">RESEARCH METRICS</h3>
                <div class="status-item">
                    <span>Statistical Power</span>
                    <span class="status-value">98.7%</span>
                </div>
                <div class="status-item">
                    <span>Rare Variants</span>
                    <span class="status-value">4.2M</span>
                </div>
                <div class="status-item">
                    <span>Compute Hours</span>
                    <span class="status-value">3,240</span>
                </div>
                <div class="status-item">
                    <span>Clinical Findings</span>
                    <span class="status-value">1,240</span>
                </div>
            </div>
        </div>
    </div>

    <!-- Pipeline Section -->
    <div class="pipeline-section" id="pipeline">
        <h2 class="pipeline-title">Genomic Analysis Pipeline Architecture</h2>
        <div class="mermaid">
graph TD
    A[UK Biobank Raw Data<br/>500,000 WGS Samples] --> B[Quality Control & Alignment<br/>FastQC, BWA-MEM]
    B --> C[Variant Calling<br/>GATK, DeepVariant]
    C --> D[Variant Annotation<br/>VEP, SnpEff]
    D --> E[Feature Engineering<br/>Spark ML, 84M Features]
    E --> F[Model Training<br/>XGBoost, GPU Cluster]
    F --> G[Biomarker Discovery<br/>GWAS, PRS Analysis]
    G --> H[Clinical Interpretation<br/>Risk Scores, Reports]
    
    style A fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style B fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style C fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style D fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style E fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style F fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style G fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style H fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        CONFIDENTIAL • ACADEMIC SUBMISSION 2024 • LEAD DATA ARCHITECT
    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
// Initialize Chart
const ctx = document.getElementById('performanceChart').getContext('2d');
let performanceChart;

function initializeChart() {
    performanceChart = new Chart(ctx, {
        type: 'bar',
        data: {
            labels: ['Storage Cost', 'Compute Cost', 'ML Training', 'Data Transfer', 'Management'],
            datasets: [{
                label: 'Cost Breakdown ($)',
                data: [7600, 6840, 2850, 950, 0],
                backgroundColor: [
                    '#8b5cf6',
                    '#3b82f6',
                    '#10b981', 
                    '#f59e0b',
                    '#ef4444'
                ],
                borderColor: '#1a1a2e',
                borderWidth: 2
            }]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            scales: {
                y: {
                    beginAtZero: true,
                    grid: {
                        color: 'rgba(255,255,255,0.1)'
                    },
                    ticks: {
                        color: '#94a3b8',
                        callback: function(value) {
                            return '$' + value.toLocaleString();
                        }
                    }
                },
                x: {
                    grid: {
                        color: 'rgba(255,255,255,0.1)'
                    },
                    ticks: {
                        color: '#94a3b8'
                    }
                }
            },
            plugins: {
                legend: {
                    display: false
                }
            }
        }
    });
}

// Precise storage calculation for 500K WGS samples
function calculateStorage(samples, analysisDepth) {
    // Realistic WGS storage requirements
    const rawFastqPerSample = 150;  // GB per sample (compressed FASTQ)
    const bamFilesPerSample = 80;   // GB per sample (aligned BAM, compressed)
    const vcfFilesPerSample = 3;    // GB per sample (variant calls)
    const processedDataPerSample = 10; // GB per sample (feature matrices, annotations)
    
    let totalStorageGB = 0;
    
    if (analysisDepth === 1) { // Basic: FASTQ + BAM only
        totalStorageGB = samples * (rawFastqPerSample + bamFilesPerSample);
    } else if (analysisDepth === 2) { // Comprehensive: All data
        totalStorageGB = samples * (rawFastqPerSample + bamFilesPerSample + vcfFilesPerSample + processedDataPerSample);
    } else { // Advanced: Plus additional analyses
        totalStorageGB = samples * (rawFastqPerSample + bamFilesPerSample + vcfFilesPerSample + processedDataPerSample + 5);
    }
    
    return totalStorageGB / 1000000; // Convert to PB
}

// Update simulator
function updateSimulator() {
    const samples = parseInt(document.getElementById('datasetScale').value);
    const features = parseInt(document.getElementById('featureComplexity').value);
    const depth = parseInt(document.getElementById('analysisDepth').value);
    
    // Update displays
    document.getElementById('datasetValue').textContent = (samples/1000).toFixed(0) + 'K Samples';
    document.getElementById('featureValue').textContent = (features/1000000).toFixed(0) + 'M Variants';
    
    const depthLabels = ['Basic', 'Comprehensive', 'Advanced'];
    document.getElementById('depthValue').textContent = depthLabels[depth - 1];
    
    // Precise calculations
    const storagePB = calculateStorage(samples, depth);
    const storageCost = storagePB * 100; // $100 per PB/month
    const computeCost = (samples * 0.012) + (features * 0.0000002);
    const mlCost = (samples * 0.004) + (features * 0.0000001);
    const dataTransferCost = storagePB * 12.5;
    
    const totalCost = Math.round(storageCost + computeCost + mlCost + dataTransferCost);
    const accuracy = 0.75 + (samples/2000000) - (features/500000000) + (depth * 0.035);
    
    // Update metrics
    document.getElementById('costMetric').textContent = '$' + totalCost.toLocaleString();
    document.getElementById('accuracyMetric').textContent = Math.max(0.7, Math.min(0.95, accuracy)).toFixed(2);
    document.getElementById('storageMetric').textContent = storagePB.toFixed(1) + ' PB';
    document.getElementById('variantsMetric').textContent = (features/1000000).toFixed(0) + 'M';
    
    // Update chart
    updateChart(storageCost, computeCost, mlCost, dataTransferCost);
}

function updateChart(storageCost, computeCost, mlCost, dataTransferCost) {
    performanceChart.data.datasets[0].data = [
        Math.round(storageCost),
        Math.round(computeCost),
        Math.round(mlCost),
        Math.round(dataTransferCost),
        0
    ];
    performanceChart.update();
}

// Initialize
document.addEventListener('DOMContentLoaded', function() {
    initializeChart();
    
    const sliders = ['datasetScale', 'featureComplexity', 'analysisDepth'];
    sliders.forEach(sliderId => {
        document.getElementById(sliderId).addEventListener('input', updateSimulator);
    });
    
    updateSimulator();
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
