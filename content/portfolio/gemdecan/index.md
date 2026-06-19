---
title: "GEMDeCan: Tumor Immune Microenvironment Deconvolution"
date: 2021-04-09
summary: "Snakemake pipelines for tumor immune microenvironment deconvolution from RNA-seq and DNA methylation data, applied to 7,000+ TCGA samples and 166 immunotherapy patients."
---

Multi-omics deconvolution framework to profile the tumor immune microenvironment (TME) and predict immunotherapy response, developed at the **Cancer Research Center of Toulouse (CRCT)**.

## Key Contributions

- **Pipeline Development:** Led the design and implementation of two containerized Snakemake pipelines — one for gene expression deconvolution, one for DNA methylation deconvolution — processing multi-omics data across multiple cancer cohorts.
- **Novel Signatures:** Contributed to deriving novel deconvolution signatures (BPRNACan, BPRNACan3DProMet, BPmetCan) for B cells, CD4/CD8 T cells, M0/M1/M2 macrophages, monocytes, neutrophils, NK cells, and cancer cells.
- **Scale:** ~7,000+ TCGA RNA-seq samples for signature derivation; immunotherapy response prediction validated on 166 patients across 6 external cohorts (melanoma, bladder, GBM, lung).
- **3D Chromatin Integration:** Incorporated PCHi-C 3D chromatin contacts from GARDEN-NET into the BPRNACan3DProMet signature, bridging chromatin architecture and immune deconvolution.

## Technical Approach

Gene expression deconvolution (bulk RNA-seq: BCL → FASTQ → TPM via STAR/RSEM/Salmon) and DNA methylation arrays (Illumina 450K and EPIC; IDAT → beta values via ChAMP/minfi) are processed in parallel pipelines. Immunotherapy response prediction uses ElasticNet penalized logistic regression with leave-one-dataset-out (LODO) cross-validation across the 6 immunotherapy cohorts.

**Technologies:** Python · Snakemake · R · Docker · Singularity · STAR · RSEM · Salmon · Scikit-Learn · ChAMP · minfi · immunedeconv · EpiDish · CIBERSORTx · Tidyverse.

[View preprint on bioRxiv](https://doi.org/10.1101/2021.04.09.439207)
