---
layout: default
title: Genomic AI Platform
description: Enterprise Genomic Analysis | Advanced ML Pipeline
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
    font-family: 'SF Mono', 'Monaco', 'Consolas', monospace;
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
    font-size: 2.8em;
    font-weight: 700;
    background: linear-gradient(135deg, var(--accent-purple), var(--accent-blue));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 10px;
}

.header .subtitle {
    font-size: 1.3em;
    color: var(--text-secondary);
    margin-bottom: 25px;
}

.tagline {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    padding: 20px 35px;
    border-radius: 8px;
    color: var(--text-secondary);
    display: inline-block;
    font-size: 1.1em;
}

/* Navigation */
.nav-links {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 30px;
}

.nav-link {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    color: var(--text-primary);
    padding: 12px 28px;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
}

.nav-link:hover {
    background: var(--accent-purple);
    transform: translateY(-2px);
    box-shadow: 0 4px 20px rgba(139, 92, 246, 0.3);
}

/* Main Grid */
.main-grid {
    display: grid;
    grid-template-columns: 1fr 400px;
    gap: 25px;
    margin-bottom: 30px;
}

/* Simulator Section */
.simulator {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 12px;
    padding: 30px;
}

.simulator h2 {
    color: var(--text-primary);
    margin-bottom: 25px;
    font-size: 1.4em;
    display: flex;
    align-items: center;
    gap: 10px;
}

/* Controls */
.control-group {
    margin-bottom: 25px;
}

.control-label {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 15px;
    color: var(--text-secondary);
}

.control-value {
    color: var(--accent-green);
    font-weight: 600;
}

.slider-container {
    background: var(--darker-bg);
    padding: 20px;
    border-radius: 8px;
    border: 1px solid var(--card-border);
    position: relative;
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
    width: 20px;
    height: 20px;
    background: var(--accent-purple);
    border-radius: 50%;
    cursor: pointer;
    box-shadow: 0 2px 10px rgba(139, 92, 246, 0.4);
    transition: all 0.3s ease;
}

input[type="range"]::-webkit-slider-thumb:hover {
    transform: scale(1.2);
    background: var(--accent-blue);
}

/* Metrics */
.metrics-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
    margin-top: 25px;
}

.metric-card {
    background: var(--darker-bg);
    border: 1px solid var(--card-border);
    border-radius: 8px;
    padding: 20px;
    text-align: center;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
}

.metric-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: var(--accent-purple);
}

.metric-card.increasing {
    border-color: var(--accent-red);
    animation: pulseIncrease 1s ease-in-out;
}

.metric-card.decreasing {
    border-color: var(--accent-green);
    animation: pulseDecrease 1s ease-in-out;
}

.metric-value {
    font-size: 1.8em;
    font-weight: 700;
    margin-bottom: 5px;
    transition: all 0.3s ease;
}

.metric-label {
    color: var(--text-muted);
    font-size: 0.9em;
}

.cost-value { color: var(--accent-orange); }
.accuracy-value { color: var(--accent-green); }
.storage-value { color: var(--accent-blue); }
.compute-value { color: var(--accent-purple); }
.variants-value { color: var(--accent-red); }

/* Chart */
.chart-container {
    background: var(--darker-bg);
    border: 1px solid var(--card-border);
    border-radius: 8px;
    padding: 25px;
    margin-top: 25px;
    height: 350px;
    position: relative;
    overflow: hidden;
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
    font-size: 1.2em;
    margin: 10px 0;
}

/* Status */
.status-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 12px 0;
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

/* Research Metrics */
.research-metrics {
    background: var(--darker-bg);
    border: 1px solid var(--card-border);
    border-radius: 8px;
    padding: 20px;
    margin-top: 20px;
}

.metric-detail {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 0;
    border-bottom: 1px solid var(--card-border);
    font-size: 0.9em;
}

.metric-detail:last-child {
    border-bottom: none;
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
}

/* Animations */
@keyframes pulseIncrease {
    0% { box-shadow: 0 0 0 0 rgba(239, 68, 68, 0.4); }
    70% { box-shadow: 0 0 0 10px rgba(239, 68, 68, 0); }
    100% { box-shadow: 0 0 0 0 rgba(239, 68, 68, 0); }
}

