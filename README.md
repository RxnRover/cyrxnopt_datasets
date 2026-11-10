# CyRxnOpt Datasets

[![License](https://img.shields.io/badge/license-CC%20BY--NC%204.0-darkgray)](./LICENSE.txt)
[![Dataset DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22311247.svg)](https://doi.org/10.5281/zenodo.22311247)
[![CyRxnOpt Paper](https://img.shields.io/badge/CyRxnOpt-Paper-green)](https://doi.org/10.1039/d6dd00180g)
[![CyRxnOpt Code](https://img.shields.io/badge/CyRxnOpt-Code-orange)](https://github.com/RxnRover/CyRxnOpt)

Datasets used in the initial benchmarking study for CyRxnOpt ([paper](https://doi.org/10.1039/d6dd00180g); [code](https://github.com/RxnRover/CyRxnOpt)). This repository may be updated in the future to include more datasets used in future studies.

## Repository Structure

Datasets exist as their own subdirectories under `datasets/`, containing one or more CSV files plus a `README.md` providing more detail about dataset collection method, columns, bounds, and optimization objective(s):

```
datasets/
  <dataset_name>/
    README.md
    <YYYYMMDD>_<dataset_name>.csv
```

CSV filenames are prefixed with the date of collection or export (`YYYYMMDD`). A dataset directory may contain more than one CSV file if it reports multiple objectives (like yield and selectivity) measured over the same grid of conditions.

## Dataset CSV Structure

Dataset CSVs follow the following conventions:

- Plain, comma-separated CSV with a single header row
- Each subsequent row is one experimental data point (no missing values)
- Feature/input columns come first, followed by one or more objective/output columns.
- Units may be indicated in the column name or documented in the dataset-specific README.

The exact columns, units, and valid ranges differ per dataset, see the dataset-specific `datasets/<dataset_name>/README.md` for details.

## Initial CyRxnOpt Datasets

To help distinguish future additions from the initial datasets, the following four datasets were used in the initial CyRxnOpt benchmarking paper are listed here:

- [`imine_reduction`](datasets/imine_reduction/README.md)
- [`pk1_paal_knorr_milliporesigma`](datasets/pk1_paal_knorr_milliporesigma/README.md)
- [`pk2_paal_knorr_ames`](datasets/pk2_paal_knorr_ames/README.md)
- [`sugar_isomerization`](datasets/sugar_isomerization/README.md)

## Additional Copyright Notice

This work was produced by Ames National Laboratory under Contract No. DE-AC02-07CH11358 with the U.S. Department of Energy. Publisher acknowledges the U.S. Government license to provide public access under the DOE Public Access Plan: https://www.energy.gov/doe-public-access-plan.
