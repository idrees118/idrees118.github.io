<div align="center">

# 🧬 Genomic Biomarker Discovery Platform
### Enterprise-Scale Genomic Data Lakehouse & Cost Simulation Engine

[![Domain](https://img.shields.io/badge/Domain-Precision_Medicine-007EC6?style=for-the-badge&logo=dna)](https://www.genome.gov/)
[![Demo](https://img.shields.io/badge/Live_Demo-View_Project-FF4500?style=for-the-badge&logo=github)](https://idrees118.github.io/)

<br/>

**A large-scale simulation platform modeling the computational and financial unit economics of processing 500,000+ Whole Genome Sequences using modern cloud-native architectures.**

</div>

---

## 📌 Executive Summary

The **Genomic Biomarker Discovery Platform** addresses a fundamental bottleneck in population-scale genomics: **the prohibitive cost of storing and analyzing hundreds of thousands of whole genomes**.

Large national initiatives such as **UK Biobank** and **NIH All of Us** generate **petabyte-scale sequencing data**. Processing **500,000 Whole Genome Sequences (30× coverage)** produces more than **15 petabytes of raw data**, making traditional flat-file genomic architectures (VCF/BAM in standard cloud storage) financially unsustainable.

This project demonstrates how a **Modern Data Lakehouse architecture** can:

- Achieve a **94% reduction in operational costs**
- Reduce storage to **$0.17 per patient per month**
- Enable scalable ML workflows across **42 trillion genomic data points**

---

## 🌍 Real-World Dataset Scale & Context

The simulator reflects **realistic sequencing volumes, formats, and access patterns** used in production genomics environments.

| Metric | Value | Description |
|------|------|------------|
| **Cohort Size** | 500,000 | Individuals with 30× WGS coverage |
| **Variant Complexity** | 84 million | Unique variants per individual |
| **Raw Data Volume** | 15.4 PB | FASTQ / BAM / CRAM (archival) |
| **Active Analytical Data** | ~400 TB | Optimized Parquet datasets |

> This scale mirrors national and multinational precision-medicine programs.

---

## 💰 Financial Impact Analysis

A primary output of this simulation is the **estimated total monthly infrastructure cost: ~$88,000**.

While substantial in absolute terms, this represents **extreme cost efficiency** when compared to legacy genomic systems.

### Legacy vs. Lakehouse Architecture

| Cost Component | Legacy Architecture | Lakehouse Architecture | Improvement |
|---------------|--------------------|-----------------------|------------|
| Storage Model | All data in S3 Standard | Tiered (Hot + Deep Archive) | **95% savings** |
| Data Format | VCF (text-based) | Parquet (columnar) | **90% compression** |
| Compute Model | On-demand instances | Spot instances | **70% savings** |
| Monthly Cost | ~$1,500,000 | **~$88,000** | **94% reduction** |
| Cost / Patient | $3.00 / month | **$0.17 / month** | Best-in-class |

> **Strategic Insight:**
> Managing a **$250M genomic asset** (sequencing cost of 500k genomes) for **0.035% of its value per month** demonstrates long-term financial sustainability for longitudinal studies.

---

## ⚙️ Core Optimization Strategies

The cost reductions are achieved through **three deliberate architectural decisions**.

### 1️⃣ Intelligent Storage Tiering (Hot vs. Cold)

**Problem:** Storing 15+ PB of raw sequencing data in standard cloud storage is prohibitively expensive.

**Solution:**
- 97% of raw reads are moved to **AWS Glacier Deep Archive**.
- Only analytical-ready data remains in high-performance storage.

💡 Result: **23× reduction in archival storage costs**

### 2️⃣ Columnar Compression (Parquet vs. VCF)

**Problem:** VCF files are text-based and inefficient for large-scale analytics.

**Solution:**
- Use **Apache Parquet**, a binary columnar format.
- Enables predicate pushdown, column pruning, and high compression.

💡 Result: **10–20× data size reduction and faster queries**

### 3️⃣ Spot Instance Compute Strategy

**Problem:** Long-running GPU clusters are extremely expensive when using on-demand instances.

**Solution:**
- Fault-tolerant pipeline design.
- Leverages **Spot Instances** for distributed ML training.

💡 Result: **60–70% compute cost reduction**

---

## 🏗️ System Architecture

The simulation mirrors a **production-grade AWS Genomic Data Lake** architecture.

```mermaid
graph TB
    subgraph Cold [🔵 Cold Storage Layer]
        A[Raw Sequencing Data] -->|FASTQ / CRAM| B[AWS Glacier Deep Archive]
        B --> C["$0.00099 / GB"]
    end

    subgraph Hot [🟠 Hot Analytical Layer]
        B -.->|Spark ETL| D[Delta Lake]
        D --> E[Parquet Storage]
        E --> F["$0.023 / GB"]
        E -.-> G[10× Compression]
    end

    subgraph Compute [🟢 Compute & ML Layer]
        E --> H[Distributed XGBoost]
        H --> I[NVIDIA A100 GPUs]
        I -->|Scaling| J[Spot Instances]
    end

    %% Diagram Styling
    classDef cold fill:#e1f5fe,stroke:#01579b,stroke-width:2px;
    classDef hot fill:#fff3e0,stroke:#e65100,stroke-width:2px;
    classDef compute fill:#e8f5e9,stroke:#1b5e20,stroke-width:2px;

    class A,B,C cold;
    class D,E,F,G hot;
    class H,I,J compute;
