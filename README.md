# Emergent Expansion Cosmology (EEC) v5 Notebook

Copyright 2026 Ismail Khan. All rights reserved.

## Description

This Jupyter notebook implements the EEC v5 model for cosmological analysis, deriving Omega_c from the peak halo formation rate at z_halo = 1.1. It uses three free parameters (omega_m, H0, sigma_8) and incorporates data from Pantheon+ supernovae, BOSS DR12 BAO, DESI DR1 BAO, and Planck omega_m prior.

## Requirements

- Python 3.x
- Jupyter Notebook or JupyterLab
- Required libraries: numpy, scipy, emcee, corner, matplotlib

## Setup

1. Install dependencies:
   ```bash
   pip install emcee corner numpy scipy matplotlib
   ```

2. Open the notebook in Jupyter:
   ```bash
   jupyter notebook Emergent_Expansion_Cosmology_EEC_Notebook_by_Ismail_Khan.ipynb
   ```

## Usage

Run the cells in order from 1 to 12:

- **Cell 1**: Setup - Installs libraries and sets up checkpoint directory.
- **Cell 2**: Constants - Defines physical constants and halo formation parameters.
- **Cell 3**: Pantheon+ data - Downloads and processes supernova data.
- **Cell 4**: BOSS DR12 + DESI DR1 - Loads BAO data.
- **Cell 5**: Configuration - Sets MCMC parameters.
- **Cell 6**: EEC engine - Defines cosmological functions.
- **Cell 7**: Likelihood - Implements combined likelihood function.
- **Cell 8**: Checkpoints - Utilities for saving/loading MCMC state.
- **Cell 9**: MCMC - Runs burn-in and production sampling.
- **Cell 10**: Results - Displays parameter estimates and derived quantities.
- **Cell 11**: Corner plot - Generates parameter corner plot.
- **Cell 12**: Save - Saves results to files.

## Outputs

- MCMC chains (eec_v5_fp_chain.npy, eec_v5_fp_lp.npy)
- Results summary (eec_v5_fp_results.txt)
- Corner plot (eec_v5_fp_corner.png)
- Console output with best-fit parameters and statistics

## Notes

- The notebook automatically downloads required datasets.
- MCMC sampling may take several hours depending on hardware.
- Checkpoints allow resuming interrupted runs.
- For Google Colab, mount Drive for persistent checkpoints.

## License

Copyright 2026 Ismail Khan. All rights reserved. This notebook is provided for educational and research purposes.