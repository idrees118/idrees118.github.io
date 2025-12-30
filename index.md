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

/* Data tiers */
.storage-tier {
    display: flex;
    justify-content: space-between;
    margin: 10px 0;
    padding: 10px;
    background: rgba(255,255,255,0.05);
    border-radius: 8px;
}

.tier-label {
    font-weight: 600;
    color: var(--text-secondary);
}

.tier-value {
    color: var(--accent-green);
    font-weight: 600;
}

.tier-cost {
    color: var(--accent-orange);
    font-weight: 600;
}
</style>

<div class="container">
    <!-- Header -->
    <div class="header">
        <h1>Genomic Biomarker Discovery Platform</h1>
        <div class="subtitle">Enterprise Data Lakehouse Architecture</div>
        <div class="tagline">
            Modern Parquet-based pipeline with intelligent tiered storage
        </div>
        
        <div class="nav-links">
            <a href="#simulator" class="nav-link">Cost Simulator</a>
            <a href="#pipeline" class="nav-link">View Architecture</a>
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
                    <div class="kpi-label">VARIANT FEATURES</div>
                </div>
                <div class="kpi-card">
                    <div class="kpi-value" id="liveStorage">0.4 PB</div>
                    <div class="kpi-label">HOT STORAGE (S3)</div>
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
                    <div class="chart-title">Storage Tier Breakdown</div>
                    <canvas id="storageChart" class="chart-canvas"></canvas>
                </div>
            </div>
        </div>

        <!-- Simulator Section -->
        <div class="simulator-section" id="simulator">
            <h2 class="simulator-title">Genomic Analysis Cost Simulator</h2>
            <div class="tagline" style="margin-bottom: 25px; font-size: 0.9em; padding: 12px 20px;">
                Based on real-world AWS genomics architecture with Parquet compression & spot instances
            </div>
            
            <div class="pricing-controls">
                <div class="pricing-control">
                    <label for="sampleCount">WGS Samples</label>
                    <input type="range" id="sampleCount" min="10000" max="2000000" value="500000" step="10000">
                    <div class="value-display" id="sampleDisplay">500,000 samples</div>
                </div>
                
                <div class="pricing-control">
                    <label for="featureCount">Genomic Variants per Sample</label>
                    <input type="range" id="featureCount" min="1000000" max="200000000" value="84000000" step="1000000">
                    <div class="value-display" id="featureDisplay">84 million variants</div>
                </div>
                
                <div class="pricing-control">
                    <label for="analysisDepth">Analysis Complexity</label>
                    <input type="range" id="analysisDepth" min="1" max="3" value="2" step="1">
                    <div class="value-display" id="depthDisplay">Comprehensive</div>
                </div>
            </div>

            <!-- Storage Tiers -->
            <div style="background: rgba(139, 92, 246, 0.1); padding: 20px; border-radius: 12px; margin-bottom: 20px; border: 1px solid rgba(139, 92, 246, 0.3);">
                <h3 style="color: var(--accent-purple); margin-bottom: 15px; text-align: center;">Storage Tier Architecture</h3>
                <div class="storage-tier">
                    <span class="tier-label">Hot Storage (S3 Standard):</span>
                    <span class="tier-value" id="hotStorage">400 TB</span>
                    <span class="tier-cost" id="hotStorageCost">$9,200</span>
                </div>
                <div class="storage-tier">
                    <span class="tier-label">Cold Storage (Glacier Deep Archive):</span>
                    <span class="tier-value" id="coldStorage">15.0 PB</span>
                    <span class="tier-cost" id="coldStorageCost">$15,000</span>
                </div>
                <div class="storage-tier" style="border-top: 1px solid rgba(255,255,255,0.1); padding-top: 15px;">
                    <span class="tier-label">Total Storage:</span>
                    <span class="tier-value" id="totalStorage">15.4 PB</span>
                    <span class="tier-cost" id="totalStorageCost">$24,200</span>
                </div>
            </div>

            <div class="cost-breakdown">
                <div class="total-cost">Total Monthly Cost: <span id="totalCost">$60,920</span></div>
                
                <div class="cost-item">
                    <span>Hot Storage (Analytical Data)</span>
                    <span id="storageCost">$9,200</span>
                </div>
                <div class="cost-item">
                    <span>Cold Storage (Raw CRAMs)</span>
                    <span id="coldStorageCostLine">$15,000</span>
                </div>
                <div class="cost-item">
                    <span>ETL Processing (Spark on Spot)</span>
                    <span id="computeCost">$15,000</span>
                </div>
                <div class="cost-item">
                    <span>ML Training (GPU Cluster)</span>
                    <span id="mlCost">$36,720</span>
                </div>
                <div class="cost-item">
                    <span>Data Transfer & Management</span>
                    <span id="otherCost">$1,000</span>
                </div>
                <div class="cost-item">
                    <span>Total Estimated Monthly Cost</span>
                    <span id="finalCost">$60,920</span>
                </div>
            </div>
        </div>

        <!-- Features Section -->
        <div class="features-section" id="features">
            <h2 class="features-title">Modern Genomics Architecture</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <h3>🏗️ Data Lakehouse Architecture</h3>
                    <p>Parquet/Delta Lake storage with 10-20× compression vs VCF. Only analytical data in hot storage, raw data in Glacier.</p>
                </div>
                <div class="feature-card">
                    <h3>💰 Intelligent Cost Optimization</h3>
                    <p>Spot instances for 60-70% compute savings. Tiered storage reduces costs by 90% vs keeping everything in S3 Standard.</p>
                </div>
                <div class="feature-card">
                    <h3>🚀 Distributed ML Training</h3>
                    <p>XGBoost on Dask/RAPIDS across GPU clusters. Scales to 42 trillion data points (500K samples × 84M variants).</p>
                </div>
                <div class="feature-card">
                    <h3>🔬 Production Genomics Pipeline</h3>
                    <p>Based on UK Biobank scale. Real-world benchmarks: $0.03/sample ETL, $0.8 GB/sample analytical storage.</p>
                </div>
            </div>
        </div>

        <!-- Pipeline Section -->
        <div class="pipeline-section" id="pipeline">
            <h2 class="pipeline-title">Modern Genomics Data Flow</h2>
            <div class="diagram-container">
                <div class="mermaid">
