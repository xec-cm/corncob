# corncob <img src="man/figures/logo.png" align="right" width="165px"/>
Count Regression for Correlated Observations with the Beta-binomial

`corncob` is an `R` package for modeling relative abundance and testing hypotheses about the effect of covariates on relative abundance. The `corncob` methodology was specifically developed for modelling microbial abundances based on high throughput sequencing data, such as 16S or whole-genome sequencing.

<!-- badges: start -->
[![R-CMD-check](https://github.com/statdivlab/CORNCOB/workflows/R-CMD-check/badge.svg)](https://github.com/statdivlab/CORNCOB/actions)
[![codecov](https://codecov.io/github/statdivlab/corncob/coverage.svg?branch=main)](https://app.codecov.io/github/statdivlab/corncob)
[![Docker Repository on Quay](https://quay.io/repository/fhcrc-microbiome/corncob/status "Docker Repository on Quay")](https://quay.io/repository/fhcrc-microbiome/corncob)
[![R-CMD-check](https://github.com/xec-cm/corncob/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/xec-cm/corncob/actions/workflows/R-CMD-check.yaml)
<!-- badges: end -->


## Installation

To install the `corncob` package, use the code below to download the development version from Github.

``` r
# install.packages("remotes")
remotes::install_github("statdivlab/corncob")
library(corncob)
```

## Docker

Instead of installing corncob to your local system, you can use corncob via the pre-compiled Docker image: `quay.io/fhcrc-microbiome/corncob`.


## Use

The vignette demonstrates example usage of all main functions. Please [file an issue](https://github.com/statdivlab/corncob/issues) if you have a request for a tutorial that is not currently included. You can see the vignette by using the following code:


``` r
library(corncob)
# Use this to view the vignette in the corncob HTML help
help(package = "corncob", help_type = "html")
# Use this to view the vignette as an isolated HTML file
utils::browseVignettes(package = "corncob")
```

Note that R does not allow variable names to start with numbers. Sometimes, when going directly from QIIME2 to phyloseq objects, taxa names will be a large string starting with numbers. To clean these taxa names for use with corncob, use  `clean_taxa_names(my_phyloseq_object)`, see `?clean_taxa_names` for details.

## Documentation 

We additionally have a `pkgdown` [website](https://statdivlab.github.io/corncob/) that contains pre-built versions of our function [documentation](https://statdivlab.github.io/corncob/reference/index.html) and [vignette](https://statdivlab.github.io/corncob/articles/corncob-intro.html). 

## Citation

If you use `corncob` for your analysis, please cite our manuscript:

Bryan D. Martin, Daniela Witten, and Amy D. Willis. (2020). [*Modeling microbial abundances and dysbiosis with beta-binomial regression*.](https://projecteuclid.org/euclid.aoas/1587002666) Annals of Applied Statistics, Volume 14, Number 1, pages 94-115.

An open-access preprint is available on arXiv [here](https://arxiv.org/abs/1902.02776).

## Bug Reports / Change Requests

If you encounter a bug or would like make a change request, please file it as an issue [here](https://github.com/statdivlab/corncob/issues).
