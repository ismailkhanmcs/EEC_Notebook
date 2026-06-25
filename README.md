# Emergent Expansion Cosmology (EEC) v8 Notebook

Copyright 2026 Ismail Khan. All rights reserved.

## Description

This Jupyter notebook implements the EEC v8 scale-free model for cosmological analysis. The stiffness is kappa = lambda*rho_m with no characteristic density or exponential cutoff. It uses three free parameters (omega_m, H0, sigma_8) and incorporates data from Pantheon+ supernovae, BOSS DR12 BAO, DESI DR1 BAO, and Planck theta* prior (model-independent, uses BBN omega_b and EEC geometry).

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
    jupyter notebook "Emergent Expansion Cosmology_EEC_Notebook _IsmailKhan.ipynb"
    ```

## Usage

Run the cells in order from 1 to 11:

- **Cell 1**: Setup - Installs libraries and sets up checkpoint directory.
- **Cell 2**: Physical constants - Defines physical constants and fixed quantities (BBN omega_b, Planck theta*).
- **Cell 3**: Pantheon+ data - Downloads and processes supernova data.
- **Cell 4**: BOSS DR12 + DESI DR1 - Loads BAO data.
- **Cell 5**: EEC engine - Defines cosmological functions and growth solver.
- **Cell 6**: Likelihood - Implements combined likelihood function (theta*, SNe, BAO, fsig8).
- **Cell 7**: Checkpoints - Utilities for saving/loading MCMC state and dashboard.
- **Cell 8**: MCMC - Runs burn-in and production sampling.
- **Cell 9**: Results - Displays parameter estimates and derived quantities.
- **Cell 10**: Corner plot - Generates parameter corner plot.
- **Cell 11**: Save - Saves results to files.

## Outputs

- MCMC chains (eec_v8_chain.npy, eec_v8_lp.npy)
- Results summary (eec_v8_results.txt)
- Corner plot (eec_v8_corner.png)
- Console output with best-fit parameters and statistics

## Notes

- The notebook automatically downloads required datasets.
- MCMC sampling may take several hours depending on hardware.
- Checkpoints allow resuming interrupted runs.
- For Google Colab, mount Drive for persistent checkpoints.

## License

Copyright 2026 Ismail Khan. All rights reserved. This notebook is provided for educational and research purposes.