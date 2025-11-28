---
layout: default
title: Genomic Biomarker Discovery Platform
description: Advanced Big Data & ML Pipeline for Whole Genome Sequencing Analysis
---

<style>
:root {
    --primary-purple: #6B46C1;
    --dark-purple: #553C9A;
    --light-purple: #9F7AEA;
    --accent-purple: #805AD5;
    --text-dark: #2D3748;
    --text-light: #718096;
    --background: #FAF5FF;
    --card-bg: #FFFFFF;
    --border-light: #E9D8FD;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    line-height: 1.6;
    color: var(--text-dark);
    background: var(--background);
    min-height: 100vh;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 40px 20px;
}

/* Header Section */
.header {
    text-align: center;
    margin-bottom: 60px;
}

.header h1 {
    font-size: 3.5em;
    font-weight: 700;
    color: var(--dark-purple);
    margin-bottom: 15px;
    letter-spacing: -0.02em;
}

.header .subtitle {
    font-size: 1.4em;
    color: var(--text-light);
    margin-bottom: 30px;
    font-weight: 400;
}

.tagline {
    font-size: 1.1em;
    color: var(--text-light);
    background: var(--card-bg);
    padding: 20px 40px;
    border-radius: 12px;
    display: inline-block;
    border: 1px solid var(--border-light);
    box-shadow: 0 4px 6px rgba(107, 70, 193, 0.1);
}

/* Navigation */
.nav-links {
    display: flex;
    justify-content: center;
    gap: 30px;
    margin-top: 40px;
}

.nav-link {
    color: var(--primary-purple);
    text-decoration: none;
    font-weight: 600;
    padding: 12px 24px;
    border: 2px solid var(--primary-purple);
    border-radius: 8px;
    transition: all 0.3s ease;
}

.nav-link:hover {
    background: var(--primary-purple);
    color: white;
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(107, 70, 193, 0.3);
}

/* Content Sections */
.content-section {
    background: var(--card-bg);
    border-radius: 16px;
    padding: 50px;
    margin: 40px 0;
    border: 1px solid var(--border-light);
    box-shadow: 0 8px 25px rgba(107, 70, 193, 0.08);
}

.section-title {
    color: var(--dark-purple);
    font-size: 2.2em;
    font-weight: 600;
    margin-bottom: 30px;
    text-align: center;
}

/* KPI Grid */
.kpi-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 25px;
    margin: 40px 0;
}

.kpi-card {
    text-align: center;
    padding: 30px 20px;
    background: linear-gradient(135deg, var(--card-bg) 0%, #F8F5FF 100%);
    border-radius: 12px;
    border: 1px solid var(--border-light);
    transition: transform 0.3s ease;
}

.kpi-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 30px rgba(107, 70, 193, 0.15);
}

.kpi-value {
    font-size: 2.8em;
    font-weight: 700;
    color: var(--primary-purple);
    margin-bottom: 8px;
}

.kpi-label {
    color: var(--text-light);
    font-size: 0.95em;
    font-weight: 500;
}

/* Feature Cards */
.feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 30px;
    margin: 40px 0;
}

.feature-card {
    padding: 35px 30px;
    background: var(--card-bg);
    border-radius: 12px;
    border: 1px solid var(--border-light);
    transition: all 0.3s ease;
    position: relative;
}

.feature-card:hover {
    border-color: var(--light-purple);
    box-shadow: 0 8px 25px rgba(107, 70, 193, 0.12);
}

.feature-card h3 {
    color: var(--dark-purple);
    font-size: 1.3em;
    font-weight: 600;
    margin-bottom: 15px;
    display: flex;
    align-items: center;
    gap: 12px;
}

.feature-card p {
    color: var(--text-light);
    line-height: 1.6;
}

/* Pricing Section */
.pricing-controls {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 30px;
    margin-bottom: 40px;
}

