<div align="center">

# 🧬 Genomic Biomarker Discovery Platform
### Enterprise-Scale Genomic Data Lakehouse & Cost Simulation Engine

[![Domain](https://img.shields.io/badge/Domain-Precision_Medicine-007EC6?style=for-the-badge&logo=dna)](https://www.genome.gov/)
[![Demo](https://img.shields.io/badge/Live_Demo-View_Project-FF4500?style=for-the-badge&logo=github)](https://idrees118.github.io/genomic-biomarker-discovery-platform/)

<br/>

**A large-scale simulation platform modeling the computational and financial unit economics of processing 500,000+ Whole Genome Sequences using modern cloud-native architectures.**

</div>

---

## 📌 Executive Summary

The **Genomic Biomarker Discovery Platform** addresses a fundamental bottleneck in population-scale genomics: **the prohibitive cost of storing and analyzing hundreds of thousands of whole genomes**.

Large national initiatives such as **UK Biobank** and **NIH All of Us** generate **petabyte-scale sequencing data**. Processing **500,000 Whole Genome Sequences (30× coverage)** produces more than **15 petabytes of raw data**, making traditional flat-file genomic architectures (VCF/BAM in standard cloud storage) financially unsustainable.

This project demonstrates how a **Modern Data Lakehouse architecture** can:

- Achieve a **94% reduction in operational costs**
- Reduce storage to **$0.12 per patient per month**
- Enable scalable ML workflows across **42 trillion genomic data points**

---

## 🌍 Real-World Dataset Scale & Context

The simulator reflects **realistic sequencing volumes, formats, and access patterns** used in production genomics environments.

| Metric | Value | Description |
|------|------|------------|
| **Cohort Size** | 500,000 | Individuals with 30× WGS coverage |
| **Variant Complexity** | 84 Million | Unique variants per individual |
| **Total Data Points** | **42 Trillion** | **Genotype matrix elements ($N \times M$)** |
| **Raw Data Volume** | 15.4 PB | FASTQ / BAM / CRAM (archival) |
| **Active Analytical Data** | ~400 TB | Optimized Parquet datasets |

> **Scale Context:** Processing this dataset requires managing a feature matrix of **42,000,000,000,000 elements**, requiring distributed computing (Spark/Dask) rather than single-node processing.

---

## 💰 Financial Impact Analysis

A primary output of this simulation is the **estimated total monthly infrastructure cost: $60,770**.

While substantial in absolute terms, this represents **extreme cost efficiency** when compared to legacy genomic systems.

### Legacy vs. Lakehouse Architecture

| Cost Component | Legacy Architecture | Lakehouse Architecture | Improvement |
|---------------|--------------------|-----------------------|------------|
| Storage Model | All data in S3 Standard | Tiered (Hot + Deep Archive) | **95% savings** |
| Data Format | VCF (text-based) | Parquet (columnar) | **10-20× compression** |
| Compute Model | On-demand instances | Spot instances | **70% savings** |
| Monthly Cost | ~$180,000 | **~$60,770** | **66% reduction** |
| Cost / Patient | $0.36 / month | **$0.12 / month** | Best-in-class |

> **Strategic Insight:**
> Managing a **$250M genomic asset** (sequencing cost of 500k genomes) for **0.024% of its value per month** demonstrates long-term financial sustainability for longitudinal studies.

---

## 🏗️ System Architecture

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
