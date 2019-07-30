# Irish Lab Data Analysis Workflow


## Getting Started

To get started, make sure you have the latest R and RStudio installed.  Then download this repository and open the 00_install_tools.rmd R markdown file in RStudio.  You can then press the green triangle play button on the right to step through each chunk of code.  The first chunk of code will simply print text explaining how to get started installing files.  The second file will list the EULA, which generally indicates that MEM can be used free in a not-profit / academic setting, but must be licensed from Vanderbilt University for any commercial use (http://mem.vueinnovations.com/licensing).  Continuing on, later lines of code will install the various packages used in the workflow examples.

### Prerequisites

Everything needed to install and run the example code is listed in the 00_install_tools.rmd file.  This will include the Bioconductor package and flowCore, which enable reading of Flow Cytometry Standard (FCS) files of single cell data.  Additional packages used in the example scripts include t-SNE, UMAP, and FlowSOM, in addition to MEM.

### Installing

Use 00_install_tools.rmd


## Computational Tools for Single Cell Data

### t-SNE and UMAP

t-SNE and UMAP are tools used for dimensionality reduction and are particularly useful for visualizing high-dimensional datasets. UMAP preserves more of the global structure of the data compared to t-SNE which emphasizes more of the local structure. An advantage of UMAP is its ability to run quickly and scale well for larger datasets. On a t-SNE or UMAP plot in the workflow example included in the repository, each dot represents a single cell that is phenotypically similar to its closest neighboring cells. 

### FlowSOM

FlowSOM is a tool used to create self-organizing maps in order to cluster a given dataset. In our current workflow, we use FlowSOM to cluster on the 2D-space of the t-SNE or UMAP. We have found that clustering on dimensionally reduced space yields more robust and biologically meaningful clusters compared to clustering on the original dimensions of the data set. In the workflow example, FlowSOM will assign a cluster value to each cell (or dot) on the t-SNE or UMAP plot.
 
### MEM

Marker Enrichment Modeling (MEM) is a tool designed to calculate enrichment scores.  MEM generates human and machine readable labels that quantify the features enriched in a sample.  The classic use of MEM is to identify multiple populations of cells and to compare each population to all of the other remaining cells from the original sample.  MEM enrichment scores range from +10 (meaning greatly enriched) through 0 (meaning not enriched) to -10 (meaning greatly lacking).  MEM scores are built form two fundamental statistics, the median and interquartile range, and the output of MEM can be represented as a heatmap of the scores where the rows are each population and the columns are measured features.  This information can also be represented in a compact label where the most enriched features are listed first. MEM will assign an enrichment score to each FlowSOM cluster in the workflow example provided. 



## Authors

* **Kirsten Diggins** - *Version 1.0* 
* **Sierra Barone** - *Versions 2.0 to 3.0* 
* **Jonathan Irish** - *Versions 1.0 to 3.0* 

## License

This project is licensed according to Vanderbilt University policy - see the [LICENSE.MD](LICENSE.MD) file for details
