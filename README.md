# CyRxnOpt Datasets

Datasets used in the initial benchmarking study for CyRxnOpt ([paper](https://doi.org/10.26434/chemrxiv.15001645/v1); [code](https://github.com/RxnRover/CyRxnOpt)). This repository may be updated in the future to include more datasets used in future studies.

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