graph TD
    A[UK Biobank: 500K WGS Samples] --> B[Raw CRAM Files: 15 PB]
    B --> C[Glacier Deep Archive<br/>$0.00099/GB]
    C --> D[Variant Calling<br/>GATK/Sentieon]
    D --> E[Analytical Dataset<br/>400 TB Parquet]
    E --> F[S3 Standard Storage<br/>$0.023/GB]
    F --> G[Apache Spark ETL<br/>Spot Instances]
    G --> H[Distributed ML Training<br/>20× GPU Cluster]
    H --> I[Biomarker Discovery<br/>XGBoost/RAPIDS]
    
    style A fill:#1a1a1a,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style B fill:#1a1a1a,stroke:#3b82f6,stroke-width:2px,color:#ffffff
    style C fill:#1a1a1a,stroke:#10b981,stroke-width:2px,color:#ffffff
    style D fill:#1a1a1a,stroke:#f59e0b,stroke-width:2px,color:#ffffff
    style E fill:#1a1a1a,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
    style F fill:#1a1a1a,stroke:#3b82f6,stroke-width:2px,color:#ffffff
    style G fill:#1a1a1a,stroke:#10b981,stroke-width:2px,color:#ffffff
    style H fill:#1a1a1a,stroke:#f59e0b,stroke-width:2px,color:#ffffff
    style I fill:#1a1a1a,stroke:#8b5cf6,stroke-width:2px,color:#ffffff
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        CONFIDENTIAL • ACADEMIC SUBMISSION 2024 • ENTERPRISE GENOMICS ARCHITECTURE
    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
// Real-world constants based on industry benchmarks
const GENOMICS_CONSTANTS = {
    // Storage: Parquet compressed analytical data (0.8 GB/sample)
    analyticalGBPerSample: 0.8,
    s3StandardPerGB: 0.023,      // AWS S3 Standard
    
    // Raw data: CRAM compressed (30 GB/sample)
    rawGBPerSample: 30,
    glacierPerGB: 0.00099,       // AWS Glacier Deep Archive
    
    // Compute: ETL processing on spot instances
    computeCostPerSample: 0.03,   // $0.03 per sample for Spark ETL
    
    // ML Training: Distributed GPU cluster
    // Base cost for 500K samples, 84M features
    mlBaseCost: 36720,
    mlSamplesReference: 500000,
    mlFeaturesReference: 84000000,
    
    // Analysis depth multipliers
    depthMultipliers: {
        storage: [0.8, 1.0, 1.2],     // Basic, Comprehensive, Advanced
        compute: [0.7, 1.0, 1.4],
        ml: [0.6, 1.0, 1.5]
    }
};

// Initialize Charts
let costChart, storageChart;

