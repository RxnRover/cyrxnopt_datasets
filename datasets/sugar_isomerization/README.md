# Sugar Isomerization Datasets

Experimental reaction datasets for fructose yield and selectivity from a NaX zeolite-catalyzed glucose isomerization reaction, used as one of four real-world benchmarking surfaces in the CyRxnOpt reaction optimization benchmarking study. The reaction is run as batch reactions in a binary γ-valerolactone (GVL)/water solvent system, with reaction mixtures prepared using a high-throughput automated dosing instrument (Chemspeed). The dataset is intended for benchmarking and comparing reaction optimization algorithms on a sharply peaked, multiple-local-optima, single- or multi-objective, continuous optimization problem.

## Dataset Collection

180 data points from a well-distributed grid of temperature, solvent composition, and reaction time.

## File

`20231102_sugar_reaction_yield.csv`

| Column                         | Description                                  | Units |
|--------------------------------|----------------------------------------------|-------|
| `Temperature/oC`               | Reaction temperature                         | °C    |
| `Solvent composition/GVL mol%` | GVL fraction of the binary GVL/water solvent | mol%  |
| `Time/h`                       | Batch reaction time                          | hours |
| `Frutcose yield (%)`           | Fructose yield                               | %     |

A companion file, `20231102_sugar_reaction_selectivity.csv`, reports `Fructose selectivity (%)` over the same grid of conditions and can be used as an alternate or secondary objective.

## Dataset Bounds and Resolution

- `Temperature/oC`: 100-150 °C, in 10 °C steps (6 levels)
- `Solvent composition/GVL mol%`: 0-60 mol% (0, 5, 15, 30, 45, 60 mol%)
- `Time/h`: 1-12 h (1, 2, 4, 8, 12 h)

## Objective

Maximize `Frutcose yield (%)`. The best point in the dataset is f(Temperature/oC, Solvent composition/GVL mol%, Time/h) = f(110, 0, 1) = 25.75%.

Maximize `Frutcose selectivity (%)`. The best point in the dataset is f(Temperature/oC, Solvent composition/GVL mol%, Time/h) = f(100, 0, 1) = 63.32%.

## References

- CyRxnOpt paper: Zachery Crandall, Dulitha P. Kulathunga, Lun An, et al. CyRxnOpt: Generalized Interface for Benchmarking Reaction Optimization Algorithms. *ChemRxiv*. 06 April 2026. DOI: https://doi.org/10.26434/chemrxiv.15001645/v1
- Dataset repository: https://github.com/RxnRover/cyrxnopt_datasets (`datasets/sugar_isomerization/`)
