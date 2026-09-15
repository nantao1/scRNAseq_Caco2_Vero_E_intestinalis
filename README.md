# scRNAseq_Caco2_Vero_E_intestinalis
Single-cell transcriptomics of *Encephalitozoon intestinalis* infection in Caco-2 and Vero cells

**Introduction**

In this study, we use single-cell RNA sequencing in Caco-2 and Vero cells infected with a human microsporidian parasite *E. intestinalis* to investigate the host response to infection and the transcriptional dynamics of parasite development. Caco-2 and Vero cells were infected with *E. intestinalis* for 12 hpi, 18 hpi, 24 hpi, 36 hpi and 42 hpi. Uninfected cells were used as a negative control. 

To combine cells from different infection timepoints and uninfected cells for scRNA-seq library preparation, the cells from each infection timepoint were hashed. Libraries were generated according to the manufacturer's protocol (10x Genomics, USA) and sequenced on half a lane of a NovaSeq X 10B flow cell (Illumina, USA).

Caco-2 infected cell dataset: 22,748 cells (12 hpi, 18 hpi, 24 hpi, 36 hpi and 42 hpi and uninfected cells)

Vero infected cell dataset: 24,543 cells (12 hpi, 18 hpi, 24 hpi, 36 hpi and 42 hpi and uninfected cells)


**Documentation**

A combined reference genome containing both the human genome (GRch38; GCF_000001405.40; contains nuclear and mitochondrial genomes) and the *E. intestinalis* genome (ATCC 50506; GCF_000146465.1) or the African Green Monkey genome (GCF_000409795.2) and the *E. intestinalis* genome was generated using Cell Ranger software version 9.0.1 with the Cell Ranger mkref function (10X Genomics, USA). Raw sequencing reads were mapped to the combined reference genome, and the gene expression matrices were generated using the Cell Ranger count function with default parameters. 

The raw sequencing reads from all three libraries can be downloaded from NCBI GEO (NCBI GEO accession no: GSE347271)

Gene expression matrices were processed using Seurat in R using three strategies

1. Total transcriptome processing: The combined host and parasite transcriptomes were analyzed in the Caco-2 infected cell dataset or the Vero infected cell dataset.
* [Total Transcriptome: Caco-2 infected cell dataset](https://github.com/nantao1/scRNAseq_Caco2_Vero_E_intestinalis/blob/fe971876bd306cb2c1f1cb2ff23b4ab2efc5b406/Total_Transcriptome_Caco2_infected_cell_dataset)
* [Total Transcriptome: Vero infected cell dataset](https://github.com/nantao1/scRNAseq_Caco2_Vero_E_intestinalis/blob/ebaba9c332cac6261a615b031275b345896065e2/Total_Transcriptome_Vero_infected_cell_dataset)

2. Parasite only transcripts processing: Parasite transcripts were analyzed separately in order to understand the dynamics of *E. intestinalis* gene expression during parasite development and if it differs between the two host cell lines.
* [Parasite only transcriptome: Caco-2 infected cell dataset](https://github.com/nantao1/scRNAseq_Caco2_Vero_E_intestinalis/blob/ebaba9c332cac6261a615b031275b345896065e2/Parasite_Only_Transcriptome_Caco2_infected_cell_dataset) 
* [Parasite only transcriptome: Vero infected cell dataset](https://github.com/nantao1/scRNAseq_Caco2_Vero_E_intestinalis/blob/ebaba9c332cac6261a615b031275b345896065e2/Parasite_Only_Transcriptome_Vero_infected_cell_dataset)
   
3. Host only transcripts processing: Host transcripts were analyzed separately in order to understand the host response to *E. intestinalis* infection in both Caco-2 and Vero cells.
* [Host only transcriptome: Caco-2 infected cell dataset](https://github.com/nantao1/scRNAseq_Caco2_Vero_E_intestinalis/blob/ebaba9c332cac6261a615b031275b345896065e2/Host_Only_Transcriptome_Caco2_infected_cell_dataset)
* [Host only transcriptome: Vero infected cell dataset](https://github.com/nantao1/scRNAseq_Caco2_Vero_E_intestinalis/blob/ebaba9c332cac6261a615b031275b345896065e2/Host_Only_Transcriptome_Vero_infected_cell_dataset)

**List of tools/versions used in this study**

* cellranger/9.0.1
* bcl2fastq/2.20.0 
* seurat/5.3.0
* tidyverse 
* dplyr 
* RColorBrewer 
* ggplot2 
