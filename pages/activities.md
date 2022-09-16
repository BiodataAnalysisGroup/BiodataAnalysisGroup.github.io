---
title: Our research activities
description: Listing our projects here
background: /assets/img/groupLogo/cropped-background.jpg
permalink: /activities/
---

[**Machine Learning**](#machine-learning) &nbsp; 

[**Multi-omics**](#multi-omics) &nbsp;
   - [**Analysis of raw NGS data**](#analysis-of-raw-ngs-data-fastq)
   - [**Downstream analysis**](#downstream-analysis)
   - [**Data Integration**](#data-integration)
   - [**Single-cell RNA-seq (scRNA-seq) analysis**](#single-cell-rna-seq-scrna-seq-analysis-a-systems-approach)
   - [**Pan-genome analysis and microbial Genome-wide Association studies (GWAS)**](#pan-genome-analysis-and-microbial-genome-wide-association-studies-gwas)) 


[**Core Bioinformatics tool development**](#core-bioinformatics-tool-development) &nbsp; 

[**Training**](#training)

## Machine Learning

![Machine Learning](/assets/img/activities/Machine_Learning_Logo.png){: .rounded .float-left width="100px"}

Machine Learning approaches are widely used in this era of highly dimensional Biological “Big-Data” to leverage actionable biological and potentially therapeutic insights.

<br/>

{: .clearfix}


Applying approaches:

- Principal Component Analysis (PCA) and generalized Principal Component Analysis (GLM-PCA)
- Random Forest
- Support vector machine
- Cluster Analysis
- t-SNE / UMAP
- Feature selection
- Ensemble methods [metaDIEA](https://github.com/BiodataAnalysisGroup/metaDIEA)

Leading efforts on standards:
- [DOME Recommendations](https://www.nature.com/articles/s41592-021-01205-4)
- [FAIR for Machine Learning](https://www.rd-alliance.org/groups/fair-machine-learning-fair4ml)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Multi-omics

The Next Generation Sequencing (NGS) pipelines generate voluminous biological data. The process of analyzing omics data usually leads to a high dimensional matrix, with the different cases listed as columns and the locations on the genome in which the examined event happened (e.g. mutation, gene expression etc.) as rows.

Relevant computational approaches in the biomedical domain include:

1. High throughput immunogenetic analysis in health and disease
2. Integrated omics analysis of hematologic malignancies: DNA methylome and Transcriptome Profiling in patients with hematologic malignancies treated with chemotherapy versus novel agents; Whole exome sequencing of pre-malignant conditions
3. Targeted NGS analysis for improved risk stratification in cancer: novel recurrent gene mutations in hematologic malignancies


#### Analysis of raw NGS data (.fastq)

- Immuno-sequencing (_IMGT_)
- RNAseq (_HISAT2_)
- WES (_GATK_)
- ChIP-seq (_MACS2_)

#### Downstream analysis

- Immunogetics analysis ([_TRIP - T cell receptor/immunoglobulin profiler_](https://github.com/BiodataAnalysisGroup/tripr), [_IgIDivA_](https://github.com/laurazara/IgIDivA) )
- Differential analysis (_DEseq2_, _limma_)
- Eenrichment analysis (_Over Representation Analysis/GSEA_, _KEGG_, _GO_, _Reactome_ , _WikiPathway_, _Appyters_)
- Transciption factor binding site analysis (_PWA_)
- Network-based Bayesian inference of signaling drivers and transcription factors (_NetBID_, _Cytoscape_, _STRINGdb_)

#### Data Integration
We developed a high-speed framework, called InterTADs, for integrating multi-omics data from the same physical source (e.g. patient) considering the chromatin configuration of the genome, i.e. the topologically associating domains (TADs).
[Check it out on our github](https://github.com/nikopech/InterTADs)

#### Single-cell RNA-seq (scRNA-seq) analysis: A Systems approach

We are assembling a computational pipeline with various in silico tools for the analysis of scRNA-seq data to facilitate the inference of actionable biological information for Systems Immunology studies. Some indicative tools from our pipeline are cited below:

1. Pre-processing (batch FASTQ to count matrices) (_Starsolo_), 
2. Basic downstream analysis (quality control, normalization, selection of variable features, scaling, dimensionality reduction, integration/batch correction, clustering, visualization) (_Seurat_, _Monocle3_, _Scanpy_)
3. Functional studies:
   - Cell annotation (_SingleR_)
   - Trajectory pseudotime (_SCORPIUS_, _Monocle3_)
   - Gene regulatory networks (_SCENIC_)
   - Pathway enrichment (_VAM_)
   - Cell-cell interactions (_CellChat_, _NicheNet_)

#### Pan-genome analysis and microbial Genome-wide Association studies (GWAS)

We are implementing a computational workflow which integrates various software tools in order to detect significant associations between genomic features, such as homolog gene clusters or SNPs, and phenotypic traits of interest (e.g., antimicrobial resistance) concerning different microorganisms. Some of the steps of are workflow are cited below:

- Pipeline for SNP calling in core genes (100% read coverage)(_BWA-MEM_, _GATK4 HaplotypeCaller_, _samtools_, _bcftools_, _vcftools_)
- SNP concatenation & phylogenetic tree (RAxML)
- Genome assembly (_SPAdes_, _Quast_)
- Annotation of genes related to antibiotic resistance, virulence, and stress (_AMRFinderPlus_)
- Genome annotation (_PROKKA_)
- Pan-genome analysis (_Panaroo_)
- Genome-wide association study (_pyseer_)
- Microbial gene annotation (_InterProScan_)
- Custom R scripts for further analysis and interpretation of the results

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Core Bioinformatics tool development

We are also active in developing tailored bioinformatic tools that addess specific challenges. These include:
1. NGS Wastewater analysis of SARS-CoV-2 mutations ([_lineagespot_](https://github.com/BiodataAnalysisGroup/lineagespot) ) 
2. Demultiplexing of UMIs ([_Umic_](https://github.com/BiodataAnalysisGroup/UMIc) )
3. Tools for analyzing miRNA data ([_mirkit_](https://github.com/BiodataAnalysisGroup/miRkit) )
4. Using k-mer based representation of omics data ([_Goedel_](https://github.com/BiodataAnalysisGroup/), [_k-taxa_](https://github.com/BiodataAnalysisGroup/k-taxatree), [_kmeranalyzer_](https://github.com/BiodataAnalysisGroup/kmerAnalyzer))

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Training


### Introduction to Machine Learning: Opportunities for advancing omics data analysis

**Material**
- [website](https://fpsom.github.io/IntroToMachineLearning/)
- [github](https://github.com/fpsom/IntroToMachineLearning)

Machine learning has emerged as a discipline that enables computers to assist humans in making sense of large and complex data sets. With the drop-in cost of sequencing technologies, large amounts of omics data are being generated and made accessible to researchers. Analyzing these complex high-volume data is not trivial and the use of classical tools cannot explore their full potential. Machine learning can thus be very useful in mining large omics datasets to uncover new insights that can advance the field of medicine and improve health care.

The aim of this tutorial is to introduce participants to the Machine learning (ML) taxonomy and common machine learning algorithms. The tutorial will cover the methods being used to analyze different omics data sets by providing a practical context through the use of basic but widely used R and Python libraries. The tutorial will comprise a number of hands on exercises and challenges, where the participants will acquire a first understanding of the standard ML processes as well as the practical skills in applying them on familiar problems and publicly available real-world data sets.

### ELIXIR / CODATA-RDA Research Data Science Advanced Workshop on Bioinformatics

**Material**
  - [website 2019](https://codata-rda-advanced-bioinformatics-2019.readthedocs.io/en/latest/)
  - [github 2019](https://github.com/fpsom/CODATA-RDA-Advanced-Bioinformatics-2019)
  - [website 2018](https://codata-rda-advanced-bioinformatics-2018.readthedocs.io/en/latest/)
  - [github 2018](https://github.com/fpsom/CODATA-RDA-Advanced-Bioinformatics-2018)

As part of the [CODATA-RDA Research Data Science Summer School](http://www.codata.org/datatrieste2018) in Trieste (6-17 Aug 2018 and 5-16 Aug 2019), ELIXIR Training has contributed in the organization of the flanking Advanced Bioinformatics workshop (20-24 Aug 2018 and 19-23 Aug 2019) with a particular focus on Machine Learning applications, as part of the ELIXIR Implementation Study on Learning Paths.

This advanced bioinformatics course provided an overview of the current status of different NGS workflows (variant calling, RNA-Seq, ChIP-Seq, Metagenomics etc), and combined them with the appropriate Machine Learning and Data Mining approaches. After providing a strong foundation of the underlying theory and concepts, the course relied heavily on hand-on exercises and tutorials in order for the participants to directly apply and practice on methods and techniques presented throughout each day.

The course was led by me (INAB/CERTH, ELIXIR Greece), with [Amel Ghouila](https://github.com/amelgh) (Institut Pasteur de Tunis / H3ABionet), [Gabriele Schweikert](http://homepages.inf.ed.ac.uk/gschweik/) (Cyber Valley Initiative, University of Tübingen, DE / Computational Biology, University of Dundee, UK) and [Phelelani Mpangase](https://github.com/phelelani) (Sydney Brenner Institute for Molecular Bioscience, University of the Witwatersrand, Johannesburg, South Africa) as co-instructors of the course. Moreover, the daily training activities were supported by three helpers; Maria Tsagiopoulou (INAB / CERTH), Ola Karrar (University of Khartoum) and a past learner to the CODATA-RDA Research Data Science Summer School, and David Helekal (University of Dundee).

### Workshop on Reproducible analysis and Research Transparency

**Material**
  - [website](https://reproducible-analysis-workshop.readthedocs.io/en/latest/)
  - [github](https://github.com/fpsom/reproducible-analysis-workshop)

This workshop was part of the [Open Science Tools, Data & Technologies for Efficient Ecological & Evolutionary Research](https://nioo.knaw.nl/en/open-science-tools) Symposium, organized by NIOO-KNAW and DANS-KNAW on 7 & 8 December 2017 at the [Amsterdam Science Park](https://www.amsterdamsciencepark.nl/about-amsterdam-science-park/profile/).

This workshop provided an overview of the to date status in reproducible analysis in order to provide transparency in research. The workshop covered methodological topics (such as the use of the Open Science Framework and reporting guidelines) as well as software tools (such as `Git`, `Docker`, `RMarkdown` / `knitr` and `Jupyter`). Going beyond simple listing and presentations, the workshop focused on hands-on skill building, with exercises and tutorials covering most of the software aspects.
