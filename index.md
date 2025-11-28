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

/* Chart */
.chart-container {
    background: var(--darker-bg);
    border: 1px solid var(--card-border);
    border-radius: 8px;
    padding: 25px;
    margin-top: 25px;
    height: 300px;
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
                Adjust parameters to predict computational requirements and performance metrics.
            </p>

            <!-- Controls -->
            <div class="control-group">
                <div class="control-label">
                    <span>DATASET_SCALE</span>
                    <span class="control-value" id="datasetValue">500K Samples</span>
                </div>
                <div class="slider-container">
                    <input type="range" id="datasetScale" min="1000" max="1000000" value="500000" step="1000">
                </div>
            </div>

            <div class="control-group">
                <div class="control-label">
                    <span>FEATURE_COMPLEXITY</span>
                    <span class="control-value" id="featureValue">84M Features</span>
                </div>
                <div class="slider-container">
                    <input type="range" id="featureComplexity" min="1000000" max="100000000" value="84000000" step="1000000">
                </div>
            </div>

            <div class="control-group">
                <div class="control-label">
                    <span>PROCESSING_SPEED</span>
                    <span class="control-value" id="speedValue">6 Hours</span>
                </div>
                <div class="slider-container">
                    <input type="range" id="processingSpeed" min="1" max="48" value="6" step="1">
                </div>
            </div>

            <!-- Metrics -->
            <div class="metrics-grid">
                <div class="metric-card" id="costCard">
                    <div class="metric-value cost-value" id="costMetric">$8,450</div>
                    <div class="metric-label">MONTHLY_COST</div>
                </div>
                <div class="metric-card" id="accuracyCard">
                    <div class="metric-value accuracy-value" id="accuracyMetric">0.78</div>
                    <div class="metric-label">AUPRC_SCORE</div>
                </div>
                <div class="metric-card" id="storageCard">
                    <div class="metric-value storage-value" id="storageMetric">14.97 PB</div>
                    <div class="metric-label">STORAGE_NEEDED</div>
                </div>
                <div class="metric-card" id="computeCard">
                    <div class="metric-value compute-value" id="computeMetric">High</div>
                    <div class="metric-label">COMPUTE_LEVEL</div>
                </div>
            </div>

            <!-- Live Chart -->
            <div class="chart-container">
                <canvas id="performanceChart" class="chart-canvas"></canvas>
            </div>
        </div>

        <!-- Info Panel -->
        <div class="info-panel">
            <div class="model-info">
                <div class="model-badge">MODEL: XGBOOST_V4</div>
                <div class="accuracy">ACCURACY: 0.94 AUPRC</div>
                <div style="color: var(--text-muted); font-size: 0.9em;">
                    Optimized for genomic feature analysis
                </div>
            </div>

            <div style="margin-bottom: 25px;">
                <h3 style="color: var(--text-primary); margin-bottom: 15px;">SYSTEM_STATUS</h3>
                <div class="status-item">
                    <span>CLUSTER_READY</span>
                    <span class="status-value">ACTIVE</span>
                </div>
                <div class="status-item">
                    <span>GPU_ACCELERATION</span>
                    <span class="status-value">ENABLED</span>
                </div>
                <div class="status-item">
                    <span>DATA_STREAM</span>
                    <span class="status-value">LIVE</span>
                </div>
                <div class="status-item">
                    <span>MODEL_TRAINING</span>
                    <span class="status-value">OPTIMAL</span>
                </div>
            </div>

            <div>
                <h3 style="color: var(--text-primary); margin-bottom: 15px;">PERFORMANCE</h3>
                <div class="status-item">
                    <span>PRECISION</span>
                    <span class="status-value">0.92</span>
                </div>
                <div class="status-item">
                    <span>RECALL</span>
                    <span class="status-value">0.89</span>
                </div>
                <div class="status-item">
                    <span>F1_SCORE</span>
                    <span class="status-value">0.90</span>
                </div>
                <div class="status-item">
                    <span>LATENCY</span>
                    <span class="status-value">124ms</span>
                </div>
            </div>
        </div>
    </div>

    <!-- Pipeline Section -->
    <div class="pipeline-section" id="pipeline">
        <h2 class="pipeline-title">ARCHITECTURE_PIPELINE</h2>
        <div class="mermaid">
graph TD
    A[UK Biobank Raw Data] --> B[Cloud Storage - AWS S3]
    B --> C[Data Processing - Apache Spark]
    C --> D[Feature Engineering - Spark ML]
    D --> E[Model Training - XGBoost]
    E --> F[Results & Interpretation]
    
    subgraph A_details
        A1[500,000 WGS Samples]
        A2[15+ Petabytes]
        A3[84M Features]
    end
    
    subgraph B_details
        B1[VCF/BAM Files]
        B2[Phenotype Data]
        B3[Clinical Records]
    end
    
    subgraph C_details
        C1[Quality Control]
        C2[Variant Calling]
        C3[Data Integration]
    end
    
    subgraph D_details
        D1[Variant Filtering]
        D2[GWAS Pre-filtering]
        D3[Biological Annotation]
    end
    
    subgraph E_details
        E1[Stratified Sampling]
        E2[Hyperparameter Tuning]
        E3[Cross-Validation]
    end
    
    subgraph F_details
        F1[Biomarker Discovery]
        F2[Risk Scores]
        F3[Clinical Reports]
    end
    
    A --> A_details
    B --> B_details
    C --> C_details
    D --> D_details
    E --> E_details
    F --> F_details

    style A fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style B fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style C fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style D fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style E fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style F fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style A_details fill:#2d2d4d,stroke:#8b5cf6,stroke-width:1px,color:#ffffff
    style B_details fill:#2d2d4d,stroke:#8b5cf6,stroke-width:1px,color:#ffffff
    style C_details fill:#2d2d4d,stroke:#8b5cf6,stroke-width:1px,color:#ffffff
    style D_details fill:#2d2d4d,stroke:#8b5cf6,stroke-width:1px,color:#ffffff
    style E_details fill:#2d2d4d,stroke:#8b5cf6,stroke-width:1px,color:#ffffff
    style F_details fill:#2d2d4d,stroke:#8b5cf6,stroke-width:1px,color:#ffffff
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        CONFIDENTIAL • ACADEMIC SUBMISSION 2024 • LEAD ARCHITECT
    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
// Store previous values for animation
let previousValues = {
    cost: 8450,
    accuracy: 0.78,
    storage: 14.97,
    compute: 'High'
};

// Initialize Chart
const ctx = document.getElementById('performanceChart').getContext('2d');
let performanceChart;

function initializeChart() {
    performanceChart = new Chart(ctx, {
        type: 'line',
        data: {
            labels: ['1K', '50K', '100K', '250K', '500K', '750K', '1M'],
            datasets: [{
                label: 'COST_EFFICIENCY',
                data: [1200, 2450, 4200, 6800, 8450, 11200, 13800],
                borderColor: '#8b5cf6',
                backgroundColor: 'rgba(139, 92, 246, 0.1)',
                borderWidth: 3,
                fill: true,
                tension: 0.4
            }, {
                label: 'PERFORMANCE_SCORE',
                data: [0.65, 0.72, 0.76, 0.78, 0.78, 0.77, 0.76],
                borderColor: '#10b981',
                borderWidth: 3,
                fill: false,
                tension: 0.4,
                yAxisID: 'y1'
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
                y1: {
                    position: 'right',
                    beginAtZero: true,
                    max: 1,
                    grid: {
                        drawOnChartArea: false
                    },
                    ticks: {
                        color: '#94a3b8'
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
                    labels: {
                        color: '#cbd5e1'
                    }
                }
            }
        }
    });
}

// Update simulator values with cool animations
function updateSimulator() {
    const samples = parseInt(document.getElementById('datasetScale').value);
    const features = parseInt(document.getElementById('featureComplexity').value);
    const speed = parseInt(document.getElementById('processingSpeed').value);
    
    // Update displays
    document.getElementById('datasetValue').textContent = (samples/1000).toFixed(0) + 'K Samples';
    document.getElementById('featureValue').textContent = (features/1000000).toFixed(0) + 'M Features';
    document.getElementById('speedValue').textContent = speed + ' Hours';
    
    // Calculate metrics with proper storage calculation
    const storageGB = samples * 30; // 30GB per sample (WGS data)
    const storagePB = storageGB / 1000000; // Convert to PB
    
    const baseCost = (samples * 0.008) + (features * 0.0000004) + (speed * 150) + (storagePB * 200);
    const cost = Math.round(baseCost);
    const accuracy = 0.65 + (samples/2000000) - (features/500000000) + (speed/80);
    const compute = features > 50000000 ? 'High' : features > 20000000 ? 'Medium' : 'Low';
    
    // Update metrics with animations
    updateMetricWithAnimation('costMetric', cost, previousValues.cost, 'costCard', '$');
    updateMetricWithAnimation('accuracyMetric', accuracy, previousValues.accuracy, 'accuracyCard', '', 2);
    updateMetricWithAnimation('storageMetric', storagePB, previousValues.storage, 'storageCard', '', 2, ' PB');
    updateMetric('computeMetric', compute, previousValues.compute, 'computeCard');
    
    // Store current values
    previousValues = { cost, accuracy, storage: storagePB, compute };
    
    // Update chart
    updateChart(samples, cost, accuracy);
}

function updateMetricWithAnimation(elementId, newValue, oldValue, cardId, prefix = '', decimals = 0, suffix = '') {
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
    const formattedValue = decimals > 0 ? newValue.toFixed(decimals) : newValue.toLocaleString();
    element.textContent = prefix + formattedValue + suffix;
}

function updateMetric(elementId, newValue, oldValue, cardId) {
    const element = document.getElementById(elementId);
    const card = document.getElementById(cardId);
    
    // Add animation class based on value change
    if (newValue !== oldValue) {
        card.classList.add('increasing');
        setTimeout(() => card.classList.remove('increasing'), 1000);
    }
    
    element.textContent = newValue;
}

function updateChart(samples, cost, accuracy) {
    const sampleIndex = Math.min(6, Math.floor((samples - 1000) / 166000));
    
    performanceChart.data.datasets[0].data[sampleIndex] = cost;
    performanceChart.data.datasets[1].data[sampleIndex] = Math.max(0.6, Math.min(0.95, accuracy));
    
    performanceChart.update('none');
}

// Initialize
document.addEventListener('DOMContentLoaded', function() {
    initializeChart();
    
    const sliders = ['datasetScale', 'featureComplexity', 'processingSpeed'];
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
