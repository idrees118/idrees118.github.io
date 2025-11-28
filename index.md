---
layout: default
title: Genomic Biomarker Discovery & Personalized Risk Stratification
description: A Big Data & Machine Learning Pipeline for Whole Genome Sequencing Analysis
---

<style>
:root {
    --primary: #1e3a8a;
    --secondary: #3730a3;
    --accent: #6366f1;
    --success: #10b981;
    --warning: #f59e0b;
    --danger: #ef4444;
    --light: #f8fafc;
    --dark: #1e293b;
    --card-bg: rgba(255, 255, 255, 0.95);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    line-height: 1.6;
    color: #334155;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    min-height: 100vh;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

/* Hero Section */
.hero {
    background: var(--card-bg);
    border-radius: 20px;
    padding: 60px 40px;
    margin: 30px 0;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
    text-align: center;
    backdrop-filter: blur(10px);
}

.hero h1 {
    color: var(--primary);
    font-size: 3em;
    font-weight: 700;
    margin-bottom: 15px;
    background: linear-gradient(135deg, var(--primary), var(--accent));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.hero p {
    font-size: 1.3em;
    color: var(--dark);
    margin-bottom: 30px;
    opacity: 0.8;
}

.tech-tags {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 20px;
}

.tech-tag {
    background: var(--accent);
    color: white;
    padding: 8px 20px;
    border-radius: 25px;
    font-size: 0.9em;
    font-weight: 500;
    transition: all 0.3s ease;
}

.tech-tag:hover {
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(99, 102, 241, 0.4);
}

/* Feature Grid */
.feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 25px;
    margin: 40px 0;
}

.feature-card {
    background: var(--card-bg);
    padding: 30px;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
    transition: all 0.3s ease;
    border: 1px solid rgba(255, 255, 255, 0.2);
}

.feature-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

.feature-card h3 {
    color: var(--primary);
    font-size: 1.4em;
    margin-bottom: 15px;
    display: flex;
    align-items: center;
    gap: 10px;
}

.feature-card p {
    color: var(--dark);
    opacity: 0.8;
    line-height: 1.6;
}

/* KPI Section */
.kpi-section {
    background: var(--card-bg);
    border-radius: 20px;
    padding: 40px;
    margin: 40px 0;
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}

.kpi-section h2 {
    color: var(--primary);
    text-align: center;
    margin-bottom: 30px;
    font-size: 2.2em;
}

.kpi-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 25px;
}

.kpi-card {
    text-align: center;
    padding: 25px;
    background: linear-gradient(135deg, var(--light), #ffffff);
    border-radius: 15px;
    border-left: 5px solid var(--accent);
    transition: transform 0.3s ease;
}

.kpi-card:hover {
    transform: scale(1.05);
}

.kpi-value {
    font-size: 2.5em;
    font-weight: 700;
    color: var(--primary);
    margin-bottom: 8px;
}

.kpi-label {
    color: var(--dark);
    font-size: 0.95em;
    opacity: 0.8;
}

/* Pricing Calculator */
.pricing-section {
    background: var(--card-bg);
    border-radius: 20px;
    padding: 40px;
    margin: 40px 0;
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}

.pricing-section h2 {
    color: var(--primary);
    text-align: center;
    margin-bottom: 30px;
    font-size: 2.2em;
}

.pricing-controls {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 25px;
    margin-bottom: 30px;
}

.pricing-control {
    background: var(--light);
    padding: 20px;
    border-radius: 12px;
    border-left: 4px solid var(--success);
}

.pricing-control label {
    display: block;
    color: var(--primary);
    font-weight: 600;
    margin-bottom: 10px;
}

.pricing-control input {
    width: 100%;
    padding: 12px;
    border: 2px solid #e2e8f0;
    border-radius: 8px;
    font-size: 1em;
    transition: border-color 0.3s ease;
}

.pricing-control input:focus {
    outline: none;
    border-color: var(--accent);
}

.cost-breakdown {
    background: var(--light);
    padding: 25px;
    border-radius: 15px;
    margin-top: 20px;
}

.cost-item {
    display: flex;
    justify-content: space-between;
    padding: 12px 0;
    border-bottom: 1px solid #e2e8f0;
}

.cost-item:last-child {
    border-bottom: none;
    font-weight: 700;
    color: var(--primary);
}

/* Diagram Section */
.diagram-section {
    background: var(--card-bg);
    border-radius: 20px;
    padding: 40px;
    margin: 40px 0;
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
    text-align: center;
}

.diagram-section h2 {
    color: var(--primary);
    margin-bottom: 30px;
    font-size: 2.2em;
}

/* Methodology Section */
.methodology-section {
    background: var(--card-bg);
    border-radius: 20px;
    padding: 40px;
    margin: 40px 0;
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}

.methodology-section h2 {
    color: var(--primary);
    margin-bottom: 25px;
    font-size: 2.2em;
}

.metric-explanation {
    background: var(--light);
    padding: 25px;
    border-radius: 12px;
    margin-top: 20px;
    border-left: 4px solid var(--warning);
}

/* Buttons */
.btn-group {
    display: flex;
    gap: 15px;
    justify-content: center;
    margin-top: 30px;
}

.btn {
    padding: 12px 30px;
    border: none;
    border-radius: 25px;
    font-size: 1em;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    text-decoration: none;
    display: inline-block;
}

.btn-primary {
    background: var(--accent);
    color: white;
}

.btn-secondary {
    background: transparent;
    color: var(--accent);
    border: 2px solid var(--accent);
}

.btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(99, 102, 241, 0.3);
}

