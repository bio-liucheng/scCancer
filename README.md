# scCancer

## Introduction

The `scCancer` package focuses on processing and analyzing droplet-based scRNA-seq data for cancer research. Except basic data processing steps, this package takes several special considerations for cancer-specific features.

The workflow of  `scCancer` mainly consists of three modules: `scStatistics`, `scAnnotation`, and `scCombination`.
* The `scStatistics` performs basic statistical analyses of raw data and quality control.
* The `scAnnotation` performs functional data analyses and visualizations, such as low dimensional representation, clustering, cell type classification, cell malignancy estimation, cellular phenotype analyses, gene signature analyses, cell-cell interaction analyses, etc.
* The `scCombination` perform multiple samples data integration, batch effect correction and analyses visualization.

After the computational analyses, detailed and graphical reports were generated in user-friendly HTML format.

<img src="http://lifeome.net/software/sccancer/scCancer-workflow.png" width="70%" alt="scCancer-workflow" align=center>

([Click to view larger workflow picture](http://lifeome.net/software/sccancer/scCancer-workflow.png))

          
## System Requirements
* R version: >= 3.5.0


## Installation

Firstly, please install or update the package `devtools` by running 
```R
install.packages("devtools")
```

Then the `scCancer` can be installed via

```R
library(devtools)
devtools::install_github("wguo-research/scCancer")
```

**Hint**: A dependent package `NNLM` was removed from the CRAN repository recently, so an error about it may be reported during the installation. 
If so, you can install a formerly available version manually from its [archive](https://cran.r-project.org/src/contrib/Archive/NNLM/). Besides, if you encounter errors saying package `SoupX` is unavalibale, you can refer to its [GitHub](https://github.com/constantAmateur/SoupX) and install it via
```R
devtools::install_github("constantAmateur/SoupX")
```


## Usage

The vignette of `scCancer` can be found in this [page](http://lifeome.net/software/sccancer/scCancer-vignette.html) or the project [wiki]( https://github.com/wguo-research/scCancer/wiki).

We provide an [example data](http://lifeome.net/software/sccancer/KC-example.tar.gz) of kidney cancer from 10X Genomics, and following are the generated HTML reports:

* [`report-scStat.html`](http://lifeome.net/software/sccancer/KC-example-report-scStat.html)
* [`report-scAnno.html`](http://lifeome.net/software/sccancer/KC-example-report-scAnno.html)

For multi-datasets, following is a generated HTML report for three kidney cancer samples integration analysis:

* [`report-scAnnoComb.html`](http://lifeome.net/software/sccancer/KC123-report-scAnnoComb.html)


## Citation
Please use the following citation:

Wenbo Guo, Dongfang Wang, Shicheng Wang, Yiran Shan, Jin Gu. 2019. bioRxiv doi: https://doi.org/10.1101/800490

## License
GPL-3