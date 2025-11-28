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
    --accent-teal: #0BC5EA;
    --accent-green: #38A169;
    --accent-orange: #DD6B20;
    --accent-pink: #D53F8C;
    --gradient-bg: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    --gradient-card: linear-gradient(135deg, #FFFFFF 0%, #F7FAFC 100%);
    --gradient-accent: linear-gradient(135deg, #6B46C1 0%, #9F7AEA 100%);
    --text-dark: #2D3748;
    --text-light: #718096;
    --border-light: #E2E8F0;
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
    background: var(--gradient-bg);
    min-height: 100vh;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 30px 20px;
}

/* Header Section */
.header {
    text-align: center;
    margin-bottom: 50px;
    background: rgba(255, 255, 255, 0.95);
    padding: 50px 40px;
    border-radius: 20px;
    box-shadow: 0 20px 40px rgba(107, 70, 193, 0.15);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.2);
}

.header h1 {
    font-size: 3.2em;
    font-weight: 800;
    background: var(--gradient-accent);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 15px;
    letter-spacing: -0.02em;
}

.header .subtitle {
    font-size: 1.3em;
    color: var(--text-light);
    margin-bottom: 25px;
    font-weight: 400;
}

.tagline {
    font-size: 1.1em;
    color: var(--text-light);
    background: var(--gradient-card);
    padding: 20px 35px;
    border-radius: 15px;
    display: inline-block;
    border: 1px solid var(--border-light);
    box-shadow: 0 8px 25px rgba(107, 70, 193, 0.1);
}

/* Navigation */
.nav-links {
    display: flex;
    justify-content: center;
    gap: 25px;
    margin-top: 35px;
}

.nav-link {
    color: var(--primary-purple);
    text-decoration: none;
    font-weight: 600;
    padding: 14px 32px;
    background: var(--gradient-card);
    border: 2px solid var(--primary-purple);
    border-radius: 12px;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba(107, 70, 193, 0.2);
}

.nav-link:hover {
    background: var(--gradient-accent);
    color: white;
    transform: translateY(-3px);
    box-shadow: 0 12px 30px rgba(107, 70, 193, 0.4);
}

/* Content Sections */
.content-section {
    background: var(--gradient-card);
    border-radius: 20px;
    padding: 45px;
    margin: 35px 0;
    border: 1px solid var(--border-light);
    box-shadow: 0 15px 35px rgba(107, 70, 193, 0.12);
    position: relative;
    overflow: hidden;
}

.content-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: var(--gradient-accent);
}

.section-title {
    color: var(--dark-purple);
    font-size: 2.4em;
    font-weight: 700;
    margin-bottom: 35px;
    text-align: center;
    position: relative;
}

.section-title::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 80px;
    height: 4px;
    background: var(--gradient-accent);
    border-radius: 2px;
}

/* KPI Grid */
.kpi-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 25px;
    margin: 40px 0;
}

.kpi-card {
    text-align: center;
    padding: 35px 25px;
    background: var(--gradient-card);
    border-radius: 16px;
    border: 2px solid;
    border-image: var(--gradient-accent) 1;
    transition: all 0.4s ease;
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
    background: var(--gradient-accent);
}

.kpi-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 40px rgba(107, 70, 193, 0.25);
}

.kpi-value {
    font-size: 3em;
    font-weight: 800;
    background: var(--gradient-accent);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 10px;
}

.kpi-label {
    color: var(--text-light);
    font-size: 1em;
    font-weight: 600;
}

/* Feature Cards */
.feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(360px, 1fr));
    gap: 30px;
    margin: 45px 0;
}

.feature-card {
    padding: 40px 30px;
    background: var(--gradient-card);
    border-radius: 16px;
    border: 2px solid var(--border-light);
    transition: all 0.4s ease;
    position: relative;
    overflow: hidden;
}

.feature-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: var(--gradient-accent);
}

.feature-card:hover {
    border-color: var(--light-purple);
    transform: translateY(-8px);
    box-shadow: 0 20px 40px rgba(107, 70, 193, 0.2);
}

