# scRNAseq_Caco2_Vero_E_intestinalis
Single-cell transcriptomics of *Encephalitozoon intestinalis* infection in Caco-2 and Vero cells

**Introduction**

In this study, we use single-cell RNA sequencing in Caco-2 and Vero cells infected with a human microsporidian parasite *E. intestinalis* to investigate the host response to infection and the transcriptional dynamics of parasite development. Caco-2 and Vero cells were infected with *E. intestinalis* for 12 hpi, 18 hpi, 24 hpi, 36 hpi and 42 hpi. Uninfected cells were used as a negative control. 

To combine cells from different infection timepoints and uninfected cells for scRNA-seq library preparation, the cells from each infection timepoint were hashed. Libraries were generated according to the manufacturer's protocol (10x Genomics, USA) and sequenced on half a lane of a NovaSeq X 10B flow cell (Illumina, USA).

Caco-2 infected cell dataset: contains 22,748 cells (12 hpi, 18 hpi, 24 hpi, 36 hpi and 42 hpi and uninfected cells)

Vero infected cell dataset: contains 24,543 cells (12 hpi, 18 hpi, 24 hpi, 36 hpi and 42 hpi and uninfected cells)


**Workflow**

**A. Raw sequencing reads data processing (cellranger)**

1. Generation of the combined reference genome between Human and E. intestinalis

2. Generation of the combined reference genome between African Green Monkey and E. intestinalis

3. Mapping raw reads with the combined reference genome and generation of gene expression matrix

**B. scRNA-seq data processing (Seurat in R)**

1. Demultiplexing cells from different infection timepoints

2. Filtering of bad quality cells

3. Normalization and dimensionality reduction

4. Cell clustering

5. Identification of marker genes and differentially expressed genes


**Documentation**

A combined reference genome containing both the human genome (GRch38; GCF_000001405.40; contains nuclear and mitochondrial genomes) and the E. intestinalis genome (ATCC 50506; GCF_000146465.1) or the African Green Monkey genome (GCF_000409795.2) and the E. intestinalis genome was generated using Cell Ranger software version 9.0.1 with the Cell Ranger mkref function (10X Genomics, USA). Raw sequencing reads were mapped to the combined reference genome and the gene expression matrices were generated using the Cell Ranger count function with default parameters. 

The raw sequencing reads from all three libraries can be downloaded from NCBI GEO (NCBI GEO accession no: )

Gene expression matrices were processed using Seurat in R using three strategies

1. Total transcriptome processing
2. Parasite only transcripts processing
3. Human only transcripts processing

**List of tools/versions used in this study**

* cellranger/9.0.1
* bcl2fastq/2.20.0 
* seurat/5.3.0
* tidyverse 
* dplyr 
* RColorBrewer 
* ggplot2 