@keyframes pulseDecrease {
    0% { box-shadow: 0 0 0 0 rgba(16, 185, 129, 0.4); }
    70% { box-shadow: 0 0 0 10px rgba(16, 185, 129, 0); }
    100% { box-shadow: 0 0 0 0 rgba(16, 185, 129, 0); }
}

@keyframes valueChange {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}

.value-changing {
    animation: valueChange 0.3s ease-in-out;
}

/* Responsive */
@media (max-width: 1024px) {
    .main-grid {
        grid-template-columns: 1fr;
    }
    
    .container {
        padding: 15px;
    }
    
    .metrics-grid {
        grid-template-columns: 1fr;
    }
}
</style>

<div class="container">
    <!-- Header -->
    <div class="header">
        <h1>Genomic AI Platform</h1>
        <div class="subtitle">Enterprise Genomic Analysis | Advanced ML Pipeline</div>
        <div class="tagline">
            Leveraging XGBoost and Distributed Computing to analyze 84M+ genomic features
        </div>
        
        <div class="nav-links">
            <a href="#simulator" class="nav-link">Launch Simulator</a>
            <a href="#pipeline" class="nav-link">View Pipeline</a>
            <a href="#case-study" class="nav-link">Case Study</a>
        </div>
    </div>

    <!-- Main Content Grid -->
    <div class="main-grid">
        <!-- Simulator Section -->
        <div class="simulator" id="simulator">
            <h2>🧬 Genomic Analysis Simulator</h2>
            <p style="color: var(--text-secondary); margin-bottom: 25px;">
                Adjust parameters to predict computational requirements and research impact metrics.
            </p>

            <!-- Controls -->
            <div class="control-group">
                <div class="control-label">
                    <span>WGS_SAMPLES</span>
                    <span class="control-value" id="datasetValue">500K Samples</span>
                </div>
                <div class="slider-container">
                    <input type="range" id="datasetScale" min="1000" max="1000000" value="500000" step="1000">
                </div>
            </div>

            <div class="control-group">
                <div class="control-label">
                    <span>GENOMIC_FEATURES</span>
                    <span class="control-value" id="featureValue">84M Variants</span>
                </div>
                <div class="slider-container">
                    <input type="range" id="featureComplexity" min="1000000" max="100000000" value="84000000" step="1000000">
                </div>
            </div>

            <div class="control-group">
                <div class="control-label">
                    <span>ANALYSIS_DEPTH</span>
                    <span class="control-value" id="depthValue">Comprehensive</span>
                </div>
                <div class="slider-container">
                    <input type="range" id="analysisDepth" min="1" max="3" value="2" step="1">
                </div>
            </div>

            <!-- Metrics -->
            <div class="metrics-grid">
                <div class="metric-card" id="costCard">
                    <div class="metric-value cost-value" id="costMetric">$12,847</div>
                    <div class="metric-label">MONTHLY_COST</div>
                </div>
                <div class="metric-card" id="accuracyCard">
                    <div class="metric-value accuracy-value" id="accuracyMetric">0.81</div>
                    <div class="metric-label">AUPRC_SCORE</div>
                </div>
                <div class="metric-card" id="storageCard">
                    <div class="metric-value storage-value" id="storageMetric">2.98 PB</div>
                    <div class="metric-label">STORAGE_NEEDED</div>
                </div>
                <div class="metric-card" id="variantsCard">
                    <div class="metric-value variants-value" id="variantsMetric">84M</div>
                    <div class="metric-label">VARIANTS_CALLED</div>
                </div>
            </div>

            <!-- Research Impact Metrics -->
            <div class="research-metrics">
                <h4 style="color: var(--text-primary); margin-bottom: 15px;">RESEARCH_IMPACT</h4>
                <div class="metric-detail">
                    <span>Statistical Power</span>
                    <span class="status-value" id="powerMetric">98.7%</span>
                </div>
                <div class="metric-detail">
                    <span>Rare Variants (MAF < 0.01)</span>
                    <span class="status-value" id="rareVariants">4.2M</span>
                </div>
                <div class="metric-detail">
                    <span>Pathogenic Findings</span>
                    <span class="status-value" id="pathogenicMetric">~1,240</span>
                </div>
                <div class="metric-detail">
                    <span>Compute Hours Needed</span>
                    <span class="status-value" id="computeHours">3,240</span>
                </div>
            </div>

            <!-- New Chart: Genomic Discovery Potential -->
            <div class="chart-container">
                <canvas id="discoveryChart" class="chart-canvas"></canvas>
            </div>
        </div>

        <!-- Info Panel -->
        <div class="info-panel">
            <div class="model-info">
                <div class="model-badge">MODEL: XGBOOST_V4_GENOMICS</div>
                <div class="accuracy">ACCURACY: 0.94 AUPRC</div>
                <div style="color: var(--text-muted); font-size: 0.9em;">
                    Optimized for polygenic risk prediction
                </div>
            </div>

            <div style="margin-bottom: 25px;">
                <h3 style="color: var(--text-primary); margin-bottom: 15px;">GENOMIC_STATISTICS</h3>
                <div class="status-item">
                    <span>Coverage Depth</span>
                    <span class="status-value">30x</span>
                </div>
                <div class="status-item">
                    <span>Variant Call Rate</span>
                    <span class="status-value">99.2%</span>
                </div>
                <div class="status-item">
                    <span>QC Pass Rate</span>
                    <span class="status-value">97.8%</span>
                </div>
                <div class="status-item">
                    <span>Annotation Complete</span>
                    <span class="status-value">100%</span>
                </div>
            </div>

            <div>
                <h3 style="color: var(--text-primary); margin-bottom: 15px;">CLINICAL_METRICS</h3>
                <div class="status-item">
                    <span>Disease Associations</span>
                    <span class="status-value">142</span>
                </div>
                <div class="status-item">
                    <span>Drug Targets</span>
                    <span class="status-value">67</span>
                </div>
                <div class="status-item">
                    <span>Biomarkers Found</span>
                    <span class="status-value">89</span>
                </div>
                <div class="status-item">
                    <span>Heritability Explained</span>
                    <span class="status-value">38%</span>
                </div>
            </div>
        </div>
    </div>

    <!-- Pipeline Section -->
    <div class="pipeline-section" id="pipeline">
        <h2 class="pipeline-title">GENOMIC_ANALYSIS_PIPELINE</h2>
        <div class="mermaid">
