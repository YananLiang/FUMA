
# FUMA: global dynamic fossil fuel material model (v1)

This repository contains the Python model developed for the paper:

> "Prospecting urban mines of fossil fuel-based energy systems in the energy transition"  
> Authors: Yanan Liang, Sebastiaan Deetman, with input from Thije Wubs  
> [Published on Communications Earth & Environment]

## Overview

FUMA estimates the material stocks and potential outflows embedded in decommissioned fossil fuel infrastructure (coal, oil, gas) using dynamic stock modeling and scenario-based fossil fuel demand from IMAGE SSP scenarios. FUMA is one of the dynamic MFA modules attached to the IMAGE model used to support climate policies. These models are summarized as IMAGE-MAT, use socio-economic and technological information from the IMAGE model and translate that in several steps to material flows and stocks. 

This model currently calculates results for **steel**, **copper**, and **aluminium**, based on scenario inputs from **IMAGE SSP2 baseline** and **SSP2-2D** pathways. However, it is open for extension to additional materials and alternative SSPs, provided that the necessary input data (e.g., demand, material intensities, lifetimes) are available.


## Folder Structure

```
FUMA_Zenodo/
├── main.py                  # Entry point script with dynamic working directory
├── README.md                # This file
├── calculations/            # Modules for pipeline, transport, extraction, etc.
├── stock_model/             # Inflow-outflow model components
├── data/                    # Input datasets
│   └── material_intensity/  # Material intensity data in CSV format
├── output/                  # Output folder for results
│   └── SSP2_2D/             # Scenario-specific output
```

## How to Run

1. Make sure you have Python 3.8+ installed.
2. Install required packages: `pandas`, `numpy`, `matplotlib`, `scipy`
3. Place the input data files in the `data/` subfolder (see paper or documentation for file descriptions).
4. Run the model:

```bash
cd FUMA_Zenodo
python main.py
```

This script automatically sets the working directory to the folder it's in, so no hardcoded paths are required.

## Notes

- All file paths use `pathlib.Path` for OS compatibility.
- Data files must be placed in the correct folders (`data/`, `data/material_intensity/`).
- Outputs are written to `output/SSP2_2D/`.

## License

MIT License

## Contact

- Yanan Liang – y.liang@cml.leidenuniv.nl
- Sebastiaan Deetman – deetman@cml.leidenuniv.nl