.feature-card h3 {
    color: var(--dark-purple);
    font-size: 1.4em;
    font-weight: 700;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 15px;
}

.feature-card p {
    color: var(--text-light);
    line-height: 1.7;
    font-size: 1.05em;
}

/* Pricing Section */
.pricing-section {
    background: var(--gradient-card);
    border-radius: 20px;
    padding: 45px;
    margin: 40px 0;
    border: 1px solid var(--border-light);
    box-shadow: 0 15px 35px rgba(107, 70, 193, 0.12);
}

.pricing-controls {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    margin-bottom: 45px;
}

.pricing-control {
    background: rgba(255, 255, 255, 0.8);
    padding: 30px;
    border-radius: 16px;
    border: 2px solid var(--border-light);
    transition: all 0.3s ease;
    backdrop-filter: blur(10px);
}

.pricing-control:hover {
    border-color: var(--light-purple);
    box-shadow: 0 10px 25px rgba(107, 70, 193, 0.15);
}

.pricing-control label {
    display: block;
    color: var(--dark-purple);
    font-weight: 700;
    margin-bottom: 20px;
    font-size: 1.2em;
}

.pricing-control input {
    width: 100%;
    padding: 15px;
    border: 2px solid var(--border-light);
    border-radius: 10px;
    font-size: 1.1em;
    transition: all 0.3s ease;
    background: white;
}

.pricing-control input:focus {
    outline: none;
    border-color: var(--primary-purple);
    box-shadow: 0 0 0 3px rgba(107, 70, 193, 0.1);
}

.value-display {
    text-align: center;
    margin-top: 15px;
    font-weight: 700;
    color: var(--primary-purple);
    font-size: 1.1em;
}

/* Live Diagram */
.live-diagram {
    background: white;
    padding: 40px;
    border-radius: 16px;
    border: 2px solid var(--border-light);
    margin: 35px 0;
    text-align: center;
}

.diagram-container {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 300px;
    margin: 25px 0;
}

.diagram-node {
    background: var(--gradient-accent);
    color: white;
    padding: 20px 30px;
    border-radius: 12px;
    margin: 15px;
    font-weight: 600;
    box-shadow: 0 8px 25px rgba(107, 70, 193, 0.3);
    transition: all 0.3s ease;
    position: relative;
}

.diagram-node::after {
    content: '→';
    position: absolute;
    right: -25px;
    top: 50%;
    transform: translateY(-50%);
    color: var(--primary-purple);
    font-size: 1.5em;
    font-weight: bold;
}

.diagram-node:last-child::after {
    display: none;
}

.diagram-node.active {
    background: var(--accent-teal);
    transform: scale(1.05);
}

.cost-breakdown {
    background: rgba(255, 255, 255, 0.9);
    padding: 35px;
    border-radius: 16px;
    border: 2px solid var(--border-light);
    margin-top: 30px;
    backdrop-filter: blur(10px);
}

.total-cost {
    text-align: center;
    font-size: 2.2em;
    font-weight: 800;
    background: var(--gradient-accent);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 25px;
}

.cost-item {
    display: flex;
    justify-content: space-between;
    padding: 18px 0;
    border-bottom: 2px solid var(--border-light);
    color: var(--text-dark);
    font-size: 1.1em;
    transition: all 0.3s ease;
}

.cost-item:hover {
    background: rgba(107, 70, 193, 0.05);
    padding-left: 15px;
    padding-right: 15px;
    margin: 0 -15px;
    border-radius: 8px;
}

.cost-item:last-child {
    border-bottom: none;
    font-weight: 800;
    color: var(--dark-purple);
    font-size: 1.2em;
    background: rgba(107, 70, 193, 0.1);
    padding: 20px 15px;
    margin: 10px -15px -10px -15px;
    border-radius: 12px;
}

/* Methodology */
.methodology-content {
    background: rgba(255, 255, 255, 0.9);
    padding: 35px;
    border-radius: 16px;
    border: 2px solid var(--border-light);
    margin-top: 30px;
    backdrop-filter: blur(10px);
}

.methodology-content h4 {
    color: var(--dark-purple);
    margin-bottom: 25px;
    font-size: 1.4em;
    font-weight: 700;
}