graph TD
    A[FASTQ Raw Sequences<br/>~300GB/sample] --> B[Alignment & QC<br/>BWA-MEM, FastQC]
    B --> C[Variant Calling<br/>GATK, FreeBayes]
    C --> D[Variant Annotation<br/>VEP, ANNOVAR]
    D --> E[Quality Filtering<br/>VQSR, Hard Filters]
    E --> F[Feature Matrix<br/>84M variants × 500K samples]
    F --> G[ML Training<br/>XGBoost, Spark ML]
    G --> H[Risk Prediction<br/>Polygenic Scores]
    H --> I[Biomarker Discovery<br/>GWAS, PRS]
    
    style A fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style B fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style C fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style D fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style E fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style F fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style G fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style H fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style I fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        CONFIDENTIAL • ACADEMIC SUBMISSION 2024 • LEAD GENOMIC ARCHITECT
    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
// Store previous values for animation
let previousValues = {
    cost: 12847,
    accuracy: 0.81,
    storage: 2.98,
    variants: 84000000
};

// Initialize Discovery Chart
const ctx = document.getElementById('discoveryChart').getContext('2d');
let discoveryChart;

function initializeChart() {
    discoveryChart = new Chart(ctx, {
        type: 'bar',
        data: {
            labels: ['Common Variants', 'Rare Variants', 'Structural Variants', 'Novel Findings', 'Clinical Actionable'],
            datasets: [{
                label: 'Discovery Potential',
                data: [65, 23, 8, 3, 1],
                backgroundColor: [
                    '#8b5cf6',
                    '#3b82f6', 
                    '#10b981',
                    '#f59e0b',
                    '#ef4444'
                ],
                borderColor: '#1a1a2e',
                borderWidth: 2,
                borderRadius: 6
            }]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            scales: {
                y: {
                    beginAtZero: true,
                    max: 100,
                    grid: {
                        color: 'rgba(255,255,255,0.1)'
                    },
                    ticks: {
                        color: '#94a3b8',
                        callback: function(value) {
                            return value + '%';
                        }
                    },
                    title: {
                        display: true,
                        text: 'Discovery Percentage',
                        color: '#cbd5e1'
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
                },
                tooltip: {
                    callbacks: {
                        label: function(context) {
                            return context.parsed.y + '% of significant findings';
                        }
                    }
                }
            }
        }
    });
}

// Precise storage calculations for WGS data
function calculateStorage(samples, analysisDepth) {
    // WGS storage breakdown (more realistic)
    const rawFastqPerSample = 100; // GB per sample (compressed FASTQ)
    const bamFilesPerSample = 50;  // GB per sample (aligned BAM)
    const vcfFilesPerSample = 2;   // GB per sample (compressed VCF)
    const processedDataPerSample = 5; // GB per sample (processed matrices)
    
    let totalStorage = 0;
    
    if (analysisDepth === 1) { // Basic analysis
        totalStorage = samples * (rawFastqPerSample + bamFilesPerSample) / 1000; // Convert to TB
    } else if (analysisDepth === 2) { // Comprehensive analysis
        totalStorage = samples * (rawFastqPerSample + bamFilesPerSample + vcfFilesPerSample) / 1000;
    } else { // Advanced analysis (includes all processed data)
        totalStorage = samples * (rawFastqPerSample + bamFilesPerSample + vcfFilesPerSample + processedDataPerSample) / 1000;
    }
    
    return totalStorage / 1000; // Convert TB to PB
}

// Update simulator values with precise calculations
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
    const baseCost = (samples * 0.015) + (features * 0.0000003) + (storagePB * 3500) + (depth * 800);
    const cost = Math.round(baseCost);
    const accuracy = 0.70 + (samples/1500000) - (features/400000000) + (depth * 0.05);
    const statisticalPower = 85 + (samples/20000) + (depth * 4);
    const rareVariants = Math.round(features * 0.05); // 5% are rare variants
    const pathogenicFindings = Math.round(samples * 0.0025); // 0.25% have pathogenic variants
    const computeHours = samples * 0.006 + features * 0.0000001 + depth * 200;
    
    // Update metrics with animations
    updateMetricWithAnimation('costMetric', cost, previousValues.cost, 'costCard', '$');
    updateMetricWithAnimation('accuracyMetric', accuracy, previousValues.accuracy, 'accuracyCard', '', 2);
    updateMetricWithAnimation('storageMetric', storagePB, previousValues.storage, 'storageCard', '', 2, ' PB');
    updateMetricWithAnimation('variantsMetric', features, previousValues.variants, 'variantsCard', '', 0, '', true);
    
    // Update research metrics
    document.getElementById('powerMetric').textContent = Math.min(99.9, statisticalPower).toFixed(1) + '%';
    document.getElementById('rareVariants').textContent = (rareVariants/1000000).toFixed(1) + 'M';
    document.getElementById('pathogenicMetric').textContent = '~' + pathogenicFindings.toLocaleString();
    document.getElementById('computeHours').textContent = Math.round(computeHours).toLocaleString();
    
    // Store current values
    previousValues = { cost, accuracy, storage: storagePB, variants: features };
    
    // Update chart based on sample size
    updateChart(samples);
}