function initializeCharts() {
    // Cost Distribution Chart
    const costCtx = document.getElementById('costChart').getContext('2d');
    costChart = new Chart(costCtx, {
        type: 'doughnut',
        data: {
            labels: ['Hot Storage', 'Cold Storage', 'ETL Processing', 'ML Training'],
            datasets: [{
                data: [9200, 15000, 15000, 36720],
                backgroundColor: [
                    '#8b5cf6',   // Hot storage
                    '#3b82f6',   // Cold storage
                    '#10b981',   // ETL
                    '#f59e0b'    // ML
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
                        font: { size: 12 }
                    }
                },
                tooltip: {
                    callbacks: {
                        label: function(context) {
                            return `${context.label}: $${context.parsed.toLocaleString()}`;
                        }
                    }
                }
            }
        }
    });

    // Storage Tier Chart
    const storageCtx = document.getElementById('storageChart').getContext('2d');
    storageChart = new Chart(storageCtx, {
        type: 'bar',
        data: {
            labels: ['Hot Storage', 'Cold Storage'],
            datasets: [{
                label: 'Capacity',
                data: [400, 15000],  // TB vs PB, scaled for visual comparison
                backgroundColor: ['#8b5cf6', '#3b82f6'],
                borderColor: ['#7c3aed', '#2563eb'],
                borderWidth: 2,
                yAxisID: 'y'
            }, {
                label: 'Cost ($)',
                data: [9200, 15000],
                backgroundColor: 'rgba(16, 185, 129, 0.3)',
                borderColor: '#10b981',
                borderWidth: 2,
                type: 'line',
                yAxisID: 'y1'
            }]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            scales: {
                y: {
                    type: 'logarithmic',
                    position: 'left',
                    title: {
                        display: true,
                        text: 'Storage (TB)',
                        color: '#d1d5db'
                    },
                    grid: { color: 'rgba(255,255,255,0.1)' },
                    ticks: { color: '#9ca3af' }
                },
                y1: {
                    type: 'linear',
                    position: 'right',
                    title: {
                        display: true,
                        text: 'Monthly Cost ($)',
                        color: '#d1d5db'
                    },
                    grid: { drawOnChartArea: false },
                    ticks: { 
                        color: '#9ca3af',
                        callback: value => '$' + value.toLocaleString()
                    }
                },
                x: {
                    grid: { color: 'rgba(255,255,255,0.1)' },
                    ticks: { color: '#9ca3af' }
                }
            },
            plugins: {
                legend: {
                    labels: { color: '#d1d5db' }
                },
                tooltip: {
                    callbacks: {
                        label: function(context) {
                            if (context.dataset.label === 'Capacity') {
                                const value = context.parsed.y;
                                const unit = context.dataIndex === 0 ? 'TB' : 'PB';
                                return `${context.dataset.label}: ${value.toLocaleString()} ${unit}`;
                            } else {
                                return `${context.dataset.label}: $${context.parsed.y.toLocaleString()}`;
                            }
                        }
                    }
                }
            }
        }
    });
}

// Calculate storage with proper tiering
function calculateRealisticStorage(samples, depth) {
    const depthMultiplier = GENOMICS_CONSTANTS.depthMultipliers.storage[depth - 1];
    
    // Hot storage: Analytical data in Parquet
    const analyticalGB = samples * GENOMICS_CONSTANTS.analyticalGBPerSample * depthMultiplier;
    const hotStorageTB = analyticalGB / 1000;
    const hotStoragePB = hotStorageTB / 1000;
    const hotStorageCost = analyticalGB * GENOMICS_CONSTANTS.s3StandardPerGB;
    
    // Cold storage: Raw CRAMs in Glacier
    const rawGB = samples * GENOMICS_CONSTANTS.rawGBPerSample * depthMultiplier;
    const coldStoragePB = rawGB / 1000000;  // GB to PB
    const coldStorageCost = rawGB * GENOMICS_CONSTANTS.glacierPerGB;
    
    return {
        hotStorage: {
            tb: hotStorageTB,
            pb: hotStoragePB,
            cost: hotStorageCost
        },
        coldStorage: {
            pb: coldStoragePB,
            cost: coldStorageCost
        },
        totalPB: hotStoragePB + coldStoragePB,
        totalCost: hotStorageCost + coldStorageCost
    };
}

