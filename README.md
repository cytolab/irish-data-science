# MEM

Marker Enrichment Modeling (MEM) is a tool designed to calculate enrichment scores.  MEM generates human and machine readable labels that quantify the features enriched in a sample.  The classic use of MEM is to identify multiple populations of cells and to compare each population to all of the other remaining cells from the original sample.  MEM enrichment scores range from +10 (meaning greatly enriched) through 0 (meaning not enriched) to -10 (meaning greatly lacking).  MEM scores are built form two fundamental statistics, the median and interquartile range, and the output of MEM can be represented as a heatmap of the scores where the rows are each population and the columns are measured features.  This information can also be represented in a compact label where the most enriched features are listed first.

## Getting Started

MEM was designed for biology users who may not have much experience in R, and this code base has and install script and example scripts showing different uses of MEM with three example datasets.  These instructions will focus on helping biologist users.  

To get started, make sure you have the latest R and RStudio installed.  Then download this repository and open the 00_install_tools.rmd R markdown file in RStudio.  You can then press the green triangle play button on the right to step through each chunk of code.  The first chunk of code will simply print text explaining how to get started installing files.  The second file will list the EULA, which generally indicates that MEM can be used free in a not-profit / academic setting, but must be licensed from Vanderbilt University for any commercial use (http://mem.vueinnovations.com/licensing).  Continuing on, later lines of code will install the various packages used in the MEM examples.

Experts may wish to skip all this and simply install MEM and test out the vignettes within it.  This is fine, but half the fun is in how MEM can compare the results of different analysis strategies for the same dataset, so we recommend clicking through the examples (or knitting them).

### Prerequisites

Everything needed to install and run the example code is listed in the 00_install_tools.rmd file.  This will include the Bioconductor package and flowCore, which enable reading of Flow Cytometry Standard (FCS) files of single cell data.  Additional packages used in the example scripts include FlowSOM, t-SNE, and UMAP, in addition to MEM.

### Installing

Use 00_install_tools.rmd

## Authors

* **Kirsten Diggins** - *Version 1.0* 
* **Sierra Barone** - *Versions 2.0 to 3.0* 
* **Jonathan Irish** - *Versions 1.0 to 3.0* 

## License

This project is licensed according to Vanderbilt University policy - see the [LICENSE.MD](LICENSE.MD) file for details
