---
layout: default
title: Genomic Biomarker Discovery
description: Advanced Big Data & ML Pipeline for Whole Genome Sequencing Analysis
---

<style>
:root {
    --dark-bg: #0a0a0a;
    --darker-bg: #000000;
    --card-bg: #1a1a1a;
    --card-border: #333333;
    --accent-purple: #8b5cf6;
    --accent-blue: #3b82f6;
    --accent-green: #10b981;
    --accent-orange: #f59e0b;
    --accent-red: #ef4444;
    --accent-pink: #ec4899;
    --text-primary: #ffffff;
    --text-secondary: #d1d5db;
    --text-muted: #9ca3af;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    line-height: 1.6;
    color: var(--text-primary);
    background: var(--dark-bg);
    min-height: 100vh;
}

.container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 20px;
}

/* Header Section */
.header {
    background: linear-gradient(135deg, var(--accent-purple), var(--accent-blue));
    border-radius: 20px;
    padding: 50px 40px;
    margin-bottom: 30px;
    text-align: center;
    position: relative;
    overflow: hidden;
}

.header::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="0.5"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
}

.header h1 {
    font-size: 3.2em;
    font-weight: 800;
    color: white;
    margin-bottom: 15px;
    position: relative;
}

.header .subtitle {
    font-size: 1.3em;
    color: rgba(255, 255, 255, 0.9);
    margin-bottom: 25px;
    font-weight: 400;
    position: relative;
}

.tagline {
    background: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(10px);
    padding: 18px 35px;
    border-radius: 12px;
    color: white;
    display: inline-block;
    font-size: 1.1em;
    border: 1px solid rgba(255, 255, 255, 0.2);
    position: relative;
}

/* Navigation */
.nav-links {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 30px;
    position: relative;
}

.nav-link {
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    color: white;
    padding: 12px 28px;
    border-radius: 10px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    border: 1px solid rgba(255, 255, 255, 0.2);
}

.nav-link:hover {
    background: white;
    color: var(--accent-purple);
    transform: translateY(-3px);
    box-shadow: 0 10px 25px rgba(139, 92, 246, 0.4);
}

/* Dashboard Grid */
.dashboard-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 25px;
    margin-bottom: 30px;
}

/* KPI Section */
.kpi-section {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 16px;
    padding: 30px;
    grid-column: 1 / -1;
}

.kpi-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
    margin-bottom: 30px;
}

.kpi-card {
    background: linear-gradient(135deg, #2d2d2d, #1a1a1a);
    border: 1px solid var(--card-border);
    border-radius: 12px;
    padding: 25px 20px;
    text-align: center;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
}

.kpi-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
}

.kpi-card:nth-child(1)::before { background: var(--accent-purple); }
.kpi-card:nth-child(2)::before { background: var(--accent-blue); }
.kpi-card:nth-child(3)::before { background: var(--accent-green); }
.kpi-card:nth-child(4)::before { background: var(--accent-orange); }

.kpi-card:hover {
    transform: translateY(-5px);
    border-color: var(--accent-purple);
}

.kpi-value {
    font-size: 2.5em;
    font-weight: 800;
    margin-bottom: 8px;
}

.kpi-card:nth-child(1) .kpi-value { color: var(--accent-purple); }
.kpi-card:nth-child(2) .kpi-value { color: var(--accent-blue); }
.kpi-card:nth-child(3) .kpi-value { color: var(--accent-green); }
.kpi-card:nth-child(4) .kpi-value { color: var(--accent-orange); }

.kpi-label {
    color: var(--text-muted);
    font-size: 0.95em;
    font-weight: 500;
}

/* Charts Grid */
.charts-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 25px;
}

.chart-container {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 12px;
    padding: 25px;
    height: 300px;
}

.chart-title {
    color: var(--text-primary);
    font-size: 1.2em;
    font-weight: 600;
    margin-bottom: 20px;
    text-align: center;
}

.chart-canvas {
    width: 100%;
    height: calc(100% - 40px);
}