// Update simulator with accurate calculations
function updateSimulator() {
    const samples = parseInt(document.getElementById('sampleCount').value);
    const features = parseInt(document.getElementById('featureCount').value);
    const depth = parseInt(document.getElementById('analysisDepth').value);
    
    // Update displays
    document.getElementById('sampleDisplay').textContent = samples.toLocaleString() + ' samples';
    const featuresM = (features / 1000000).toFixed(0);
    document.getElementById('featureDisplay').textContent = featuresM + ' million variants';
    
    const depthLabels = ['Basic (SNVs only)', 'Comprehensive (Indels+SVs)', 'Advanced (Full omics)'];
    document.getElementById('depthDisplay').textContent = depthLabels[depth - 1];
    
    // Calculate storage with tiering
    const storage = calculateRealisticStorage(samples, depth);
    
    // Calculate compute costs
    const depthComputeMultiplier = GENOMICS_CONSTANTS.depthMultipliers.compute[depth - 1];
    const computeCost = samples * GENOMICS_CONSTANTS.computeCostPerSample * depthComputeMultiplier;
    
    // Calculate ML training costs (scales with samples × features × depth)
    const depthMLMultiplier = GENOMICS_CONSTANTS.depthMultipliers.ml[depth - 1];
    const samplesScale = samples / GENOMICS_CONSTANTS.mlSamplesReference;
    const featuresScale = features / GENOMICS_CONSTANTS.mlFeaturesReference;
    const mlCost = GENOMICS_CONSTANTS.mlBaseCost * samplesScale * featuresScale * depthMLMultiplier;
    
    // Data transfer & management (scales with data volume)
    const otherCost = storage.totalCost * 0.05;  // 5% for data management
    
    const totalCost = Math.round(
        storage.totalCost + computeCost + mlCost + otherCost
    );
    
    // Update KPI cards
    document.getElementById('liveSamples').textContent = (samples/1000).toFixed(0) + 'K';
    document.getElementById('liveFeatures').textContent = featuresM + 'M';
    document.getElementById('liveStorage').textContent = storage.hotStorage.pb.toFixed(2) + ' PB';
    
    // Calculate accuracy (realistic model performance)
    const baseAccuracy = 0.75;
    const sampleEffect = Math.min(0.1, Math.log10(samples / 10000) * 0.03);
    const featureEffect = Math.min(0.05, Math.log10(features / 1000000) * 0.01);
    const depthEffect = (depth - 1) * 0.025;
    const accuracy = Math.min(0.95, baseAccuracy + sampleEffect + featureEffect + depthEffect);
    document.getElementById('liveAccuracy').textContent = accuracy.toFixed(2);
    
    // Update storage tier displays
    document.getElementById('hotStorage').textContent = storage.hotStorage.tb.toFixed(0) + ' TB';
    document.getElementById('hotStorageCost').textContent = '$' + Math.round(storage.hotStorage.cost).toLocaleString();
    document.getElementById('coldStorage').textContent = storage.coldStorage.pb.toFixed(1) + ' PB';
    document.getElementById('coldStorageCost').textContent = '$' + Math.round(storage.coldStorage.cost).toLocaleString();
    document.getElementById('totalStorage').textContent = (storage.hotStorage.pb + storage.coldStorage.pb).toFixed(1) + ' PB';
    document.getElementById('totalStorageCost').textContent = '$' + Math.round(storage.totalCost).toLocaleString();
    
    // Update cost breakdown
    document.getElementById('storageCost').textContent = '$' + Math.round(storage.hotStorage.cost).toLocaleString();
    document.getElementById('coldStorageCostLine').textContent = '$' + Math.round(storage.coldStorage.cost).toLocaleString();
    document.getElementById('computeCost').textContent = '$' + Math.round(computeCost).toLocaleString();
    document.getElementById('mlCost').textContent = '$' + Math.round(mlCost).toLocaleString();
    document.getElementById('otherCost').textContent = '$' + Math.round(otherCost).toLocaleString();
    document.getElementById('finalCost').textContent = '$' + totalCost.toLocaleString();
    document.getElementById('totalCost').textContent = '$' + totalCost.toLocaleString();
    
    // Update charts
    updateCharts(storage, computeCost, mlCost, otherCost, samples);
}

function updateCharts(storage, computeCost, mlCost, otherCost, samples) {
    // Update cost chart
    costChart.data.datasets[0].data = [
        Math.round(storage.hotStorage.cost),
        Math.round(storage.coldStorage.cost),
        Math.round(computeCost),
        Math.round(mlCost)
    ];
    costChart.update();
    
    // Update storage chart
    storageChart.data.datasets[0].data[0] = storage.hotStorage.tb;  // Hot in TB
    storageChart.data.datasets[0].data[1] = storage.coldStorage.pb * 1000;  // Cold in TB equivalent
    storageChart.data.datasets[1].data[0] = Math.round(storage.hotStorage.cost);
    storageChart.data.datasets[1].data[1] = Math.round(storage.coldStorage.cost);
    storageChart.update();
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
        securityLevel: 'loose',
        flowchart: {
            useMaxWidth: true,
            htmlLabels: true
        }
    });
</script>