.methodology-content ul {
    list-style: none;
    padding: 0;
}

.methodology-content li {
    padding: 18px 0;
    border-bottom: 2px solid var(--border-light);
    color: var(--text-light);
    font-size: 1.1em;
    transition: all 0.3s ease;
}

.methodology-content li:hover {
    background: rgba(107, 70, 193, 0.05);
    padding-left: 20px;
    border-radius: 8px;
}

.methodology-content li:last-child {
    border-bottom: none;
}

.methodology-content strong {
    color: var(--text-dark);
    font-weight: 700;
}

/* Responsive */
@media (max-width: 768px) {
    .container {
        padding: 20px 15px;
    }
    
    .header {
        padding: 35px 25px;
    }
    
    .header h1 {
        font-size: 2.4em;
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
    
    .diagram-node {
        padding: 15px 20px;
        font-size: 0.9em;
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
        <h2 class="section-title">Business Challenge</h2>
        <div style="text-align: center; color: var(--text-light); font-size: 1.15em; line-height: 1.8; padding: 0 20px;">
            Traditional genomic analysis collapses under the weight of modern sequencing data. Our platform revolutionizes 
            how we process 15+ Petabytes and 84 million features per sample, enabling breakthrough discoveries in 
            personalized medicine and disease prevention.
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
                <div class="kpi-label">Target AUPRC Score</div>
            </div>
        </div>
    </div>

    <!-- Features Section -->
    <div class="content-section">
        <h2 class="section-title">Platform Capabilities</h2>
        <div class="feature-grid">
            <div class="feature-card">
                <h3>🚀 Distributed Architecture</h3>
                <p>Apache Spark cluster with auto-scaling capabilities designed specifically for genomic data processing at petabyte scale with real-time monitoring.</p>
            </div>
            <div class="feature-card">
                <h3>🧬 Machine Learning Core</h3>
                <p>XGBoost with GPU acceleration, automated hyperparameter tuning, and feature importance analysis for high-dimensional genomic data.</p>
            </div>
            <div class="feature-card">
                <h3>💰 Smart Cost Management</h3>
                <p>Intelligent cloud resource allocation with spot instances, auto-scaling policies, and cost optimization algorithms.</p>
            </div>
            <div class="feature-card">
                <h3>📊 Clinical Intelligence</h3>
                <p>Comprehensive biomarker discovery, polygenic risk scoring, and clinical validation frameworks with interpretable AI.</p>
            </div>
        </div>
    </div>

    <!-- Pricing Calculator with Live Diagram -->
    <div class="content-section" id="pricing">
        <h2 class="section-title">Infrastructure Cost Analysis</h2>
        <div style="text-align: center; color: var(--text-light); margin-bottom: 35px; font-size: 1.1em;">
            Adjust your genomic analysis requirements and see real-time cost impact across the pipeline
        </div>
        
        <div class="pricing-controls">
            <div class="pricing-control">
                <label for="sampleCount">📊 Number of Samples</label>
                <input type="range" id="sampleCount" min="1000" max="1000000" value="500000" step="1000">
                <div class="value-display" id="sampleDisplay">500,000 samples</div>
            </div>
            
            <div class="pricing-control">
                <label for="featureCount">🧬 Features per Sample</label>
                <input type="range" id="featureCount" min="1000000" max="100000000" value="84000000" step="1000000">
                <div class="value-display" id="featureDisplay">84M features</div>
            </div>
            
            <div class="pricing-control">
                <label for="processingTime">⏱️ Processing Time (hours)</label>
                <input type="range" id="processingTime" min="1" max="48" value="6" step="1">
                <div class="value-display" id="timeDisplay">6 hours</div>
            </div>
        </div>

        <!-- Live Diagram -->
        <div class="live-diagram">
            <h3 style="color: var(--dark-purple); margin-bottom: 25px; font-size: 1.4em;">Live Pipeline Impact</h3>
            <div class="diagram-container">
                <div class="diagram-node" id="node-storage">Storage<br><small id="storage-size">15 PB</small></div>
                <div class="diagram-node" id="node-compute">Compute<br><small id="compute-scale">Large Cluster</small></div>
                <div class="diagram-node" id="node-ml">ML Training<br><small id="ml-complexity">High</small></div>
                <div class="diagram-node" id="node-results">Results<br><small id="result-scale">Enterprise</small></div>
            </div>
        </div>

        <div class="cost-breakdown">
            <div class="total-cost">Estimated Monthly Cost: <span id="totalCost">$8,450</span></div>
            
            <div class="cost-item">
                <span>🏢 Cloud Storage (AWS S3)</span>
                <span id="storageCost">$3,200</span>
            </div>
            <div class="cost-item">
                <span>⚡ Compute (Spark Cluster)</span>
                <span id="computeCost">$4,150</span>
            </div>
            <div class="cost-item">
                <span>🤖 ML Training (GPU Instances)</span>
                <span id="mlCost">$850</span>
            </div>
            <div class="cost-item">
                <span>🔗 Data Transfer & Management</span>
                <span id="otherCost">$250</span>
            </div>
            <div class="cost-item">
                <span>💰 Total Estimated Cost</span>
                <span id="finalCost">$8,450</span>
            </div>
        </div>
    </div>

    <!-- Pipeline Diagram -->
    <div class="content-section" id="pipeline">
        <h2 class="section-title">End-to-End Pipeline Architecture</h2>
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

    <!-- Methodology Section -->
    <div class="content-section" id="methodology">
        <h2 class="section-title">Machine Learning Methodology</h2>
        <div style="text-align: center; color: var(--text-light); margin-bottom: 30px; font-size: 1.1em;">
            Primary Evaluation Metric: Area Under Precision-Recall Curve (AUPRC)
        </div>
        
        <div class="methodology-content">
            <h4>Why AUPRC for Genomic Risk Prediction?</h4>
            <ul>
                <li>
                    <strong>🎯 Recall Optimization:</strong> Minimizing false negatives is critical in healthcare - 
                    missing high-risk individuals has significant clinical consequences and impacts patient outcomes
                </li>
                <li>
                    <strong>💰 Precision Focus:</strong> Reducing false positives prevents unnecessary patient anxiety, 
                    costly follow-up procedures, and optimizes healthcare resource allocation
                </li>
                <li>
                    <strong>⚡ Imbalance Handling:</strong> AUPRC provides meaningful performance assessment 
                    for highly imbalanced datasets common in rare disease prediction and genomic studies
                </li>
            </ul>
        </div>
    </div>
</div>

<script>
// Pricing Calculator with Live Diagram Updates
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
    
    // Update Live Diagram
    updateLiveDiagram(samples, features, time, totalCost);
}

function updateLiveDiagram(samples, features, time, totalCost) {
    // Storage node
    const storageSize = (samples * 0.03).toFixed(1) + ' PB';
    document.getElementById('storage-size').textContent = storageSize;
    
    // Compute node
    let computeScale = 'Small Cluster';
    if (samples > 750000) computeScale = 'Large Cluster';
    else if (samples > 250000) computeScale = 'Medium Cluster';
    document.getElementById('compute-scale').textContent = computeScale;
    
    // ML Training node
    let mlComplexity = 'Low';
    if (features > 60000000) mlComplexity = 'High';
    else if (features > 30000000) mlComplexity = 'Medium';
    document.getElementById('ml-complexity').textContent = mlComplexity;
    
    // Results node
    let resultScale = 'Basic';
    if (totalCost > 10000) resultScale = 'Enterprise';
    else if (totalCost > 5000) resultScale = 'Advanced';
    document.getElementById('result-scale').textContent = resultScale;
    
    // Add active states based on changes
    const nodes = ['node-storage', 'node-compute', 'node-ml', 'node-results'];
    nodes.forEach(node => document.getElementById(node).classList.remove('active'));
    
    // Determine which node to highlight based on biggest change
    if (samples > 750000) document.getElementById('node-storage').classList.add('active');
    if (features > 60000000) document.getElementById('node-ml').classList.add('active');
    if (totalCost > 10000) document.getElementById('node-results').classList.add('active');
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
