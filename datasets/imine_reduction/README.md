# Imine Hydrogenation Dataset

## Overview

Experimental reaction dataset for the heterogeneously catalyzed hydrogenation of an imine, used as one of four real-world benchmarking surfaces in the CyRxnOpt reaction optimization benchmarking study. Pd/C-catalyzed hydrogenation of *N*-1-diphenylethan-1-imine is run in a plug-flow reactor. Three pumps deliver the imine reactant, polymethylhydrosiloxane (PMHS, the hydrogen source), and ethanol (solvent) to the Pd/C bed, with the ethanol pump topping up the total combined flow rate to a constant 0.6 mL/min. The dataset is intended for benchmarking and comparing reaction optimization algorithms on a smooth, low-dimensional, single-objective continuous optimization problem representative of automated flow chemistry.

## Dataset Collection

241 data points collected from a well-distributed grid of three flow rates and the reaction temperature.

## File

`20230907_imine_data.csv`

| Column        | Description                                                                               | Units    |
|---------------|-------------------------------------------------------------------------------------------|----------|
| `Flow 1`      | Reactant pump flow rate (imine or PMHS)                                                   | mL/min   |
| `Flow 2`      | Reactant pump flow rate (imine or PMHS)                                                   | mL/min   |
| `Flow 3`      | Ethanol (solvent) flow rate - dependent variable, set so `Flow 1 + Flow 2 + Flow 3 = 0.6` | mL/min   |
| `Temperature` | Reactor temperature                                                                       | °C       |
| `Yield`       | Product concentration                                                                     | Molarity |

## Dataset Bounds and Resolution

- `Flow 1`: 0.05-0.3 mL/min (0.0625 mL/min steps)
- `Flow 2`: 0.05-0.3 mL/min (0.0625 mL/min steps)
- `Flow 3`: not independently searchable, computed as `0.6 − Flow 1 − Flow 2`, so total flow is held fixed at 0.6 mL/min
- `Temperature`: 10-80 °C (5 °C steps, refined to 2 °C steps between 20-40 °C to resolve the optimum region)

This dataset contains three effective independent dimensions (two flow rates + temperature).

## Objective

Maximize `Yield`. The best point in the dataset is f(Flow 1, Flow 2, Temperature) = f(0.3, 0.3, 30) = 0.1664 M.

## References

- CyRxnOpt paper: Zachery Crandall, Dulitha P. Kulathunga, Lun An, et al. CyRxnOpt: Generalized Interface for Benchmarking Reaction Optimization Algorithms. *ChemRxiv*. 06 April 2026. DOI: https://doi.org/10.26434/chemrxiv.15001645/v1
- Dataset repository: https://github.com/RxnRover/cyrxnopt_datasets (`datasets/imine_reduction/`)
