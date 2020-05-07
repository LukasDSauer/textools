
<!-- README.md is generated from README.Rmd. -->

[![Build
Status](https://travis-ci.org/lbau7/textools.svg?branch=master)](https://travis-ci.org/lbau7/textools)

# textools

textools create nice looking LaTeX tables.

## Installation

``` r
# install.packages("devtools")
devtools::install_github("lbau7/textools")
```

## Usage

The main function of textools is `texmod` which creates LaTeX tables for
the regression output of various models.

``` r
library(textools)

iris.lm <- lm(Sepal.Length ~ Sepal.Width + Petal.Width + Species, data = iris)
texmod(iris.lm,
  title = "Linear Model for Sepal Length",
  rowlabs = c("Sepal Width", "Petal Width", "Species (versicolor)",
    "Species (setosa)", "Species (virginica)")
)
```