function updateMetricWithAnimation(elementId, newValue, oldValue, cardId, prefix = '', decimals = 0, suffix = '', compact = false) {
    const element = document.getElementById(elementId);
    const card = document.getElementById(cardId);
    
    // Add animation class based on value change
    if (newValue > oldValue) {
        card.classList.add('increasing');
        setTimeout(() => card.classList.remove('increasing'), 1000);
    } else if (newValue < oldValue) {
        card.classList.add('decreasing');
        setTimeout(() => card.classList.remove('decreasing'), 1000);
    }
    
    // Add value change animation
    element.classList.add('value-changing');
    setTimeout(() => element.classList.remove('value-changing'), 300);
    
    // Update value
    let formattedValue;
    if (compact && newValue >= 1000000) {
        formattedValue = (newValue/1000000).toFixed(1) + 'M';
    } else {
        formattedValue = decimals > 0 ? newValue.toFixed(decimals) : newValue.toLocaleString();
    }
    element.textContent = prefix + formattedValue + suffix;
}

function updateChart(samples) {
    // Update discovery potential based on sample size
    const sampleFactor = Math.min(1, samples / 500000);
    
    discoveryChart.data.datasets[0].data = [
        65 * sampleFactor,
        23 * (0.5 + sampleFactor * 0.5),
        8 * (0.3 + sampleFactor * 0.7),
        3 * (0.1 + sampleFactor * 0.9),
        1 * (0.05 + sampleFactor * 0.95)
    ];
    
    discoveryChart.update('none');
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
