---
layout: default
title: "🧬 Genomic Research Pipeline"
description: "Cloud-Native High-Throughput Genomic Analysis"
---

<!-- Modern CSS Framework -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<style>
:root {
  --primary: #6366f1;
  --primary-dark: #4f46e5;
  --secondary: #10b981;
  --accent: #f59e0b;
  --dark: #1f2937;
  --light: #f8fafc;
}

.hero-section {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 4rem 0;
  position: relative;
  overflow: hidden;
}

.hero-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><polygon fill="rgba(255,255,255,0.05)" points="0,1000 1000,0 1000,1000"/></svg>');
}

.hero-content {
  position: relative;
  z-index: 2;
}

.glass-card {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 16px;
  padding: 2rem;
}

.metric-card {
  background: white;
  border-radius: 12px;
  padding: 1.5rem;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  border-left: 4px solid var(--primary);
  transition: all 0.3s ease;
  height: 100%;
}

.metric-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
}

.architecture-layer {
  background: linear-gradient(135deg, var(--primary), var(--primary-dark));
  color: white;
  border-radius: 12px;
  padding: 2rem;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.architecture-layer::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(255, 255, 255, 0.1);
}

.phase-section {
  background: var(--light);
  border-radius: 12px;
  padding: 2rem;
  margin: 2rem 0;
  border-left: 4px solid var(--secondary);
}

.code-block {
  background: #1a1b26;
  color: #c0caf5;
  border-radius: 8px;
  padding: 1.5rem;
  font-family: 'Monaco', 'Menlo', 'Ubuntu Mono', monospace;
  font-size: 0.9rem;
}

.badge-modern {
  background: var(--primary);
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
}
</style>

