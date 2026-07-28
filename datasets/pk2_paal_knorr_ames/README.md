# PK2 - Paal-Knorr Reaction Dataset (Steady-State, Continuous Flow)

## Overview

Experimental reaction dataset for a Paal-Knorr reaction, collected via a continuous, steady-state flow method, used as one of four real-world benchmarking surfaces in the CyRxnOpt reaction optimization benchmarking study. Each set of reaction conditions was allowed to reach equilibrium before the result was measured. The dataset is intended for benchmarking and comparing reaction optimization algorithms on a rugged, sparsely sampled, multiple-local-optima, single-objective, continuous optimization problem, contrasting the PK1 dataset for a similar reaction class.

## Dataset Collection

224 data points collected on a 3D grid of temperature, concentration, and residence time.

## File

`20240205_pk2_paal_knorr_ames.csv`

| Column           | Description            | Units   |
|------------------|------------------------|---------|
| `Temperature`    | Reaction temperature   | °C      |
| `conc.`          | Reactant concentration | mol/L   |
| `residence time` | Residence time         | minutes |
| `conversion`     | Reaction conversion    | %       |

## Dataset Bounds and Resolution

- `Temperature`: 30-90 °C (15 °C steps)
- `conc.`: 0.05-0.5 mol/L
- `residence time`: 1-13.3 min

## Objective

Maximize `conversion`. The best point in the dataset is f(Temperature, conc., residence time) = f(90, 0.5, 12.5) = 62.92%.

**Note**: A small number of `conversion` values are slightly negative, reflecting measurement noise near zero conversion rather than a physically negative conversion.

## References

- CyRxnOpt paper: Zachery Crandall, Dulitha P. Kulathunga, Lun An, et al. CyRxnOpt: Generalized Interface for Benchmarking Reaction Optimization Algorithms. *ChemRxiv*. 06 April 2026. DOI: https://doi.org/10.26434/chemrxiv.15001645/v1
- Dataset repository: https://github.com/RxnRover/cyrxnopt_datasets (`datasets/pk2_paal_knorr_ames/`)