/* Simulator Section */
.simulator-section {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 16px;
    padding: 30px;
    grid-column: 1 / -1;
}

.simulator-title {
    color: var(--text-primary);
    font-size: 1.8em;
    font-weight: 700;
    margin-bottom: 25px;
    text-align: center;
}

.pricing-controls {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 25px;
    margin-bottom: 30px;
}

.pricing-control {
    background: linear-gradient(135deg, #2d2d2d, #1a1a1a);
    padding: 25px;
    border-radius: 12px;
    border: 1px solid var(--card-border);
}

.pricing-control label {
    display: block;
    color: var(--text-primary);
    font-weight: 600;
    margin-bottom: 15px;
    font-size: 1.1em;
}

.pricing-control input {
    width: 100%;
    padding: 12px;
    border: 2px solid var(--card-border);
    border-radius: 8px;
    font-size: 1em;
    transition: all 0.3s ease;
    background: var(--darker-bg);
    color: var(--text-primary);
}

.pricing-control input:focus {
    outline: none;
    border-color: var(--accent-purple);
}

.value-display {
    text-align: center;
    margin-top: 12px;
    font-weight: 600;
    color: var(--accent-green);
    font-size: 1.1em;
}

.cost-breakdown {
    background: linear-gradient(135deg, #2d2d2d, #1a1a1a);
    padding: 30px;
    border-radius: 12px;
    border: 1px solid var(--card-border);
    margin-top: 25px;
}

.total-cost {
    text-align: center;
    font-size: 2em;
    font-weight: 800;
    color: var(--accent-purple);
    margin-bottom: 25px;
}

.cost-item {
    display: flex;
    justify-content: space-between;
    padding: 15px 0;
    border-bottom: 1px solid var(--card-border);
    color: var(--text-secondary);
}

.cost-item:last-child {
    border-bottom: none;
    font-weight: 700;
    color: var(--text-primary);
    font-size: 1.1em;
    padding-top: 20px;
}

/* Features Grid */
.features-section {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 16px;
    padding: 30px;
    grid-column: 1 / -1;
    margin-top: 25px;
}

.features-title {
    color: var(--text-primary);
    font-size: 1.8em;
    font-weight: 700;
    margin-bottom: 30px;
    text-align: center;
}

.feature-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 25px;
}

.feature-card {
    background: linear-gradient(135deg, #2d2d2d, #1a1a1a);
    padding: 30px 25px;
    border-radius: 12px;
    border: 1px solid var(--card-border);
    transition: all 0.3s ease;
}

.feature-card:hover {
    transform: translateY(-5px);
    border-color: var(--accent-purple);
}

.feature-card h3 {
    color: var(--text-primary);
    font-size: 1.3em;
    font-weight: 600;
    margin-bottom: 15px;
    display: flex;
    align-items: center;
    gap: 12px;
}

.feature-card p {
    color: var(--text-muted);
    line-height: 1.6;
}

/* Pipeline Section */
.pipeline-section {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 16px;
    padding: 30px;
    grid-column: 1 / -1;
    margin-top: 25px;
}

.pipeline-title {
    color: var(--text-primary);
    font-size: 1.8em;
    font-weight: 700;
    margin-bottom: 25px;
    text-align: center;
}

.diagram-container {
    background: var(--darker-bg);
    padding: 30px;
    border-radius: 12px;
    border: 1px solid var(--card-border);
}

/* Footer */
.footer {
    text-align: center;
    color: var(--text-muted);
    font-size: 0.9em;
    margin-top: 50px;
    padding: 25px;
    border-top: 1px solid var(--card-border);
}

/* Responsive */
@media (max-width: 1024px) {
    .dashboard-grid {
        grid-template-columns: 1fr;
    }
    
    .kpi-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    
    .charts-grid {
        grid-template-columns: 1fr;
    }
    
    .pricing-controls {
        grid-template-columns: 1fr;
    }
    
    .feature-grid {
        grid-template-columns: 1fr;
    }
    
    .header h1 {
        font-size: 2.5em;
    }
}

@media (max-width: 768px) {
    .container {
        padding: 15px;
    }
    
    .kpi-grid {
        grid-template-columns: 1fr;
    }
    
    .nav-links {
        flex-direction: column;
        align-items: center;
    }
}
</style>

<div class="container">
    <!-- Header -->
    <div class="header">
        <h1>Genomic Biomarker Discovery Platform</h1>
        <div class="subtitle">Advanced Big Data & Machine Learning Pipeline</div>
        <div class="tagline">
            Leveraging XGBoost and Distributed Computing to analyze 84M+ genomic features
        </div>
        
        <div class="nav-links">
            <a href="#simulator" class="nav-link">Launch Simulator</a>
            <a href="#pipeline" class="nav-link">View Pipeline</a>
            <a href="#features" class="nav-link">Platform Features</a>
        </div>
    </div>

    <!-- KPI Dashboard -->
    <div class="dashboard-grid">
        <div class="kpi-section">
            <div class="kpi-grid">
                <div class="kpi-card">
                    <div class="kpi-value" id="liveSamples">500K</div>
                    <div class="kpi-label">WHOLE GENOME SEQUENCES</div>
                </div>
                <div class="kpi-card">
                    <div class="kpi-value" id="liveFeatures">84M</div>
                    <div class="kpi-label">FEATURES PER SAMPLE</div>
                </div>
                <div class="kpi-card">
                    <div class="kpi-value" id="liveStorage">76.0 PB</div>
                    <div class="kpi-label">STORAGE REQUIRED</div>
                </div>
                <div class="kpi-card">
                    <div class="kpi-value" id="liveAccuracy">0.82</div>
                    <div class="kpi-label">AUPRC SCORE</div>
                </div>
            </div>

            <!-- Live Charts -->
            <div class="charts-grid">
                <div class="chart-container">
                    <div class="chart-title">Cost Distribution</div>
                    <canvas id="costChart" class="chart-canvas"></canvas>
                </div>
                <div class="chart-container">
                    <div class="chart-title">Performance vs Scale</div>
                    <canvas id="performanceChart" class="chart-canvas"></canvas>
                </div>
            </div>
        </div>

        <!-- Simulator Section -->
        <div class="simulator-section" id="simulator">
            <h2 class="simulator-title">Genomic Analysis Simulator</h2>
            
            <div class="pricing-controls">
                <div class="pricing-control">
                    <label for="sampleCount">WGS Samples</label>
                    <input type="range" id="sampleCount" min="1000" max="1000000" value="500000" step="1000">
                    <div class="value-display" id="sampleDisplay">500,000 samples</div>
                </div>
                
                <div class="pricing-control">
                    <label for="featureCount">Genomic Variants</label>
                    <input type="range" id="featureCount" min="1000000" max="100000000" value="84000000" step="1000000">
                    <div class="value-display" id="featureDisplay">84M variants</div>
                </div>
                
                <div class="pricing-control">
                    <label for="analysisDepth">Analysis Depth</label>
                    <input type="range" id="analysisDepth" min="1" max="3" value="2" step="1">
                    <div class="value-display" id="depthDisplay">Comprehensive</div>
                </div>
            </div>

            <div class="cost-breakdown">
                <div class="total-cost">Estimated Monthly Cost: <span id="totalCost">$18,240</span></div>
                
                <div class="cost-item">
                    <span>Cloud Storage (76.0 PB)</span>
                    <span id="storageCost">$7,600</span>
                </div>
                <div class="cost-item">
                    <span>Compute (Spark Cluster)</span>
                    <span id="computeCost">$6,840</span>
                </div>
                <div class="cost-item">
                    <span>ML Training (GPU Instances)</span>
                    <span id="mlCost">$2,850</span>
                </div>
                <div class="cost-item">
                    <span>Data Transfer & Management</span>
                    <span id="otherCost">$950</span>
                </div>
                <div class="cost-item">
                    <span>Total Estimated Cost</span>
                    <span id="finalCost">$18,240</span>
                </div>
            </div>
        </div>

        <!-- Features Section -->
        <div class="features-section" id="features">
            <h2 class="features-title">Platform Capabilities</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <h3>🚀 Distributed Architecture</h3>
                    <p>Apache Spark cluster with auto-scaling for petabyte-scale genomic data processing and real-time monitoring.</p>
                </div>
                <div class="feature-card">
                    <h3>🧬 Machine Learning Core</h3>
                    <p>XGBoost with GPU acceleration, automated hyperparameter tuning, and feature importance analysis.</p>
                </div>
                <div class="feature-card">
                    <h3>💰 Smart Cost Management</h3>
                    <p>Intelligent cloud resource allocation with spot instances and cost optimization algorithms.</p>
                </div>
                <div class="feature-card">
                    <h3>📊 Clinical Intelligence</h3>
                    <p>Comprehensive biomarker discovery, polygenic risk scoring, and clinical validation frameworks.</p>
                </div>
            </div>
        </div>

        <!-- Pipeline Section -->
        <div class="pipeline-section" id="pipeline">
            <h2 class="pipeline-title">Genomic Analysis Pipeline</h2>
            <div class="diagram-container">
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

    style A fill:#1a1a1a,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style B fill:#1a1a1a,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style C fill:#1a1a1a,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style D fill:#1a1a1a,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style E fill:#1a1a1a,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style F fill:#1a1a1a,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style A_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
    style B_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
    style C_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
    style D_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
    style E_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
    style F_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        CONFIDENTIAL • ACADEMIC SUBMISSION 2024 • LEAD DATA ARCHITECT
    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
// Initialize Charts
let costChart, performanceChart;

function initializeCharts() {
    // Cost Distribution Chart
    const costCtx = document.getElementById('costChart').getContext('2d');
    costChart = new Chart(costCtx, {
        type: 'doughnut',
        data: {
            labels: ['Storage', 'Compute', 'ML Training', 'Data Transfer'],
            datasets: [{
                data: [7600, 6840, 2850, 950],
                backgroundColor: [
                    '#8b5cf6',
                    '#3b82f6',
                    '#10b981',
                    '#f59e0b'
                ],
                borderColor: '#1a1a1a',
                borderWidth: 3
            }]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    position: 'bottom',
                    labels: {
                        color: '#d1d5db',
                        font: {
                            size: 12
                        }
                    }
                },
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

    // Performance vs Scale Chart
    const perfCtx = document.getElementById('performanceChart').getContext('2d');
    performanceChart = new Chart(perfCtx, {
        type: 'line',
        data: {
            labels: ['100K', '250K', '500K', '750K', '1M'],
            datasets: [{
                label: 'AUPRC Score',
                data: [0.75, 0.78, 0.82, 0.81, 0.80],
                borderColor: '#8b5cf6',
                backgroundColor: 'rgba(139, 92, 246, 0.1)',
                borderWidth: 3,
                fill: true,
                tension: 0.4
            }, {
                label: 'Cost ($K)',
                data: [8.2, 12.4, 18.2, 23.8, 29.5],
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
                    beginAtZero: false,
                    min: 0.7,
                    max: 0.85,
                    grid: {
                        color: 'rgba(255,255,255,0.1)'
                    },
                    ticks: {
                        color: '#9ca3af'
                    },
                    title: {
                        display: true,
                        text: 'AUPRC Score',
                        color: '#d1d5db'
                    }
                },
                y1: {
                    position: 'right',
                    beginAtZero: true,
                    grid: {
                        drawOnChartArea: false
                    },
                    ticks: {
                        color: '#9ca3af',
                        callback: function(value) {
                            return '$' + value + 'K';
                        }
                    },
                    title: {
                        display: true,
                        text: 'Monthly Cost',
                        color: '#d1d5db'
                    }
                },
                x: {
                    grid: {
                        color: 'rgba(255,255,255,0.1)'
                    },
                    ticks: {
                        color: '#9ca3af'
                    }
                }
            },
            plugins: {
                legend: {
                    labels: {
                        color: '#d1d5db'
                    }
                }
            }
        }
    });
}

// Precise storage calculation
function calculateStorage(samples, analysisDepth) {
    const rawFastqPerSample = 150;  // GB per sample
    const bamFilesPerSample = 80;   // GB per sample
    const vcfFilesPerSample = 3;    // GB per sample
    const processedDataPerSample = 10; // GB per sample
    
    let totalStorageGB = samples * (rawFastqPerSample + bamFilesPerSample + vcfFilesPerSample + processedDataPerSample);
    return totalStorageGB / 1000000; // Convert to PB
}

// Update simulator and charts
function updateSimulator() {
    const samples = parseInt(document.getElementById('sampleCount').value);
    const features = parseInt(document.getElementById('featureCount').value);
    const depth = parseInt(document.getElementById('analysisDepth').value);
    
    // Update displays
    document.getElementById('sampleDisplay').textContent = samples.toLocaleString() + ' samples';
    document.getElementById('featureDisplay').textContent = (features / 1000000).toFixed(0) + 'M variants';
    
    const depthLabels = ['Basic', 'Comprehensive', 'Advanced'];
    document.getElementById('depthDisplay').textContent = depthLabels[depth - 1];
    
    // Calculate metrics
    const storagePB = calculateStorage(samples, depth);
    const storageCost = storagePB * 100;
    const computeCost = (samples * 0.012) + (features * 0.0000002);
    const mlCost = (samples * 0.004) + (features * 0.0000001);
    const dataTransferCost = storagePB * 12.5;
    
    const totalCost = Math.round(storageCost + computeCost + mlCost + dataTransferCost);
    const accuracy = 0.75 + (samples/2000000) - (features/500000000) + (depth * 0.035);
    
    // Update KPI cards
    document.getElementById('liveSamples').textContent = (samples/1000).toFixed(0) + 'K';
    document.getElementById('liveFeatures').textContent = (features/1000000).toFixed(0) + 'M';
    document.getElementById('liveStorage').textContent = storagePB.toFixed(1) + ' PB';
    document.getElementById('liveAccuracy').textContent = Math.max(0.7, Math.min(0.85, accuracy)).toFixed(2);
    
    // Update cost breakdown
    document.getElementById('storageCost').textContent = '$' + Math.round(storageCost).toLocaleString();
    document.getElementById('computeCost').textContent = '$' + Math.round(computeCost).toLocaleString();
    document.getElementById('mlCost').textContent = '$' + Math.round(mlCost).toLocaleString();
    document.getElementById('otherCost').textContent = '$' + Math.round(dataTransferCost).toLocaleString();
    document.getElementById('finalCost').textContent = '$' + totalCost.toLocaleString();
    document.getElementById('totalCost').textContent = '$' + totalCost.toLocaleString();
    
    // Update charts
    updateCharts(samples, totalCost, accuracy, storageCost, computeCost, mlCost, dataTransferCost);
}

function updateCharts(samples, totalCost, accuracy, storageCost, computeCost, mlCost, dataTransferCost) {
    // Update cost chart
    costChart.data.datasets[0].data = [
        Math.round(storageCost),
        Math.round(computeCost),
        Math.round(mlCost),
        Math.round(dataTransferCost)
    ];
    costChart.update();
    
    // Update performance chart based on sample size
    const sampleIndex = Math.min(4, Math.floor((samples - 100000) / 225000));
    performanceChart.data.datasets[0].data[sampleIndex] = Math.max(0.7, Math.min(0.85, accuracy));
    performanceChart.data.datasets[1].data[sampleIndex] = totalCost / 1000;
    performanceChart.update();
}

// Initialize
document.addEventListener('DOMContentLoaded', function() {
    initializeCharts();
    
    const sliders = ['sampleCount', 'featureCount', 'analysisDepth'];
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