.pricing-control {
    background: linear-gradient(135deg, #F8F5FF 0%, #FFFFFF 100%);
    padding: 25px;
    border-radius: 12px;
    border: 1px solid var(--border-light);
}

.pricing-control label {
    display: block;
    color: var(--dark-purple);
    font-weight: 600;
    margin-bottom: 15px;
    font-size: 1.1em;
}

.pricing-control input {
    width: 100%;
    padding: 12px;
    border: 2px solid var(--border-light);
    border-radius: 8px;
    font-size: 1em;
    transition: border-color 0.3s ease;
    background: var(--card-bg);
}

.pricing-control input:focus {
    outline: none;
    border-color: var(--primary-purple);
}

.value-display {
    text-align: center;
    margin-top: 10px;
    font-weight: 600;
    color: var(--primary-purple);
}

.cost-breakdown {
    background: linear-gradient(135deg, #F8F5FF 0%, #FFFFFF 100%);
    padding: 30px;
    border-radius: 12px;
    border: 1px solid var(--border-light);
}

.cost-item {
    display: flex;
    justify-content: space-between;
    padding: 15px 0;
    border-bottom: 1px solid var(--border-light);
    color: var(--text-dark);
}

.cost-item:last-child {
    border-bottom: none;
    font-weight: 700;
    color: var(--dark-purple);
    font-size: 1.1em;
}

.total-cost {
    text-align: center;
    font-size: 1.8em;
    font-weight: 700;
    color: var(--dark-purple);
    margin-bottom: 20px;
}

/* Diagram Section */
.diagram-container {
    background: var(--card-bg);
    padding: 40px;
    border-radius: 12px;
    border: 1px solid var(--border-light);
    margin: 30px 0;
}

/* Methodology */
.methodology-content {
    background: linear-gradient(135deg, #F8F5FF 0%, #FFFFFF 100%);
    padding: 30px;
    border-radius: 12px;
    border: 1px solid var(--border-light);
    margin-top: 25px;
}

.methodology-content h4 {
    color: var(--dark-purple);
    margin-bottom: 20px;
    font-size: 1.3em;
}

.methodology-content ul {
    list-style: none;
    padding: 0;
}

.methodology-content li {
    padding: 12px 0;
    border-bottom: 1px solid var(--border-light);
    color: var(--text-light);
}

.methodology-content li:last-child {
    border-bottom: none;
}

.methodology-content strong {
    color: var(--text-dark);
}

/* Responsive */
@media (max-width: 768px) {
    .container {
        padding: 20px 15px;
    }
    
    .header h1 {
        font-size: 2.5em;
    }
    
    .content-section {
        padding: 30px 20px;
    }
    
    .nav-links {
        flex-direction: column;
        align-items: center;
        gap: 15px;
    }
    
    .feature-grid {
        grid-template-columns: 1fr;
    }
    
    .pricing-controls {
        grid-template-columns: 1fr;
    }
}
</style>

<div class="container">
    <!-- Header Section -->
    <div class="header">
        <h1>Genomic Biomarker Discovery</h1>
        <div class="subtitle">Advanced Big Data & Machine Learning Pipeline</div>
        <div class="tagline">
            Leveraging XGBoost and Distributed Computing to analyze 84M+ genomic features across 500,000 whole genome sequences.
        </div>
        
        <div class="nav-links">
            <a href="#pipeline" class="nav-link">View Pipeline</a>
            <a href="#methodology" class="nav-link">System Design</a>
        </div>
    </div>

    <!-- Business Problem Section -->
    <div class="content-section">
        <h2 class="section-title">Business Problem</h2>
        <div style="text-align: center; color: var(--text-light); font-size: 1.1em; line-height: 1.8;">
            Current genomic analysis methods struggle with the scale of modern whole genome sequencing data. 
            Traditional approaches cannot efficiently process 15+ Petabytes of data or handle 84 million features per sample, 
            limiting our ability to discover meaningful biomarkers and provide personalized risk assessments at scale.
        </div>
        
        <!-- KPI Grid -->
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
                <div class="kpi-label">Target AUPRC</div>
            </div>
        </div>
    </div>

    <!-- Features Section -->
    <div class="content-section">
        <h2 class="section-title">Platform Capabilities</h2>
        <div class="feature-grid">
            <div class="feature-card">
                <h3>🚀 Distributed Processing</h3>
                <p>Apache Spark cluster architecture designed to handle petabyte-scale genomic data with horizontal scaling and fault tolerance.</p>
            </div>
            <div class="feature-card">
                <h3>🧬 Advanced ML</h3>
                <p>XGBoost with GPU acceleration for high-dimensional feature spaces and automated hyperparameter optimization.</p>
            </div>
            <div class="feature-card">
                <h3>💰 Cost Optimization</h3>
                <p>Intelligent cloud resource management with spot instances and auto-scaling to minimize operational costs.</p>
            </div>
            <div class="feature-card">
                <h3>📊 Clinical Insights</h3>
                <p>Comprehensive biomarker discovery and polygenic risk scoring with clinical validation frameworks.</p>
            </div>
        </div>
    </div>

    <!-- Pricing Calculator -->
    <div class="content-section" id="pricing">
        <h2 class="section-title">Infrastructure Cost Analysis</h2>
        <div style="text-align: center; color: var(--text-light); margin-bottom: 30px;">
            Adjust parameters to estimate cloud infrastructure costs for your genomic analysis needs
        </div>
        
        <div class="pricing-controls">
            <div class="pricing-control">
                <label for="sampleCount">Number of Samples</label>
                <input type="range" id="sampleCount" min="1000" max="1000000" value="500000" step="1000">
                <div class="value-display" id="sampleDisplay">500,000 samples</div>
            </div>
            
            <div class="pricing-control">
                <label for="featureCount">Features per Sample</label>
                <input type="range" id="featureCount" min="1000000" max="100000000" value="84000000" step="1000000">
                <div class="value-display" id="featureDisplay">84M features</div>
            </div>
            
            <div class="pricing-control">
                <label for="processingTime">Processing Time (hours)</label>
                <input type="range" id="processingTime" min="1" max="48" value="6" step="1">
                <div class="value-display" id="timeDisplay">6 hours</div>
            </div>
        </div>

        <div class="cost-breakdown">
            <div class="total-cost">Estimated Monthly Cost: <span id="totalCost">$8,450</span></div>
            
            <div class="cost-item">
                <span>Cloud Storage (AWS S3)</span>
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
                <span>Data Transfer & Management</span>
                <span id="otherCost">$250</span>
            </div>
            <div class="cost-item">
                <span>Total Estimated Cost</span>
                <span id="finalCost">$8,450</span>
            </div>
        </div>
    </div>

    <!-- Pipeline Diagram -->
    <div class="content-section" id="pipeline">
        <h2 class="section-title">End-to-End Pipeline Architecture</h2>
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

    style A fill:#6B46C1,stroke:#553C9A,stroke-width:2px,color:#ffffff
    style B fill:#6B46C1,stroke:#553C9A,stroke-width:2px,color:#ffffff
    style C fill:#6B46C1,stroke:#553C9A,stroke-width:2px,color:#ffffff
    style D fill:#6B46C1,stroke:#553C9A,stroke-width:2px,color:#ffffff
    style E fill:#6B46C1,stroke:#553C9A,stroke-width:2px,color:#ffffff
    style F fill:#6B46C1,stroke:#553C9A,stroke-width:2px,color:#ffffff
    style A_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
    style B_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
    style C_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
    style D_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
    style E_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
    style F_details fill:#9F7AEA,stroke:#805AD5,stroke-width:1px,color:#ffffff
            </div>
        </div>
    </div>

    <!-- Methodology Section -->
    <div class="content-section" id="methodology">
        <h2 class="section-title">Machine Learning Methodology</h2>
        <div style="text-align: center; color: var(--text-light); margin-bottom: 25px;">
            Primary Evaluation Metric: Area Under Precision-Recall Curve (AUPRC)
        </div>
        
        <div class="methodology-content">
            <h4>Why AUPRC for Genomic Risk Prediction?</h4>
            <ul>
                <li>
                    <strong>Recall Optimization:</strong> Minimizing false negatives is critical in healthcare - 
                    missing high-risk individuals has significant clinical consequences
                </li>
                <li>
                    <strong>Precision Focus:</strong> Reducing false positives prevents unnecessary patient anxiety 
                    and costly follow-up procedures
                </li>
                <li>
                    <strong>Imbalance Handling:</strong> AUPRC provides meaningful performance assessment 
                    for highly imbalanced datasets common in disease prediction
                </li>
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
    
    // Calculate costs
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
    
    updatePricing();
});
</script>

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>
    mermaid.initialize({ 
        startOnLoad: true,
        theme: 'default',
        securityLevel: 'loose'
    });
</script>
</script>

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>
    mermaid.initialize({ startOnLoad: true });
</script>
