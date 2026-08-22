# Comprehensive-RNA-Seq-Analysis-of-Monocyte-Derived-Macrophages-in-Systemic-Sclerosis(SSc)
Comprehensive RNA-Seq workflow for investigating gene expression changes in monocyte-derived macrophages associated with Systemic Sclerosis (SSc), including quality control, alignment, quantification, differential expression analysis, and functional interpretation.
## Project Overview

This project focuses on the comparative transcriptomic analysis of *Control samples and monocyte-derived macrophages* using RNA-seq data.
The main objective is to identify *Differentially Expressed Genes (DEGs)* between the control condition and monocyte-derived macrophages and to characterize the transcriptional changes associated with macrophage differentiation.
The RNA-seq data were processed through quality control, read preprocessing, quantification, count matrix generation, differential expression analysis using DESeq2, gene annotation, and visualization.
The identified DEGs provide a foundation for understanding the molecular changes associated with the transition toward a macrophage state and for performing downstream functional analysis.
## Objective

The main objective of this project is to perform a comparative RNA-seq analysis of *Control samples and monocyte-derived macrophages (MDM)*.

The specific objectives are:

- To perform quality control of raw RNA-seq data.
- To preprocess and quantify RNA-seq reads.
- To generate a gene-level count matrix.
- To identify Differentially Expressed Genes (DEGs) between Control and MDM samples.
- To classify DEGs into upregulated and downregulated genes.
- To annotate the identified genes using Ensembl gene identifiers.
- To visualize the transcriptional differences between the two conditions.
- To provide a basis for downstream functional and biological interpretation.
## Study Comparison

The RNA-seq analysis compares two experimental conditions:

| Condition | Samples |
|-----------|---------|
| *Control* | SRR6063653, SRR6063654, SRR6063655 |
| *Monocyte-derived Macrophages (MDM)* | SRR6063627, SRR6063628, SRR6063629 |


## Computational Workflow

```text
SRA Accession Data
        ↓
SRA Toolkit – prefetch
        ↓
SRA Files
        ↓
SRA → FASTQ Conversion
        ↓
FASTQ Files
        ↓
FastQC
        ↓
MultiQC
        ↓
Read Trimming
   [Skipped]
        ↓
Alignment to Human Reference Genome
        ↓
SAM / BAM Alignment Files
        ↓
featureCounts
        ↓
Gene-level Count Matrix
        ↓
Sample Metadata
        ↓
DESeq2 Differential Expression Analysis
        ↓
Differentially Expressed Genes (DEGs)
        ↓
Upregulated / Downregulated Genes
        ↓
Ensembl Gene Annotation
        ↓
PCA Plot
        ↓
MA Plot
        ↓
Volcano Plot
        ↓
Heatmap
        ↓
Downstream Functional Analysis

