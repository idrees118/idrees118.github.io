<div align="center">

# 🧬 Genomic Biomarker Discovery Platform
### Enterprise-Scale Data Lakehouse & Cost Simulation Engine

[![Architecture](https://img.shields.io/badge/Architecture-Data_Lakehouse-8A2BE2?style=for-the-badge&logo=apache-spark)](https://spark.apache.org/)
[![Scale](https://img.shields.io/badge/Scale-Petabyte_Class-2ea44f?style=for-the-badge&logo=amazonaws)](https://aws.amazon.com/)
[![Domain](https://img.shields.io/badge/Domain-Precision_Medicine-007EC6?style=for-the-badge&logo=dna)](https://www.genome.gov/)
[![Status](https://img.shields.io/badge/Status-Academic_Research-orange?style=for-the-badge)](https://github.com/)

<br />

**A simulation engine modeling the computational physics and financial unit economics of processing 500,000+ Whole Genome Sequences.**

[View Demo](index.html) · [Report Bug](issues) · [Request Feature](issues)

</div>

---

## 📖 Executive Summary

The **Genomic Biomarker Discovery Platform** addresses the critical infrastructure bottleneck in population-scale genomics (e.g., **UK Biobank**, **All of Us**).

Processing **500,000 Whole Genome Sequences (WGS)** generates over **15 Petabytes** of raw data. Traditional architectures (VCF/BAM flat files) are financially unsustainable at this scale, often exceeding **$1.5M/month** in storage fees. 

This project demonstrates a **Modern Data Lakehouse** approach, achieving a **94% reduction in operational costs** ($0.17/patient/month) while enabling high-performance ML training on **42 Trillion** data points.

---

## 📊 Dataset Scale & "Real-World" Context

To understand the cost model, one must first appreciate the sheer magnitude of the data being simulated.

| Metric | Value | Description |
| :--- | :--- | :--- |
| **Total Cohort Size** | `500,000` | Patients with 30x WGS Coverage |
| **Feature Complexity** | `84 Million` | Unique genetic variants per patient |
| **Raw Data Volume** | `15.4 PB` | Uncompressed BAM/CRAM files (Archival) |
| **Active Data Volume** | `400 TB` | Compressed Parquet files (Analytical) |

---

## 💰 Financial Impact Analysis

A key output of this simulator is the **Total Estimated Monthly Cost** (~$88,000). While high in absolute terms, it represents extreme efficiency compared to legacy models.

### 🔴 Legacy vs. 🟢 Modern Architecture

| Cost Component | Legacy Model (Standard) | Our Lakehouse Model | Efficiency Gain |
| :--- | :--- | :--- | :--- |
| **Storage Strategy** | All data in S3 Standard | 🔴 Hot + 🔵 Deep Archive | **95% Savings** |
| **Data Format** | Raw VCF (Text) | 🟢 Parquet (Binary) | **90% Compression** |
| **Compute Strategy** | On-Demand Instances | 🟢 Spot Instances | **70% Savings** |
| **Monthly Bill** | `~$1,500,000` | `~$88,000` | **94% Reduction** |

### 💡 Strategic Research Insight
> **Managing a genomic asset value of $250 Million (the sequencing cost of 500k genomes) for an operational cost of just 0.035% per month demonstrates extreme financial viability for large-scale longitudinal studies.**

---

## 🏗️ System Architecture

The simulation logic is based on a production-grade **AWS Genomic Data Lake** pipeline.

```mermaid
graph TB
    subgraph "Ingestion Layer (Cold)"
        A[Raw Sequencing Data] -->|FASTQ/CRAM| B[AWS Glacier Deep Archive]
        B -->|Cost Basis| C["$0.00099 / GB"]
    end
    
    subgraph "Analytical Layer (Hot)"
        B -.->|Spark ETL| D[Delta Lake Storage]
        D -->|Format| E[Compressed Parquet]
        E -->|Cost Basis| F["$0.023 / GB"]
        E -.->|Optimization| G[10x Compression vs VCF]
    end
    
    subgraph "Discovery Layer (Compute)"
        E --> H[Distributed XGBoost]
        H -->|Hardware| I[NVIDIA A100 Cluster]
        I -->|Scaling| J[Spot Instances]
    end
