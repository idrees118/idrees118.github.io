# 🧬 Genomic Biomarker Discovery Platform
### Enterprise-Scale Data Lakehouse Architecture Simulator

![Project Status](https://img.shields.io/badge/Status-Academic%20Submission-blue)
![Architecture](https://img.shields.io/badge/Architecture-Data%20Lakehouse-purple)
![Scale](https://img.shields.io/badge/Scale-Petabyte-green)

## 📋 Project Overview

This project is a **web-based architectural simulator** designed to model the computational resources, storage tiering, and financial implications of processing **Whole Genome Sequencing (WGS)** data at population scale (e.g., UK Biobank scale).

It demonstrates a **Modern Data Lakehouse** approach, moving away from legacy flat-file storage (VCFs) to optimized columnar formats (Parquet/Delta Lake), resulting in massive cost efficiencies for large-scale Machine Learning pipelines.

---

## 🚀 Live Simulation
The simulation provides real-time modeling of:
* **Data Volume:** 500,000+ WGS Samples (~15 Petabytes raw).
* **Feature Complexity:** 84 Million genetic variants per sample.
* **Infrastructure Costs:** AWS Spot Instances + Glacier Deep Archive.

### 📊 Key Architecture Features
1.  **Tiered Storage Strategy:** * **Hot Storage:** Active analytical data (Parquet) stored in S3 Standard.
    * **Cold Storage:** Raw CRAM/FASTQ files moved to Glacier Deep Archive ($0.00099/GB).
2.  **Distributed ML Training:** * Models the cost of running XGBoost on distributed GPU clusters (NVIDIA A100/V100) using Dask/RAPIDS.
3.  **Scientific Accuracy:** * Calculations account for compression ratios (10:1 for Parquet), shuffle partitions, and diminishing returns on model accuracy (AUPRC).

---

## 📉 Financial Analysis & Unit Economics

A key output of this simulator is the **Total Estimated Monthly Cost** (approx. **$88,000** for 500k samples). While this figure appears high, it represents a **94% cost reduction** compared to legacy architectures.

| Metric | Legacy Architecture | Modern Lakehouse (This Model) |
| :--- | :--- | :--- |
| **Storage Strategy** | All data in S3 Standard | Tiered (Hot + Deep Archive) |
| **Data Format** | Raw VCF (Text) | Snappy-Compressed Parquet |
| **Compute** | On-Demand Instances | Spot Instances (60% Savings) |
| **Monthly Cost** | ~$1,500,000 | **~$88,000** |
| **Cost Per Patient** | $3.00 / month | **$0.17 / month** |

> **Context:** Managing an asset value of **$250 Million** (the sequencing cost of 500k genomes) for an operational cost of **0.035% per month** demonstrates extreme financial efficiency.

---

## 🏗️ Technical Pipeline Visualized

The project uses `Mermaid.js` to render the data flow dynamically:

```mermaid
graph TB
    subgraph "Ingestion & Archival"
        A[Raw WGS Data] --> B[Glacier Deep Archive (Cold)]
    end
    
    subgraph "Active Analytics"
        B -.->|ETL| C[Apache Spark Cluster]
        C --> D[Delta Lake (Hot/Parquet)]
    end
    
    subgraph "Discovery"
        D --> E[Distributed GPU Training]
        E --> F[Biomarker Identification]
    end
