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
    justify-content: between;
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
}

input[type="range"] {
    width: 100%;
    height: 6px;
    background: var(--card-border);
    border-radius: 3px;
    outline: none;
}

input[type="range"]::-webkit-slider-thumb {
    appearance: none;
    width: 20px;
    height: 20px;
    background: var(--accent-purple);
    border-radius: 50%;
    cursor: pointer;
    box-shadow: 0 2px 10px rgba(139, 92, 246, 0.4);
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
}

.metric-value {
    font-size: 1.8em;
    font-weight: 700;
    color: var(--accent-green);
    margin-bottom: 5px;
}

.metric-label {
    color: var(--text-muted);
    font-size: 0.9em;
}

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

/* Responsive */
@media (max-width: 1024px) {
    .main-grid {
        grid-template-columns: 1fr;
    }
    
    .container {
        padding: 15px;
    }
}

/* Chart Animation */
@keyframes pulse {
    0% { opacity: 0.4; }
    50% { opacity: 1; }
    100% { opacity: 0.4; }
}

.loading {
    animation: pulse 2s infinite;
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
                <div class="metric-card">
                    <div class="metric-value" id="costMetric">$8,450</div>
                    <div class="metric-label">MONTHLY_COST</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value" id="accuracyMetric">0.78</div>
                    <div class="metric-label">AUPRC_SCORE</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value" id="storageMetric">15 PB</div>
                    <div class="metric-label">STORAGE_NEEDED</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value" id="computeMetric">High</div>
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
    A[RAW_GENOMIC_DATA] --> B[CLOUD_STORAGE_S3]
    B --> C[DISTRIBUTED_PROCESSING]
    C --> D[FEATURE_ENGINEERING]
    D --> E[ML_TRAINING_XGBOOST]
    E --> F[BIOMARKER_DISCOVERY]
    
    style A fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style B fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style C fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style D fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style E fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style F fill:#1a1a2e,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        CONFIDENTIAL • ACADEMIC SUBMISSION 2024 • LEAD ARCHITECT
    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
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

// Update simulator values
function updateSimulator() {
    const samples = parseInt(document.getElementById('datasetScale').value);
    const features = parseInt(document.getElementById('featureComplexity').value);
    const speed = parseInt(document.getElementById('processingSpeed').value);
    
    // Update displays
    document.getElementById('datasetValue').textContent = (samples/1000).toFixed(0) + 'K Samples';
    document.getElementById('featureValue').textContent = (features/1000000).toFixed(0) + 'M Features';
    document.getElementById('speedValue').textContent = speed + ' Hours';
    
    // Calculate metrics
    const baseCost = (samples * 0.008) + (features * 0.0000004) + (speed * 150);
    const cost = Math.round(baseCost * 1.2);
    const accuracy = 0.65 + (samples/2000000) - (features/500000000) + (speed/80);
    const storage = (samples * 0.03).toFixed(1);
    const compute = features > 50000000 ? 'High' : features > 20000000 ? 'Medium' : 'Low';
    
    // Update metrics
    document.getElementById('costMetric').textContent = '$' + cost.toLocaleString();
    document.getElementById('accuracyMetric').textContent = Math.max(0.6, Math.min(0.95, accuracy)).toFixed(2);
    document.getElementById('storageMetric').textContent = storage + ' PB';
    document.getElementById('computeMetric').textContent = compute;
    
    // Update chart
    updateChart(samples, cost, accuracy);
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
