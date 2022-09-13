---
title: Our software activities
description: Listing our packages here
background: /assets/img/groupLogo/coding.jpg
permalink: /software/
---

## Software 

![Software](/assets/img/software/computer-engineering-logo.png){: .rounded .float-left width="100px"}

<br/>

{: .clearfix}
<br>

# **lineagespot**
![lineagespot](/assets/img/software/lineagespotlogo.png){: .rounded .float-left width="100px"}

Lineagespot is a [Bioconductor](http://bioconductor.org) package
written in [R](https://www.r-project.org/), and aims to identify 
SARS-CoV-2 related mutations based on a single (or a list) of variant(s) 
file(s) (i.e., [variant calling format](https://gatk.broadinstitute.org/hc/en-us/articles/360035531692-VCF-Variant-Call-Format)). 

### Installation

```r
# install.packages("devtools")
devtools::install_github("BiodataAnalysisGroup/lineagespot")
```

### Raw data analysis

The processing steps of the raw fastq files can be found [here](inst/scripts/raw-data-analysis.md).

**Material**
- [github](https://github.com/BiodataAnalysisGroup/lineagespot)

### Citation

If you use the tool, please cite the following work:

Nikolaos Pechlivanis, Maria Tsagiopoulou, Maria Christina Maniou, Anastasis Togkousidis, Evangelia Mouchtaropoulou, Taxiarchis Chassalevris, Serafeim Chaintoutis, Chrysostomos Dovas, Maria Petala, Margaritis Kostoglou, Thodoris Karapantsios, Stamatia Laidou, Elisavet Vlachonikola, Anastasia Chatzidimitriou, Agis Papadopoulos, Nikolaos Papaioannou, Anagnostis Argiriou, Fotis Psomopoulos, "_Detecting SARS-CoV-2 lineages and mutational load in municipal wastewater; a use-case in the metropolitan area of Thessaloniki, Greece_", medRxiv 2021.03.17.21252673; doi: [https://doi.org/10.1101/2021.03.17.21252673](https://doi.org/10.1101/2021.03.17.21252673)


# **tripr**
![tripr](/assets/img/software/tripr.png){: .rounded .float-left width="100px"}


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

### Installation

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


### Launching the app

Once `tripr` is successfully installed, it can be loaded as follow:

``` r
library(tripr)
```
**Material**
- [github](https://github.com/BiodataAnalysisGroup/tripr)


# **IgIDivA**


### Overview

`IgIDivA` (Immunoglobulin Intraclonal Diversification Analysis) is a purpose-built tool for the analysis of the intraclonal diversification process using high-throughput sequencing data. It is written in [shiny](https://shiny.rstudio.com/). Every step of the analysis can be performed interactively, thus not requiring any programming skills. It takes as input the output files "clonotypes_computation" and "grouped_alignment_nt" from the [`tripr`](https://bio.tools/TRIP_-_T-cell_Receptor_Immunoglobulin_Profiler) package.  
Functions for an `R` command-line use are also available.  
The UserGuide of IgIDivA can be found [here](https://rpubs.com/laura_zara/911248) and an example dataset to be used as Input of IgIDivA can be found [here](https://doi.org/10.5281/zenodo.6616046).



### Installation
The `IgIDivA` scripts can be freely downloaded [here](https://github.com/laurazara/IgIDivA).
It requires `R` (version "4.1"), which can be installed on any operating system from [CRAN](https://cran.r-project.org/). `IgIDivA` has been successfully tested in Windows 10, macOS 10.15 and Linux WSL.
All the packages that need to be installed in your `R` session are the following:

```r
install.packages("shiny")
install.packages("shinyFiles")
install.packages("fs")
install.packages("pdftools")
install.packages("purrr")
install.packages("DT")
install.packages("bslib")
install.packages("shinyhelper")
install.packages("data.table")
install.packages("stringr")
install.packages("RGenetics")
install.packages("dplyr")
install.packages("ggsci")
install.packages("tidygraph")
install.packages("ggraph")
install.packages("igraph")
install.packages("ggplot2")
install.packages("ggpubr")
install.packages("rstatix")
install.packages("shinyvalidate")

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







# **UMIc**

UMIc is a framework, written in [R](https://www.r-project.org/), implementing a new proposed method for UMI deduplication and reads correction. The method works at nucleotide level, taking into account the frequency and the mean quality of each base. 

### Getting started

### Prerequisites

The packages needed to be installed, in order to run the project are:
- from CRAN

```
install.packages(c("tidyverse", "data.table", "stringdist", "pryr"))
```

- from Bioconductor
```
BiocManager::install(c("Biostrings", "ShortRead"))
```

### Installing

The project can be downloaded using git:

```
git clone https://github.com/BiodataAnalysisGroup/UMIc
```

### Running the project

The framework consists of three scripts:
- ```UMIsProject.R``` 
- ```casesWorkflows.R```
- ```functions.R```

In order to run the project, set the [R](https://github.com/BiodataAnalysisGroup/UMIc/tree/master/R) folder as your working directory, set the input parameters in the main script ```UMIsProject.R``` and then use the following command:
```
source("UMIsProject.R")
```

The project provides example input datasets and their outputs, for testing purposes. The folder [data](https://github.com/BiodataAnalysisGroup/UMIc/tree/master/data) includes example datasets for all three scenarios in their corresponding subfolders. Each subfolder icludes the fastq files and a Readme.md file with the parameter values, used to generate the files in folder [outputs](https://github.com/BiodataAnalysisGroup/UMIc/tree/master/outputs). The user must provide the input and output folders' filepaths. 

### Inputs
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


### Outputs 
The output data are stored also in fastq files, named the same as the input files with an added ```_corrected``` suffix and the name of the folder can be provided by the user. The files contain the corrected sequences (without the UMI) and their quality. It is worth mentioning that the new sequence ID is constructed by combining the ID of one of the input sequences, that has that same UMI, and the UMI itself.

The framework also produces a csv file with all the information of the output fastq files and extra information, that can help return from the output sequences to their corresponding input sequences. The file is named the same as the Read1 fastq file with an added ```_summary_table``` suffix.

For more details, please refer to the [wiki](https://github.com/BiodataAnalysisGroup/UMIc/wiki).



