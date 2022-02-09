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