/* Responsive */
@media (max-width: 768px) {
    .container {
        padding: 15px;
    }
    
    .hero {
        padding: 40px 20px;
    }
    
    .hero h1 {
        font-size: 2.2em;
    }
    
    .feature-grid {
        grid-template-columns: 1fr;
    }
    
    .pricing-controls {
        grid-template-columns: 1fr;
    }
    
    .btn-group {
        flex-direction: column;
        align-items: center;
    }
    
    .btn {
        width: 200px;
        text-align: center;
    }
}
</style>

<div class="container">
    <!-- Hero Section -->
    <div class="hero">
        <h1>Genomic Biomarker Discovery Platform</h1>
        <p>A Big Data & Machine Learning Pipeline for Whole Genome Sequencing Analysis</p>
        <div class="tech-tags">
            <span class="tech-tag">Apache Spark</span>
            <span class="tech-tag">XGBoost</span>
            <span class="tech-tag">AWS S3</span>
            <span class="tech-tag">Python</span>
            <span class="tech-tag">UK Biobank</span>
            <span class="tech-tag">GPU Computing</span>
        </div>
        <div class="btn-group">
            <a href="#pipeline" class="btn btn-primary">View Pipeline</a>
            <a href="#methodology" class="btn btn-secondary">Methodology</a>
        </div>
    </div>

    <!-- KPI Section -->
    <div class="kpi-section">
        <h2>Platform Scale & Performance</h2>
        <div class="kpi-grid">
            <div class="kpi-card">
                <div class="kpi-value">500K</div>
                <div class="kpi-label">Whole Genome Sequences</div>
            </div>
            <div class="kpi-card">
                <div class="kpi-value">84M</div>
                <div class="kpi-label">Features per Sample</div>
            </div>
            <div class="kpi-card">
                <div class="kpi-value">15+ PB</div>
                <div class="kpi-label">Raw Data Volume</div>
            </div>
            <div class="kpi-card">
                <div class="kpi-value">> 0.7</div>
                <div class="kpi-label">Target AUPRC Score</div>
            </div>
        </div>
    </div>

    <!-- Feature Grid -->
    <div class="feature-grid">
        <div class="feature-card">
            <h3>🚀 Scalable Architecture</h3>
            <p>Process 15+ Petabytes of genomic data using distributed computing with Apache Spark on cloud infrastructure with dynamic resource allocation.</p>
        </div>
        <div class="feature-card">
            <h3>🧬 Advanced ML Pipeline</h3>
            <p>Leverage XGBoost with GPU acceleration for handling 84 million features and severe class imbalance with automated hyperparameter tuning.</p>
        </div>
        <div class="feature-card">
            <h3>💰 Cost Optimization</h3>
            <p>Intelligent resource management with spot instances and auto-scaling to minimize cloud costs while maintaining performance SLAs.</p>
        </div>
        <div class="feature-card">
            <h3>📊 Clinical Interpretation</h3>
            <p>Generate actionable insights through biomarker discovery and personalized polygenic risk scores with clinical validation frameworks.</p>
        </div>
    </div>

    <!-- Pricing Calculator -->
    <div class="pricing-section" id="pricing">
        <h2>Cloud Cost Estimation</h2>
        <p style="text-align: center; margin-bottom: 30px; opacity: 0.8;">Adjust parameters to see real-time cost impact</p>
        
        <div class="pricing-controls">
            <div class="pricing-control">
                <label for="sampleCount">Number of Samples</label>
                <input type="range" id="sampleCount" min="1000" max="1000000" value="500000" step="1000">
                <div style="text-align: center; margin-top: 8px; font-weight: 600;" id="sampleDisplay">500,000 samples</div>
            </div>
            
            <div class="pricing-control">
                <label for="featureCount">Features per Sample</label>
                <input type="range" id="featureCount" min="1000000" max="100000000" value="84000000" step="1000000">
                <div style="text-align: center; margin-top: 8px; font-weight: 600;" id="featureDisplay">84M features</div>
            </div>
            
            <div class="pricing-control">
                <label for="processingTime">Processing Speed</label>
                <input type="range" id="processingTime" min="1" max="48" value="6" step="1">
                <div style="text-align: center; margin-top: 8px; font-weight: 600;" id="timeDisplay">6 hours</div>
            </div>
        </div>

        <div class="cost-breakdown">
            <h3 style="color: var(--primary); margin-bottom: 20px;">Estimated Monthly Cost: <span id="totalCost">$8,450</span></h3>
            
            <div class="cost-item">
                <span>Storage (S3)</span>
                <span id="storageCost">$3,200</span>
            </div>
            <div class="cost-item">
                <span>Compute (Spark Cluster)</span>
                <span id="computeCost">$4,150</span>
            </div>
            <div class="cost-item">
                <span>ML Training (GPU Instances)</span>
                <span id="mlCost">$850</span>
            </div>
            <div class="cost-item">
                <span>Data Transfer & Other</span>
                <span id="otherCost">$250</span>
            </div>
            <div class="cost-item">
                <span><strong>Total Estimated Cost</strong></span>
                <span><strong id="finalCost">$8,450</strong></span>
            </div>
        </div>
    </div>

    <!-- Pipeline Diagram -->
    <div class="diagram-section" id="pipeline">
        <h2>End-to-End Pipeline Architecture</h2>
        
        ```mermaid
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

            style A fill:#1e3a8a,stroke:#1e40af,stroke-width:2px,color:#ffffff
            style B fill:#7e22ce,stroke:#9333ea,stroke-width:2px,color:#ffffff
            style C fill:#0f766e,stroke:#0d9488,stroke-width:2px,color:#ffffff
            style D fill:#b45309,stroke:#d97706,stroke-width:2px,color:#ffffff
            style E fill:#be123c,stroke:#e11d48,stroke-width:2px,color:#ffffff
            style F fill:#047857,stroke:#059669,stroke-width:2px,color:#ffffff
            style A_details fill:#1e3a8a,stroke:#1e40af,stroke-width:1px,color:#ffffff
            style B_details fill:#7e22ce,stroke:#9333ea,stroke-width:1px,color:#ffffff
            style C_details fill:#0f766e,stroke:#0d9488,stroke-width:1px,color:#ffffff
            style D_details fill:#b45309,stroke:#d97706,stroke-width:1px,color:#ffffff
            style E_details fill:#be123c,stroke:#e11d48,stroke-width:1px,color:#ffffff
            style F_details fill:#047857,stroke:#059669,stroke-width:1px,color:#ffffff
        ```
    </div>

    <!-- Methodology Section -->
    <div class="methodology-section" id="methodology">
        <h2>Evaluation Methodology</h2>
        <p><strong>Primary Metric: Area Under Precision-Recall Curve (AUPRC)</strong></p>
        <p>Selected for its robustness in handling severe class imbalance common in disease prediction scenarios. Optimizes the critical trade-off between identifying true at-risk individuals (Recall) and minimizing false alarms (Precision).</p>
        
        <div class="metric-explanation">
            <h4>📊 Why AUPRC over Accuracy?</h4>
            <ul style="list-style: none; padding: 0;">
                <li style="padding: 8px 0; border-bottom: 1px solid #e2e8f0;">🎯 <strong>Recall:</strong> Missing high-risk patients leads to preventable late-stage diseases</li>
                <li style="padding: 8px 0; border-bottom: 1px solid #e2e8f0;">💰 <strong>Precision:</strong> False positives cause unnecessary anxiety and healthcare costs</li>
                <li style="padding: 8px 0;">🚀 <strong>AUPRC:</strong> Directly optimizes this clinical cost-benefit tradeoff</li>
            </ul>
        </div>
    </div>
