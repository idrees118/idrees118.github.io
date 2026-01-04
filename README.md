<div align="center">

# 🧬 Genomic Biomarker Discovery Platform
### Enterprise-Scale Data Lakehouse & Cost Simulation Engine

[![Architecture](https://img.shields.io/badge/Architecture-Data_Lakehouse-8A2BE2?style=for-the-badge&logo=apache-spark)](https://spark.apache.org/)
[![Scale](https://img.shields.io/badge/Scale-Petabyte_Class-2ea44f?style=for-the-badge&logo=amazonaws)](https://aws.amazon.com/)
[![Domain](https://img.shields.io/badge/Domain-Precision_Medicine-007EC6?style=for-the-badge&logo=dna)](https://www.genome.gov/)
[![Demo](https://img.shields.io/badge/Live_Demo-View_Project-FF4500?style=for-the-badge&logo=github)](https://idrees118.github.io/)

<br />

**A simulation engine modeling the computational physics and financial unit economics of processing 500,000+ Whole Genome Sequences.**

[View Live Demo](https://idrees118.github.io/) 

</div>

---

## Executive Summary

The **Genomic Biomarker Discovery Platform** addresses the critical infrastructure bottleneck in population-scale genomics (e.g., **UK Biobank**, **All of Us**).

Processing **500,000 Whole Genome Sequences (WGS)** generates over **15 Petabytes** of raw data. Traditional architectures (VCF/BAM flat files) are financially unsustainable at this scale, often exceeding **$1.5M/month** in storage fees. 

This project demonstrates a **Modern Data Lakehouse** approach, achieving a **94% reduction in operational costs** ($0.17/patient/month) while enabling high-performance ML training on **42 Trillion** data points.

---

## Dataset Scale & "Real-World" Context

To understand the cost model, one must first appreciate the sheer magnitude of the data being simulated.

| Metric | Value | Description |
| :--- | :--- | :--- |
| **Total Cohort Size** | `500,000` | Patients with 30x WGS Coverage |
| **Feature Complexity** | `84 Million` | Unique genetic variants per patient |
| **Raw Data Volume** | `15.4 PB` | Uncompressed BAM/CRAM files (Archival) |
| **Active Data Volume** | `400 TB` | Compressed Parquet files (Analytical) |

---

## Financial Impact Analysis

A key output of this simulator is the **Total Estimated Monthly Cost** (~$88,000). While high in absolute terms, it represents extreme efficiency compared to legacy models.

### Legacy vs. Modern Architecture Comparison

| Cost Component | Legacy Model (Standard) | Our Lakehouse Model | Efficiency Gain |
| :--- | :--- | :--- | :--- |
| **Storage Strategy** | All data in S3 Standard | **Tiered (Hot + Deep Archive)** | **95% Savings** |
| **Data Format** | Raw VCF (Text) | **Parquet (Binary)** | **90% Compression** |
| **Compute Strategy** | On-Demand Instances | **Spot Instances** | **70% Savings** |
| **Monthly Bill** | ~$1,500,000 | **~$88,000** | **94% Reduction** |
| **Cost Per Patient** | $3.00 / month | **$0.17 / month** | **Best-in-Class** |

> ** Strategic Research Insight:**
> Managing a genomic asset value of **$250 Million** (the sequencing cost of 500k genomes) for an operational cost of just **0.035% per month** demonstrates extreme financial viability for large-scale longitudinal studies.

---

##  Technical Optimization Strategies

Here is exactly what we used to achieve these savings:

### 1. Intelligent Storage Tiering (Hot vs. Cold)
* **The Problem:** Storing 15 Petabytes of raw sequencing data (CRAM files) in standard cloud storage is prohibitively expensive ($0.023/GB).
* **Our Solution:** We moved 97% of the data (the raw reads) to **AWS Glacier Deep Archive** ($0.00099/GB), which is 23x cheaper. We only keep the "Hot" analytical data (variants) in expensive storage.

### 2. Columnar Compression (Parquet vs. VCF)
* **The Problem:** Genomic data usually comes in VCF format, which is a bloated text file.
* **Our Solution:** We utilized **Apache Parquet**, a binary columnar format. This compresses genomic data by **10-20x** compared to text, drastically reducing the storage footprint and speeding up queries.

### 3. Spot Instance Computing
* **The Problem:** Running high-performance GPU clusters for weeks costs a fortune.
* **Our Solution:** The pipeline is designed to be fault-tolerant, allowing us to use **Spot Instances** (spare cloud capacity) which are **60-70% cheaper** than standard on-demand servers.

---

##  System Architecture

The simulation logic is based on a production-grade **AWS Genomic Data Lake** pipeline.

```mermaid
graph TB
    %% Nodes
    subgraph Cold_Layer ["🔵 Cold Storage Layer (Archival)"]
        A[Raw Sequencing Data] -->|FASTQ/CRAM| B[AWS Glacier Deep Archive]
        B -->|Cost Basis| C["$0.00099 / GB"]
    end
    
    subgraph Hot_Layer ["🟠 Hot Analytical Layer (Active)"]
        B -.->|Spark ETL| D[Delta Lake Storage]
        D -->|Format| E[Compressed Parquet]
        E -->|Cost Basis| F["$0.023 / GB"]
        E -.->|Optimization| G[10x Compression vs VCF]
    end
    
    subgraph Compute_Layer ["🟢 Discovery Layer (Compute)"]
        E --> H[Distributed XGBoost]
        H -->|Hardware| I[NVIDIA A100 Cluster]
        I -->|Scaling| J[Spot Instances]
    end

    %% Styles
    classDef cold fill:#e1f5fe,stroke:#01579b,stroke-width:2px;
    classDef hot fill:#fff3e0,stroke:#e65100,stroke-width:2px;
    classDef compute fill:#e8f5e9,stroke:#1b5e20,stroke-width:2px;

    class A,B,C cold;
    class D,E,F,G hot;
    class H,I,J compute;
