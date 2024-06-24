```markdown
# LipinskiFilters

**Lipinski Evaluation of Drug Molecules**

## Overview

LipinskiFilters is an R package designed to evaluate drug molecules based on Lipinski's Rule of Five. It provides functions to compute molecular properties, visualize these properties, assess drug-likeness, and predict oral bioavailability.

## Installation

To install the LipinskiFilters package, you can use the following command in R:

```r
# Install from GitHub (assuming the package is hosted on GitHub)
# install.packages("devtools")
devtools::install_github("ocheab/LipinskiFilters")
```

## Usage

To get started with LipinskiFilters, load the package using:

```r
library(LipinskiFilters)
## Loading required package: cowplot
## Loading required package: rcdk
## Loading required package: rcdklibs
## Warning: package 'rcdklibs' was built under R version 4.1.3
## Loading required package: rJava
## Loading required package: ggplot2
```

### Set Working Directory

Set the working directory containing concatenated compounds in SDF format:

```r
file <- system.file("extdata", "test.sdf", package = "LipinskiFilters")
```

### Read SDF Molecules

Read SDF molecules from the specified file:

```r
mols <- load.molecules(file)
```

### Computing Molecular Properties

You can compute molecular properties using the `compute_properties` function. Here’s an example:

```r
properties <- compute_properties(mols)
print(properties)
```

### Creating Lipinski Plots

Visualize Lipinski Rule of Five parameters using the `create_lipinski_plots` function:

```r
create_lipinski_plots(properties)
```

### Druglikeness Evaluation

Evaluate drug-likeness using the `assess_drug_likeness` function:

```r
assess_drug_likeness(properties)
```

### Bioavailability Prediction

Predict oral bioavailability using the `predict_oral_bioavailability` function:

```r
predict_oral_bioavailability(properties)
```

## License

YEAR: 2024
COPYRIGHT HOLDER: George Oche Ambrose

## Contributing

For any issue kindly send to ocheab1@gmail.com