</div>

<script>
// Pricing Calculator Functionality
function updatePricing() {
    const samples = parseInt(document.getElementById('sampleCount').value);
    const features = parseInt(document.getElementById('featureCount').value);
    const time = parseInt(document.getElementById('processingTime').value);
    
    // Update displays
    document.getElementById('sampleDisplay').textContent = samples.toLocaleString() + ' samples';
    document.getElementById('featureDisplay').textContent = (features / 1000000).toFixed(0) + 'M features';
    document.getElementById('timeDisplay').textContent = time + ' hours';
    
    // Calculate costs (simplified model)
    const storageCost = Math.round((samples * 0.0064) + (features * 0.00000038));
    const computeCost = Math.round((samples * 0.0083) + (time * 692));
    const mlCost = Math.round((samples * 0.0017) + (features * 0.0000001) + (time * 142));
    const otherCost = 250;
    
    const totalCost = storageCost + computeCost + mlCost + otherCost;
    
    // Update cost displays
    document.getElementById('storageCost').textContent = '$' + storageCost.toLocaleString();
    document.getElementById('computeCost').textContent = '$' + computeCost.toLocaleString();
    document.getElementById('mlCost').textContent = '$' + mlCost.toLocaleString();
    document.getElementById('otherCost').textContent = '$' + otherCost.toLocaleString();
    document.getElementById('finalCost').textContent = '$' + totalCost.toLocaleString();
    document.getElementById('totalCost').textContent = '$' + totalCost.toLocaleString();
}

// Initialize event listeners
document.addEventListener('DOMContentLoaded', function() {
    const sliders = ['sampleCount', 'featureCount', 'processingTime'];
    sliders.forEach(sliderId => {
        document.getElementById(sliderId).addEventListener('input', updatePricing);
    });
    
    // Initial calculation
    updatePricing();
});
</script>
