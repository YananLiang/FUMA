# FUMA
Global dynamic material flow model of fossil fuel infrastructure, developed within IMAGE-Materials.
# FUMA: Global Dynamic Fossil Fuel Material Model

FUMA is a Python-based dynamic material flow model that estimates material stocks, inflows and potential end-of-life outflows associated with fossil fuel infrastructure.

Developed within the IMAGE-Materials (IMAGE-MAT) modelling framework, it links IMAGE energy scenarios to the physical infrastructure supporting coal, oil and natural gas supply chains.

## Model scope

The model covers infrastructure for fossil fuel extraction, processing, refining, transport, pipelines and storage.

The archived model focuses on **steel, copper and aluminium**, using inputs from two IMAGE scenarios:

- **SSP2**: baseline pathway
- **SSP2_2D**: climate mitigation pathway

The framework can be extended to other materials and scenarios where suitable input data are available. Potential material outflows represent material becoming available from retired infrastructure; they do not necessarily represent recovered or recycled material.

## Repository structure

| File or folder | Description |
| --- | --- |
| `main.py` | Main model script and scenario selection |
| `attributes/` | Model constants and settings |
| `calculations/` | Infrastructure and material calculation modules |
| `stock_model/` | Dynamic stock modelling routines |
| `mym/` | Reader for IMAGE MYM input files |
| `data/` | Scenario inputs, material intensities and lifetime assumptions |
| `prepare_output_files.py` | Output aggregation functions |
| `README_FUMA_Zenodo.md` | Original documentation accompanying the Zenodo archive |

## Getting started

The original documentation recommends Python 3.8 or later.

Install the required packages:

```bash
python -m pip install numpy pandas scipy matplotlib
```

Before running:

1. Download or clone this repository.
2. Select `SSP2` or `SSP2_2D` using the `scenario` variable in `main.py`.
3. Create an `output` folder in the repository root, with subfolders named `SSP2` and `SSP2_2D`.

Run the model:

```bash
python main.py
```

The archived code contains Windows-style file paths. Running it on Linux or macOS may require path adjustments.

## Model archive and associated publication

The original model package, including precomputed outputs, is available on Zenodo:

**[FUMA model archive](https://zenodo.org/records/17822259)**

The model supports the following publication:

**Liang et al. (2025). _Prospecting urban mines of fossil fuel-based energy systems in the energy transition._ Communications Earth & Environment.**

**[Read the paper](https://doi.org/10.1038/s43247-025-02518-4)**

Please cite the associated publication and acknowledge the archived model when using this work.

## Authors and contributions

Developed by **Yanan Liang** and **Sebastiaan Deetman**, with contributions from **Thije Wubs**.

## Contact

- Yanan Liang: y.liang@cml.leidenuniv.nl
