---
title: Our software activities
description: Listing our packages here
background: /assets/img/groupLogo/coding.jpg
permalink: /software/
---

[**lineagespot**](#lineagespot) &nbsp; [**tripr**](#tripr) &nbsp; [**IgIDivA**](#IgIDivA) &nbsp; [**InterTads**](#InterTads) &nbsp; [**UMIc**](#UMIc) &nbsp; [**metaDIEA**](#metaDIEA) &nbsp; [**miRkit**](#miRkit) &nbsp; [**Goedel-numbering**](#Goedel numbering) &nbsp; [**kmerAnalyzer**](#kmerAnalyzer) &nbsp; [**k-taxatree**](#k-taxatree) &nbsp; [**Odysseus**](#Odysseus) &nbsp; [**BEEMUS**](#BEEMUS) &nbsp; [**GridCG**](#GridCG) &nbsp; [**BPM**](#BPM) &nbsp; [**Mutations-Meta-Analyser**](#Mutations-Meta-Analyser) &nbsp; [**align-paths**](#align-paths) &nbsp; [**G-Class**](#G-Class) &nbsp;

<br/>

{: .clearfix}
<br>

# **lineagespot**
![lineagespot](/assets/img/software/lineagespotlogo.png){: .rounded .float-left width="200px"}

<br/>
{: .clearfix}
<br>

lineagespot is a [Bioconductor](http://bioconductor.org) package
written in [R](https://www.r-project.org/), and aims to identify 
SARS-CoV-2 related mutations based on a single (or a list) of variant(s) 
file(s) (i.e., [variant calling format](https://gatk.broadinstitute.org/hc/en-us/articles/360035531692-VCF-Variant-Call-Format)). 

#### Installation

```r
# install.packages("devtools")
devtools::install_github("BiodataAnalysisGroup/lineagespot")
```

#### Raw data analysis

The processing steps of the raw fastq files can be found [here](https://github.com/BiodataAnalysisGroup/lineagespot/blob/master/inst/scripts/raw-data-analysis.md)

#### Material
- [github](https://github.com/BiodataAnalysisGroup/lineagespot)

#### Citation

If you use the tool, please cite the following work:

Nikolaos Pechlivanis, Maria Tsagiopoulou, Maria Christina Maniou, Anastasis Togkousidis, Evangelia Mouchtaropoulou, Taxiarchis Chassalevris, Serafeim Chaintoutis, Chrysostomos Dovas, Maria Petala, Margaritis Kostoglou, Thodoris Karapantsios, Stamatia Laidou, Elisavet Vlachonikola, Anastasia Chatzidimitriou, Agis Papadopoulos, Nikolaos Papaioannou, Anagnostis Argiriou, Fotis Psomopoulos, "_Detecting SARS-CoV-2 lineages and mutational load in municipal wastewater; a use-case in the metropolitan area of Thessaloniki, Greece_", medRxiv 2021.03.17.21252673; doi: [https://doi.org/10.1101/2021.03.17.21252673](https://doi.org/10.1101/2021.03.17.21252673)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **tripr**
![tripr](/assets/img/software/tripr.png){: .rounded .float-left width="200px"}

<br/>
{: .clearfix}
<br>

is a [Bioconductor](http://bioconductor.org) package, written in
[shiny](https://shiny.rstudio.com/) that provides analytics services on
antigen receptor (B cell receptor immunoglobulin, BcR IG | T cell
receptor, TR) gene sequence data. Every step of the analysis can be
performed interactively, thus not requiring any programming skills. It
takes as input the output files of the [IMGT/HighV-Quest
tool](http://www.imgt.org/HighV-QUEST/home.action). Users can select to
analyze the data from each of the input samples separately, or the
combined data files from all samples and visualize the results
accordingly.

Functions for an `R` command-line use are also available.

#### Installation

<!-- When accepted in Bioconductor -->

`tripr` is distributed as a [Bioconductor](https://www.bioconductor.org/) 
package and requires `R` (version "4.1"), which can be installed on any 
operating system from [CRAN](https://cran.r-project.org/), and 
Bioconductor (version "3.14").

To install `tripr` package enter the following commands in your `R` session:


```r
if (!requireNamespace("BiocManager", quietly = TRUE)) {
    install.packages("BiocManager")
}

BiocManager::install("tripr", version="devel")

## Check that you have a valid Bioconductor installation
BiocManager::valid()
```


#### Launching the app

Once `tripr` is successfully installed, it can be loaded as follow:

``` r
library(tripr)
```
#### Material
- [github](https://github.com/BiodataAnalysisGroup/tripr)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **IgIDivA**

#### Overview

`IgIDivA` (Immunoglobulin Intraclonal Diversification Analysis) is a purpose-built tool for the analysis of the intraclonal diversification process using high-throughput sequencing data. It is written in [shiny](https://shiny.rstudio.com/). Every step of the analysis can be performed interactively, thus not requiring any programming skills. It takes as input the output files "clonotypes_computation" and "grouped_alignment_nt" from the [`tripr`](https://bio.tools/TRIP_-_T-cell_Receptor_Immunoglobulin_Profiler) package.  
Functions for an `R` command-line use are also available.  
The UserGuide of IgIDivA can be found [here](https://rpubs.com/laura_zara/911248) and an example dataset to be used as Input of IgIDivA can be found [here](https://doi.org/10.5281/zenodo.6616046).

#### Installation
The `IgIDivA` scripts can be freely downloaded [here](https://github.com/laurazara/IgIDivA).
It requires `R` (version "4.1"), which can be installed on any operating system from [CRAN](https://cran.r-project.org/). `IgIDivA` has been successfully tested in Windows 10, macOS 10.15 and Linux WSL.
All the packages that need to be installed in your `R` session are the following:

```r
install.packages(c("shiny", "shinyFiles", "fs", "pdftools", "purrr", "DT", "bslib", "shinyhelper", "data.table", "stringr", "RGenetics", "dplyr", "ggsci", "tidygraph", "ggraph", "igraph", "ggplot2", "ggpubr", "rstatix", "shinyvalidate"))

```

All the scripts need to be downloaded in the same folder, and the input should be saved in a folder called `Input`  

To run the app, open the script `app.R` in your `R` session and press the button `Run App`.   


Alternatively, `IgIDivA` can be installed using a `conda` environment. We recommend to use [Miniconda](https://docs.conda.io/en/latest/miniconda.html) to install all the dependencies. The dependencies can be found in .yml format [in the IgIDivA GitHub repository](https://github.com/laurazara/IgIDivA). The yml file and the `IgIDivA` scripts need to be stored in the working folder. After downloading all the files, a terminal should be opened and the following commands should be written:  
```r
conda env create -f IgIDivA.yml 
conda activate IgIDivA
R
install.packages(c("shinyvalidate", "RGenetics","rstatix"))
q()
Rscript app.R
```  
This will produce a url that can be copied in a web browser and will direct the user to the IgIDivA app.  

#### Citation

If you use the tool, please cite the following work:

Laura Zaragoza-Infante, Valentin Junet, Nikos Pechlivanis, Styliani-Christina Fragkouli, Serovpe Amprachamian, Triantafyllia Koletsa, Anastasia Chatzidimitriou, Maria Papaioannou, Kostas Stamatopoulos, Andreas Agathangelidis, Fotis Psomopoulos, "_IgIDivA: immunoglobulin intraclonal diversification analysis_", Briefings in Bioinformatics; doi: [https://doi.org/10.1093%2Fbib%2Fbbac349](https://doi.org/10.1093%2Fbib%2Fbbac349)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **InterTads**

`InterTADs` is an open-source tool written in R, for integrating multi-omics data (e.g. DNA methylation, expression, mutation) from the same physical source (e.g. patient) taking into account the chromatin configuration of the genome, i.e. the topologically associating domains (TADs).

#### Material
Installation instructions can be found here:

- [github](https://github.com/BiodataAnalysisGroup/InterTADs)

#### Citation

If you use the tool, please cite the following work:

M. Tsagiopoulou, N. Pechlivanis, and F. Psomopoulos, “InterTADs: Integration of Multi-Omics Data on Topological Associated Domains.” Aug. 2020, doi: [10.21203/rs.3.rs-54194/v1](10.21203/rs.3.rs-54194/v1)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **UMIc**

UMIc is a framework, written in [R](https://www.r-project.org/), implementing a new proposed method for UMI deduplication and reads correction. The method works at nucleotide level, taking into account the frequency and the mean quality of each base. 

#### Prerequisites

The packages needed to be installed, in order to run the project are:
- from CRAN

```r
install.packages(c("tidyverse", "data.table", "stringdist", "pryr"))
```

- from Bioconductor
```r
BiocManager::install(c("Biostrings", "ShortRead"))
```

#### Installing

The project can be downloaded using git:

```r
git clone https://github.com/BiodataAnalysisGroup/UMIc
```

#### Running the project

The framework consists of three scripts:
- ```UMIsProject.R``` 
- ```casesWorkflows.R```
- ```functions.R```

In order to run the project, set the [R](https://github.com/BiodataAnalysisGroup/UMIc/tree/master/R) folder as your working directory, set the input parameters in the main script ```UMIsProject.R``` and then use the following command:
```
source("UMIsProject.R")
```

The project provides example input datasets and their outputs, for testing purposes. The folder [data](https://github.com/BiodataAnalysisGroup/UMIc/tree/master/data) includes example datasets for all three scenarios in their corresponding subfolders. Each subfolder icludes the fastq files and a Readme.md file with the parameter values, used to generate the files in folder [outputs](https://github.com/BiodataAnalysisGroup/UMIc/tree/master/outputs). The user must provide the input and output folders' filepaths. 

#### Inputs
Before running the project, the user must set the appropriate input parameters in the main script ```UMIsProject.R```.

The later has the following inputs:
- ```pairedData```: boolean variable that indicates, whether data are paired ```T``` or single ```F```. 
- ```UMIlocation```: variable that indicates, whether UMI is located only in Read1 ```R1``` or Read1 and Read2 ```R1 & R2```.
- ```UMIlength```: the length of the UMI sequence.
- ```sequenceLength```: the length of the read sequence. 
- ```countsCutoff```: min read counts per UMI, for initial data cleaning.
- ```UMIdistance```: max UMI distance for UMI merging.
- ```sequenceDistance```: max sequence distance for UMI merging.
- ```inputsFolder```: name or filepath of the inputs folder.
- ```outputsFolder```: name or filepath of the outputs folder, default value is ```UMIc_output```.
 
The input data must be provided in fastq files and it is assumed that the UMI is placed at the beginning of each sequence. The library preparation step of the input files must be genarated using the same protocol and fulfil the same input parameters described above.


#### Outputs 
The output data are stored also in fastq files, named the same as the input files with an added ```_corrected``` suffix and the name of the folder can be provided by the user. The files contain the corrected sequences (without the UMI) and their quality. It is worth mentioning that the new sequence ID is constructed by combining the ID of one of the input sequences, that has that same UMI, and the UMI itself.

The framework also produces a csv file with all the information of the output fastq files and extra information, that can help return from the output sequences to their corresponding input sequences. The file is named the same as the Read1 fastq file with an added ```_summary_table``` suffix.

For more details, please refer to the [wiki](https://github.com/BiodataAnalysisGroup/UMIc/wiki).

#### Citation

If you use the tool, please cite the following work:

M. Tsagiopoulou, M. C. Maniou, N. Pechlivanis, A. Togkousidis, M. Kotrová, T. Hutzenlaub, I. Kappas, A. Chatzidimitriou, and F. Psomopoulos, “UMIc: A Preprocessing Method for UMI Deduplication and Reads Correction,” Frontiers in Genetics, vol. 12, May 2021, doi: [10.3389/fgene.2021.660366](10.3389/fgene.2021.660366)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **metaDIEA**

RNA sequencing has become the standard technique for high resolution genome-wide monitoring of gene expression. As such, it often comprises the first step towards understanding complex mo-lecular mechanisms driving various phenotypes, spanning organ development to disease genesis, monitoring and progression. One of the many advantages of RNA sequencing is its ability to capture complex transcriptomic events such as alternative splicing which results in alternate isoform abundance. At the same time, this advantage still remains algorithmically and computationally challenging, especially with the emergence of even higher resolution technologies such as single-cell RNA sequencing. Although several algorithms have been proposed for the effective detection of differential isoform expression from RNA-Seq data, no widely accepted golden standards have been established. This fact is further compounded by the significant differences in the output of different algorithms when applied on the same data. In addition, many of the proposed algorithms remain scarce and poorly maintained. Driven by these challenges, we developed metaDIEA (meta- Differential Isoform Expression Analysis), a novel integrative ap-proach that effectively combines the top most widely used algorithms for differential transcript and isoform analysis using state-of-the-art Machine Learning techniques. We demonstrate its usability by applying it on simulated data based on several organisms, and using several performance metrics we conclude that our strategy outperforms the application of the individual algorithms. Finally, our approach is implemented as an R Shiny application, with the underlying data analysis pipelines also available as Docker containers.

#### Material
Installation instructions can be found here:
- [github](https://github.com/BiodataAnalysisGroup/metaDIEA)

#### Citation

If you use the tool, please cite the following work:

N. Pechlivanis, A. Togkousidis, M. Tsagiopoulou, S. Sgardelis, I. Kappas, and F. Psomopoulos, “A Computational Framework for Pattern Detection on Unaligned Sequences: An Application on SARS-CoV-2 Data,” Frontiers in Genetics, vol. 12, May 2021, doi: [10.3389/fgene.2021.618170](10.3389/fgene.2021.618170)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **miRkit**

`miRkit` is an open source framework written in R, that allows for the comprehensive analysis of RT-PCR data, from the processing of raw data to a functional analysis of the produced results. The main goal of the proposed tool is to provide an assessment of the samples’ quality, perform data normalization by endogenous and exogenous miRNAs, and facilitate differential and functional enrichment analysis. The tool offers fast execution times with low memory usage, and is freely available under a ΜΙΤ license from https://bio.tools/mirkit. Overall, miRkit offers the full analysis from the raw RT-PCR data to functional analysis of targeted genes, and specifically designed to support the popular miScript miRNA PCR Array (Qiagen) technology.

#### Dependencies
Execute the following lines to install the required packages:
- from CRAN:

```r
install.packages(c("data.table", "tidyverse", "gsubfn", "yaml", "enrichR", "lubridate"))
```

- from Bioconductor:

```r
BiocManager::install(c("naniar", "prada", "ComplexHeatmap", "multiMiR", "limma"))
```


#### Installing
The project can be downloaded using git:
```
git clone https://github.com/BiodataAnalysisGroup/miRkit.git
```

#### Running the project
`miRkit` is a collection of R scripts/functions as listed bellow:

- ```01_miRkit.R```
- ```02a_qc.R``` 
- ```02b_diff_analysis.R```
- ```02c_fa.R```
- ```03a_save_as_pdf.R``` 
- ```03b_save_image.R```

In order to run the project:

1. Set the [R](https://github.com/BiodataAnalysisGroup/miRNAtool/tree/main/R) folder as your working directory
2. Place the required input files inside the `data` directory and set the parameters inside the .yaml file. See instructions [here](https://github.com/BiodataAnalysisGroup/miRNAtool/tree/main/data). 
3. Use the first script which works as a wrapper by calling the required functions:

```r
source("01_miRkit.R")
```

#### Additional scripts
- `initial_script.R`: Contains the full code of the initial version of the project. There is no need to execute this file.

#### Input
- For extra details about the input please move to the `data` [folder](https://github.com/BiodataAnalysisGroup/miRNAtool/tree/main/data) and checkout the correpsonding README.md file.

#### Output
- For extra details about the output please move to the `output` [folder](https://github.com/BiodataAnalysisGroup/miRNAtool/tree/main/output) and checkout the correpsonding README.md file

#### Material
Installation instructions can be found here:
- [github](https://github.com/BiodataAnalysisGroup/miRkit)

#### Citation

If you use the tool, please cite the following work:

M. Tsagiopoulou, A. Togkousidis, N. Pechlivanis, M. C. Maniou, A. Batsali, A. Matheakakis, C. Pontikoglou, and F. Psomopoulos, “miRkit: R Framework Analyzing miRNA PCR Array Data,” BMC Research Notes, vol. 14, no. 376, Sep. 2021, doi: [10.1186/s13104-021-05788-1](10.1186/s13104-021-05788-1)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Goedel numbering**

Evolution consists of distinct stages: cosmological, biological, linguistic. Since biology verges on natural sciences and linguistics, we expect that it shares structures and features from both forms of knowledge. Indeed, in DNA we encounter the biological "atoms", the four nucleotide molecules. At the same time these four nucleotides may be considered as the "letters" of an alphabet. These four "letters", through a genetic code, generate biological "words", "phrases", "sentences" (aminoacids, proteins, cells, living organisms). In this spirit we may consider equally well a DNA strand as a mathematical statement. Inspired by the work of Kurt Gödel, we attach to each DNA strand a Gödel's number, a product of prime numbers raised to appropriate powers. To each DNA chain corresponds a single Gödel's number G, and inversely given a Gödel's number G, we can specify the DNA chain it stands for. Next, considering a single DNA strand composed of N bases, we study the statistical distribution of g, the logarithm of G. Our assumption is that the choice of the m-th term is random and with equal probability for the four possible outcomes. The "experiment", to some extent, appears as throwing N times a four-faces die. Through the moment generating function we obtain the discrete and then the continuum distribution of g. There is an excellent agreement between our formalism and simulated data. At the end we compare our formalism to actual data, to specify the presence of traces of non-random dynamics.

#### Material
Installation instructions can be found here:
- [github](https://github.com/BiodataAnalysisGroup/godel-numbering)

#### Citation

If you use the tool, please cite the following work:

A. Nicolaidis and F. Psomopoulos, “DNA coding and Gödel numbering,” Physica A: Statistical Mechanics and its Applications, vol. 594, p. 127053, 2022, doi: [https://doi.org/10.1016/j.physa.2022.127053]( https://doi.org/10.1016/j.physa.2022.127053)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **kmerAnalyzer**

`kmerAnalyzer` is an alignment-free method capable of processing and counting k-mers in a reasonable time, while evaluating multiple values of the k parameter concurrently. `kmerAnalyzer` was initially implemented in Python 2.7 version, but it seems to work pretty well in Python 3.8 too.

#### Prerequisites

- [`pandas`](https://pandas.pydata.org/getting_started.html) 
- [`numpy`](https://numpy.org/install/)

#### Material
Installation instructions can be found here:
- [github](https://github.com/BiodataAnalysisGroup/kmerAnalyzer)

#### Citation

If you use the tool, please cite the following work:

N. Pechlivanis, A. Togkousidis, M. Tsagiopoulou, S. Sgardelis, I. Kappas, and F. Psomopoulos, “A Computational Framework for Pattern Detection on Unaligned Sequences: An Application on SARS-CoV-2 Data,” Frontiers in Genetics, vol. 12, May 2021, doi: [10.3389/fgene.2021.618170](10.3389/fgene.2021.618170)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **k-taxatree**

`k-taxatree` is a classification workflow written in R, predicting the labels of the first four taxonomic levels (kingdom, phylum, class, order) of metagenomic data with a multi-label Random Forest as the underlying model. The latter accepts as input 6-mer count vectors and as such a method to determine the appropriate k-length was also implemented.

#### Prerequisites

The packages needed to be installed, in order to run the project are:
- from CRAN

```r
install.packages(c("parallel", "data.table", "cluster", "Rfast", "plyr", "caret", "stats", "UBL", "splitstackshape", "mlr", "mldr", "dplyr", "hash", "stringr", "randomForestSRC"))
```


#### Material
Installation instructions can be found here:

- [github](https://github.com/BiodataAnalysisGroup/k-taxatree)

#### Citation

If you use the tool, please cite the following work:

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Odysseus**

`Odysseus` is a versatile high performance framework for optimizing bioinformatics workflow parallelization in hybrid cloud environments.

More specifically, Odysseus is a framework for component-based bioinformatics workflows that aims to optimize parallelization performance, resource allocation and load distribution across heterogeneous computational resources comprising of both cloud-based solutions as well as local HPC infrastructures and general resources. Odysseus attempts to set the core principles of cost efficient parallel processing for large scale bioinformatics workflows by introducing data preprocessing and organization techniques as well as achieving optimal parallelization and resource utilization both across and within the available computational resources.

#### Material
Installation instructions can be found here:

- [github](https://github.com/BiodataAnalysisGroup/odysseys)

#### Citation

If you use the tool, please cite the following work:

A. M. Kintsakis, F. E. Psomopoulos, and P. A. Mitkas, “Reinforcement Learning based scheduling in a workflow management system,” Engineering Applications of Artificial Intelligence, vol. 81, pp. 94–106, 2019, doi: [10.1016/j.engappai.2019.02.013](10.1016/j.engappai.2019.02.013)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **BEEMUS**

#### Overview

`BEEMUS` is a novel method for detecting patterns of co-occuring mutations beyond strain-specific / strain-defining ones and making use of those patterns in an endeavor to group samples in such a way that they could indicate evolutionary paths of the virus. In otherwords, mutational occurrence patterns might suggest different ways of grouping sample revealing the evolutionary history of SARS-CoV-2.

#### Material
Installation instructions can be found here:
- [github](https://github.com/BiodataAnalysisGroup/BEEMUS)

#### Citation

If you use the tool, please cite the following work:
N. Pechlivanis, M. Tsagiopoulou, M. C. Maniou, A. Togkousidis, E. Mouchtaropoulou, S. C. Chassalevris Taxiarchisand Chaintoutis, M. Petala, M. Kostoglou, T. Karapantsios, S. Laidou, E. Vlachonikola, A. Chatzidimitriou, A. Papadopoulos, N. Papaioannou, C. I. Dovas, A. Argiriou, and F. Psomopoulos, “Detecting SARS-CoV-2 lineages and mutational load in municipal wastewater and a use-case in the metropolitan area of Thessaloniki, Greece,” Scientific Reports, vol. 12, no. 1, p. 2659, Feb. 2022, doi: [10.1038/s41598-022-06625-6](10.1038/s41598-022-06625-6).
 
--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **GridCG**

A scalable and modular Grid computing framework for Comparative Genomics.

This projects contains a large-scale data analysis tool, aiming towards similarity detection between
protein sequences, employing the computational resources offered by [EGI](https://www.egi.eu/).

The functionality provided by the tool is currently addressing:

1. Optimization of data management (optimal distribution of data load across nodes).
2. Automatic submission of multiple jobs to the Grid worker nodes.
3. Automatic detection of job failures and resubmission to another node.
4. Visualization of the end results through extensible post processing libraries.
 
The similarity between a given pair of sequences is infered either by a high similarity score 
created by the [BLAST](http://blast.ncbi.nlm.nih.gov/Blast.cgi) tool, and/or by similar phylogenetic profiles constructed using a novel algorithm designed and implemented by the author.

The example folder provides a working scenario for the user to experiment with.
Details about this analysis can be found in the folder's specific README

#### Material
Installation instructions can be found here:

- [github](https://github.com/BiodataAnalysisGroup/GridCG)

#### Citation

If you use the tool, please cite the following work:


--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **BPM**

`BPM` (BLAST - Phylogenetic Profile - MCL) is a distributed modular application for sequence alignment, phylogenetic profiling and clustering of protein sequences, by utilizing the European Grid Infrastructure. Specifically, the application comprises three main components; (a) BLAST alignment (b) construction of phylogenetic profiles based on the produced alignment scores and (c) clustering of entities using the MCL algorithm. These modules have been selected as they represent a common aspect of a vast majority of bionformatics workflows. It is important to note that the modules can be combined independently, and ultimately provide 4 different modes of operation.

#### Material
Installation instructions can be found here:

- [github](https://github.com/BiodataAnalysisGroup/BPM)

#### Citation

If you use the tool, please cite the following work:

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Mutations-Meta-Analyser**

#### Material
Installation instructions can be found here:

- [github](https://github.com/BiodataAnalysisGroup/Mutations-Meta-Analyser)

#### Citation

If you use the tool, please cite the following work:

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **align-paths**

In the wake of gene-oriented data analysis in large-scale bioinformatics studies, focus in research is currently shifting towards the analysis of the functional association of genes, namely the metabolic pathways in which genes participate. The goal of this paper is to attempt to identify the core genes in a specific pathway, based on a user-defined selection of genomes. To this end, a novel algorithm has been developed that uses data from the KEGG database, and through the application of the MCL clustering algorithm, identifies clusters that correspond to different “layers” of genes, either on a phylogenetic or a functional level. The algorithm's complexity, evaluated experimentally, is presented and the results on three characteristic case studies are discussed.

#### Material
Installation instructions can be found here:

- [github](https://github.com/BiodataAnalysisGroup/align-paths)

#### Citation

If you use the tool, please cite the following work:

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **G-Class**

`G-Class` is a Divide and Conquer Application for Grid Protein Classification.

Protein classification has always been one of the major challenges in bioinformatics. Prediction of the functional behavior of proteins is enabled by the presence of motifs in protein chains. The correlation between protein properties and their motifs is not obvious, since multiple motifs may coexist in a protein chain and combined they determine its function. Due to the complexity of this correlation, most data mining algorithms are either non-efficient or time-consuming. One solution to this problem lies in the parallelization of the classification procedure.

GClass is an application implementing a methodology for parallel classification that utilizes grid technologies. First, data are split into multiple sets while preserving the original data distribution. Each one of these data sets is then used to train a separate classification model. Finally, all models are combined to produce the final classification rules, which are used to classify new proteins or test the methodology itself. Experiments have shown a considerable increase in execution speed with no loss in classification accuracy. In fact, there are several experiments where an improvement in accuracy was observed. Moreover, classification rules were extracted from experiments that were previously too memory-demanding to be conducted in one computer. Other internal characteristics, such as classification algorithm independency and data adaptability, along with a user-friendly graphical interface can facilitate usage and adoption of the procedure.

#### Material
Installation instructions can be found here:

- [github](https://github.com/BiodataAnalysisGroup/GClass)

#### Citation

If you use the tool, please cite the following work:

--------------------------------------------------------------------------------------------------------------------------------------------------------------------