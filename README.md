# Comprehensive-RNA-Seq-Analysis-of-Monocyte-Derived-Macrophages-in-Systemic-Sclerosis(SSc)
Systemic Sclerosis (SSc) is a chronic autoimmune connective tissue disease characterized by vascular abnormalities, immune dysregulation, and progressive fibrosis. Macrophages play an important role in inflammatory and fibrotic processes associated with SSc.
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

 ## Dataset Information

The RNA-seq data used in this project were obtained from the NCBI Gene Expression Omnibus (GEO) dataset GSE104174, titled "Changes in macrophage transcriptome associate with systemic sclerosis and mediate GSDMA contribution to disease risk."

- GEO Accession: GSE104174
- SRA Accession: SRP118741
- BioProject: PRJNA411909
- Organism: Homo sapiens
- Data type: RNA-seq
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
SRA Toolkit
(prefetch)
        ↓
SRA → FASTQ Conversion
(fasterq-dump)
        ↓
FASTQ Files
        ↓
Quality Control
(FastQC)
        ↓
Quality Aggregation
(MultiQC)
        ↓
Read Trimming
(Not Required)
        ↓
Read Alignment
(Human Reference Genome)
        ↓
SAM/BAM Files
        ↓
Gene-level Quantification
(featureCounts)
        ↓
Raw Count Matrix
        ↓
Sample Metadata
(Control vs MDM)
        ↓
Low-count Filtering
        ↓
Differential Expression Analysis
(DESeq2)
        ↓
DEG Identification
        ↓
Upregulated / Downregulated Genes
        ↓
PCA Plot
        ↓
MA Plot
        ↓
Volcano Plot
        ↓
Heatmap
        ↓
Final Results & Interpretation
```

## Results Visualization

Four major visualizations were generated to assess differential gene expression:

1. *PCA Plot* – Evaluated sample-level expression patterns and separation between MDM and Control samples.
2. *MA Plot* – Visualized log2 fold changes across different expression levels.
3. *Volcano Plot* – Highlighted significantly upregulated and downregulated genes based on fold change and adjusted p-value.
4. *Heatmap* – Displayed expression patterns of the top 50 differentially expressed genes across all samples.

## Key Findings

- 78,932 genes were initially quantified.
- 16,288 genes were retained after low-count filtering.
- 1,775 significant DEGs were identified using padj < 0.1.
- 935 genes were upregulated.
- 840 genes were downregulated.
- PCA, MA plot, Volcano plot, and Heatmap were used to visualize the differential expression patterns.

## Conclusion

This project successfully identified transcriptional differences between *Control and monocyte-derived macrophage (MDM)* samples using RNA-seq differential expression analysis.

A total of *1,775 significant DEGs* were identified, including *935 upregulated* and *840 downregulated genes*. The PCA, MA plot, Volcano plot, and Heatmap provided visual insights into the gene-expression differences between the two conditions.

Overall, the analysis provides a computational overview of transcriptional changes associated with the *monocyte-derived macrophage state*

## Software & Tools
* SRA Toolkit
* FastQC
* MultiQC
* HISAT2
* Samtools
* Human Reference Genome
* featureCounts
* R
* DESeq2
* ggplot2
* pheatmap
* ggrepel