<div class="hero-section">
  <div class="container">
    <div class="row align-items-center">
      <div class="col-lg-8">
        <div class="hero-content">
          <h1 class="display-4 fw-bold mb-3">🧬🌐 Genomic Research Pipeline</h1>
          <p class="lead mb-4">Cloud-Native High-Throughput Platform for Large-Scale Disease Risk Prediction</p>
          <div class="d-flex flex-wrap gap-2 mb-4">
            <span class="badge-modern"><i class="fas fa-check-circle me-1"></i> Production Ready</span>
            <span class="badge-modern" style="background: var(--secondary);"><i class="fas fa-code-branch me-1"></i> v2.1.0</span>
            <span class="badge-modern" style="background: var(--accent);"><i class="fas fa-dollar-sign me-1"></i> $2.5K-$4K/Run</span>
            <span class="badge-modern" style="background: #ef4444;"><i class="fas fa-chart-line me-1"></i> 0.87 PR-AUC</span>
          </div>
          <div class="glass-card">
            <p class="mb-0"><strong>84 Million Variants</strong> processed across <strong>2,504 samples</strong> from the 1000 Genomes Project</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="container my-5">
  
  <!-- Executive Dashboard -->
  <section class="mb-5">
    <h2 class="text-center mb-4">📊 Live Performance Dashboard</h2>
    <div class="row g-4">
      <div class="col-md-3">
        <div class="metric-card">
          <div class="text-primary mb-2"><i class="fas fa-rocket fa-2x"></i></div>
          <h3 class="h4">1.2 TB/Hour</h3>
          <p class="text-muted">Data Processing Speed</p>
          <div class="progress" style="height: 8px;">
            <div class="progress-bar bg-primary" style="width: 85%"></div>
          </div>
          <small class="text-success"><i class="fas fa-arrow-up"></i> +20% Above Target</small>
        </div>
      </div>
      <div class="col-md-3">
        <div class="metric-card">
          <div class="text-success mb-2"><i class="fas fa-dollar-sign fa-2x"></i></div>
          <h3 class="h4">$2,800</h3>
          <p class="text-muted">Cost per Run</p>
          <div class="progress" style="height: 8px;">
            <div class="progress-bar bg-success" style="width: 78%"></div>
          </div>
          <small class="text-success"><i class="fas fa-arrow-down"></i> 7% Under Budget</small>
        </div>
      </div>
      <div class="col-md-3">
        <div class="metric-card">
          <div class="text-warning mb-2"><i class="fas fa-bullseye fa-2x"></i></div>
          <h3 class="h4">0.87 PR-AUC</h3>
          <p class="text-muted">Model Performance</p>
          <div class="progress" style="height: 8px;">
            <div class="progress-bar bg-warning" style="width: 87%"></div>
          </div>
          <small class="text-success"><i class="fas fa-arrow-up"></i> Target Exceeded</small>
        </div>
      </div>
      <div class="col-md-3">
        <div class="metric-card">
          <div class="text-info mb-2"><i class="fas fa-bolt fa-2x"></i></div>
          <h3 class="h4">14.5 Hours</h3>
          <p class="text-muted">Processing Time</p>
          <div class="progress" style="height: 8px;">
            <div class="progress-bar bg-info" style="width: 65%"></div>
          </div>
          <small class="text-success"><i class="fas fa-arrow-up"></i> 9% Faster</small>
        </div>
      </div>
    </div>
  </section>

  <!-- Phase 1: Problem Identification -->
  <section class="phase-section">
    <h2 class="mb-4">🎯 Phase 1: Problem Identification</h2>
    <div class="row">
      <div class="col-lg-8">
        <h4>Selected Use Case: <strong>Genomic Disease Risk Prediction</strong></h4>
        <p class="lead">Build a polygenic risk score (PRS) model to predict individual disease susceptibility from whole-genome sequencing data.</p>
        <div class="code-block">
          <strong>Business Problem:</strong> "Enable early intervention and personalized treatment strategies for complex diseases by analyzing 84 million genetic variants across 2,504 global samples."
        </div>
      </div>
    </div>
  </section>

  <!-- Phase 2: Data Sourcing -->
  <section class="phase-section">
    <h2 class="mb-4">📁 Phase 2: Data Sourcing</h2>
    <div class="row">
      <div class="col-md-6">
        <h5><i class="fas fa-database"></i> Dataset: 1000 Genomes Project</h5>
        <p><strong>Source:</strong> International Genome Sample Resource</p>
        <p><strong>Direct Link:</strong> <a href="ftp://ftp.1000genomes.ebi.ac.uk/vol1/ftp/release/20130502/">FTP Repository</a></p>
      </div>
      <div class="col-md-6">
        <div class="code-block">
          <strong>Dataset Specifications:</strong><br>
          • Samples: 2,504 individuals<br>
          • Variants: 84,801,890<br>
          • Populations: 26 global<br>
          • Size: 3.8 TB (compressed)<br>
          • Format: VCF.gz
        </div>
      </div>
    </div>
  </section>

  <!-- Pipeline Architecture -->
  <section class="my-5">
    <h2 class="text-center mb-4">🏗️ Pipeline Architecture</h2>
    <div class="row g-3">
      <div class="col-md-3">
        <div class="architecture-layer">
          <i class="fas fa-database fa-2x mb-3"></i>
          <h5>Bronze Layer</h5>
          <p>Raw Data</p>
          <small>3-4 TB VCF.gz</small>
        </div>
      </div>
      <div class="col-md-3">
        <div class="architecture-layer" style="background: linear-gradient(135deg, #10b981, #059669);">
          <i class="fas fa-shield-alt fa-2x mb-3"></i>
          <h5>Silver Layer</h5>
          <p>Quality Control</p>
          <small>1.5-2 TB Parquet</small>
        </div>
      </div>
      <div class="col-md-3">
        <div class="architecture-layer" style="background: linear-gradient(135deg, #f59e0b, #d97706);">
          <i class="fas fa-star fa-2x mb-3"></i>
          <h5>Gold Layer</h5>
          <p>Feature Engineering</p>
          <small>500-800 GB Feather</small>
        </div>
      </div>
      <div class="col-md-3">
        <div class="architecture-layer" style="background: linear-gradient(135deg, #ef4444, #dc2626);">
          <i class="fas fa-crown fa-2x mb-3"></i>
          <h5>Platinum Layer</h5>
          <p>ML Models</p>
          <small>XGBoost + MLflow</small>
        </div>
      </div>
    </div>
  </section>

</div>

<script>
// Animation for metric cards
document.addEventListener('DOMContentLoaded', function() {
  const metricCards = document.querySelectorAll('.metric-card');
  
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.1 });

  metricCards.forEach(card => {
    card.style.opacity = '0';
    card.style.transform = 'translateY(20px)';
    card.style.transition = 'all 0.6s ease';
    observer.observe(card);
  });
});
</script>
