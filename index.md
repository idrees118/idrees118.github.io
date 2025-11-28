---
layout: default
title: Genomic Biomarker Discovery & Personalized Risk Stratification
description: A Big Data & Machine Learning Pipeline for Whole Genome Sequencing Analysis
---

<style>
:root {
    --primary: #1a365d;
    --secondary: #2d3748;
    --accent: #3182ce;
    --success: #38a169;
    --warning: #d69e2e;
    --danger: #e53e3e;
    --light: #f7fafc;
    --dark: #1a202c;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #2d3748;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    margin: 0;
    padding: 0;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

.hero {
    background: rgba(255, 255, 255, 0.95);
    border-radius: 15px;
    padding: 40px;
    margin: 20px 0;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    text-align: center;
}

.hero h1 {
    color: var(--primary);
    font-size: 2.5em;
    margin-bottom: 10px;
}

.hero p {
    font-size: 1.2em;
    color: var(--secondary);
}

.feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
    margin: 30px 0;
}

.feature-card {
    background: white;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
}

.feature-card:hover {
    transform: translateY(-5px);
}

.feature-card h3 {
    color: var(--primary);
    margin-bottom: 15px;
}

.kpi-section {
    background: white;
    border-radius: 15px;
    padding: 30px;
    margin: 30px 0;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.kpi-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    margin-top: 20px;
}

.kpi-card {
    text-align: center;
    padding: 20px;
    background: var(--light);
    border-radius: 10px;
    border-left: 4px solid var(--accent);
}

.kpi-value {
    font-size: 2em;
    font-weight: bold;
    color: var(--primary);
}

.kpi-label {
    color: var(--secondary);
    font-size: 0.9em;
}

.diagram-container {
    background: white;
    border-radius: 15px;
    padding: 30px;
    margin: 30px 0;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    text-align: center;
}

.pipeline-step {
    background: var(--light);
    margin: 15px 0;
    padding: 20px;
    border-radius: 10px;
    border-left: 4px solid var(--accent);
}

.tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 15px;
}

.tech-tag {
    background: var(--accent);
    color: white;
    padding: 5px 15px;
    border-radius: 20px;
    font-size: 0.9em;
}

@media (max-width: 768px) {
    .container {
        padding: 10px;
    }
    
    .hero {
        padding: 20px;
    }
    
    .feature-grid {
        grid-template-columns: 1fr;
    }
}
</style>

<div class="container">
    <!-- Hero Section -->
    <div class="hero">
        <h1>Genomic Biomarker Discovery & Personalized Risk Stratification</h1>
        <p>An End-to-End Big Data & Machine Learning Pipeline for Whole Genome Sequencing Analysis</p>
        <div style="margin-top: 20px;">
            <span class="tech-tag">Apache Spark</span>
            <span class="tech-tag">XGBoost</span>
            <span class="tech-tag">AWS S3</span>
            <span class="tech-tag">Python</span>
            <span class="tech-tag">UK Biobank</span>
        </div>
    </div>

    <!-- Key Features -->
    <div class="feature-grid">
        <div class="feature-card">
            <h3>🚀 Scalable Architecture</h3>
            <p>Process 15+ Petabytes of genomic data using distributed computing with Apache Spark on cloud infrastructure.</p>
        </div>
        <div class="feature-card">
            <h3>🧬 Advanced ML Pipeline</h3>
            <p>Leverage XGBoost with GPU acceleration for handling 84 million features and severe class imbalance.</p>
        </div>
        <div class="feature-card">
            <h3>📊 Clinical Interpretation</h3>
            <p>Generate actionable insights through biomarker discovery and personalized polygenic risk scores.</p>
        </div>
    </div>

    <!-- KPI Section -->
    <div class="kpi-section">
        <h2>Key Performance Indicators</h2>
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

    <!-- Pipeline Diagram -->
    <div class="diagram-container">
        <h2>End-to-End Pipeline Architecture</h2>
        
        <div class="pipeline-step">
            <h3>1. Data Ingestion & Storage</h3>
            <p><strong>UK Biobank → AWS S3 Data Lake</strong></p>
            <div class="tech-stack">
                <span class="tech-tag">VCF/BAM Files</span>
                <span class="tech-tag">AWS S3</span>
                <span class="tech-tag">Parquet Format</span>
            </div>
        </div>

        <div class="pipeline-step">
            <h3>2. Data Processing</h3>
            <p><strong>Quality Control & Variant Calling</strong></p>
            <div class="tech-stack">
                <span class="tech-tag">Apache Spark</span>
                <span class="tech-tag">FastQC</span>
                <span class="tech-tag">GATK</span>
                <span class="tech-tag">Hail</span>
            </div>
        </div>

        <div class="pipeline-step">
            <h3>3. Feature Engineering</h3>
            <p><strong>Variant Filtering & Annotation</strong></p>
            <div class="tech-stack">
                <span class="tech-tag">Spark ML</span>
                <span class="tech-tag">GWAS Pre-filtering</span>
                <span class="tech-tag">Biological Annotation</span>
            </div>
        </div>

        <div class="pipeline-step">
            <h3>4. Machine Learning</h3>
            <p><strong>Model Training & Validation</strong></p>
            <div class="tech-stack">
                <span class="tech-tag">XGBoost</span>
                <span class="tech-tag">GPU Acceleration</span>
                <span class="tech-tag">MLflow</span>
                <span class="tech-tag">Stratified Sampling</span>
            </div>
        </div>

        <div class="pipeline-step">
            <h3>5. Results & Interpretation</h3>
            <p><strong>Biomarker Discovery & Risk Stratification</strong></p>
            <div class="tech-stack">
                <span class="tech-tag">Feature Importance</span>
                <span class="tech-tag">Polygenic Risk Scores</span>
                <span class="tech-tag">Clinical Reports</span>
                <span class="tech-tag">Tableau</span>
            </div>
        </div>
    </div>

    <!-- Methodology Section -->
    <div class="feature-card">
        <h2>📈 Evaluation Methodology</h2>
        <p><strong>Primary Metric: Area Under Precision-Recall Curve (AUPRC)</strong></p>
        <p>Selected for its robustness in handling severe class imbalance common in disease prediction scenarios. Optimizes the critical trade-off between identifying true at-risk individuals (Recall) and minimizing false alarms (Precision).</p>
        
        <div style="background: var(--light); padding: 15px; border-radius: 8px; margin-top: 15px;">
            <h4>Why AUPRC over Accuracy?</h4>
            <ul>
                <li><strong>Recall:</strong> Missing high-risk patients leads to preventable late-stage diseases</li>
                <li><strong>Precision:</strong> False positives cause unnecessary anxiety and healthcare costs</li>
                <li><strong>AUPRC:</strong> Directly optimizes this clinical cost-benefit tradeoff</li>
            </ul>
        </div>
    </div>

    <!-- Footer -->
    <div style="text-align: center; margin-top: 40px; padding: 20px; color: white;">
        <p><strong>Genomic Research Big Data Pipeline</strong> | Advanced Machine Learning for Precision Medicine</p>
        <p>Built with cutting-edge technologies for transformative healthcare insights</p>
    </div>
</div>
