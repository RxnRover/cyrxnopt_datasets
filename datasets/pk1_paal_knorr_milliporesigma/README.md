# PK1 - Paal-Knorr Reaction Dataset (Transient Flow)

## Overview

Experimental reaction dataset for a Paal-Knorr reaction, collected via a transient flow study, used as one of four real-world benchmarking surfaces in the CyRxnOpt reaction optimization benchmarking study. Conditions were explored via a transient flow method in which residence time was continuously ramped rather than held at discrete steady-state points, at multiple fixed temperatures. The dataset is intended for benchmarking and comparing reaction optimization algorithms on a smooth, single-objective, continuous optimization problem with dense data coverage.

## Dataset Collection

1,708 data points collected via a transient flow study with continuously ramped residence time at each of 5 fixed temperatures, considerably denser than the other three reaction datasets.

## File

`20230927_pk1_paal_knorr_milliporesigma.csv`

| Column         | Description          | Units   |
|----------------|----------------------|---------|
| `τ [min]`      | Residence time       | minutes |
| `Temp [°C]`    | Reaction temperature | °C      |
| `Conversion %` | Reaction conversion  | %       |

## Dataset Bounds and Resolution

- `τ [min]`: ramped from 0.5 to 15 min at a ramp rate of 0.5 min/min (observed data range approximately 1.25-14.0 min), effectively near-continuous due to the transient collection method
- `Temp [°C]`: 5 discrete levels (24.7, 34.7, 44.5, 59.2, and 74.0 °C)

## Objective

Maximize `Conversion %`. The best point in the dataset is f(τ [min], Temp [°C]) = f(12.946, 74.0) = 65.31%.

## References

- CyRxnOpt paper: Zachery Crandall, Dulitha P. Kulathunga, Lun An, et al. CyRxnOpt: Generalized Interface for Benchmarking Reaction Optimization Algorithms. *ChemRxiv*. 06 April 2026. DOI: https://doi.org/10.26434/chemrxiv.15001645/v1
- Dataset repository: https://github.com/RxnRover/cyrxnopt_datasets (`datasets/pk1_paal_knorr_milliporesigma/`)
