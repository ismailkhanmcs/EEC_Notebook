# Emergent Expansion Cosmology (EEC) v10 Notebook

Copyright 2026 Ismail Khan. All rights reserved.

## Description

This Jupyter notebook implements the EEC v10 scale-free model for cosmological analysis. The stiffness is kappa = beta*rho_m with no characteristic density or exponential cutoff. It uses three free parameters (omega_m, H0, sigma_8) and incorporates data from Pantheon+ supernovae, BOSS DR12 BAO, DESI DR1 BAO, and Planck theta* prior (model-independent, uses BBN omega_b and EEC geometry).

**v10 (new):** adds the exact late-time attractor cell (f\* = (√73−1)/12, w\* = (1−√73)/9, q\* = 2/3−√73/6; H → 0, Ω_neq → 1), computed with the full self-consistent engine extended past a = 1. Also includes equation-of-state analysis (w_eff(z) and CPL-equivalent w0, wa). Fit, datasets, and all v8/v9 numerical results unchanged.

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

Run the cells in order:

- **Cell 1**: Setup - Installs libraries and sets up checkpoint directory (EEC_V10).
- **Cell 2**: Physical constants - Defines physical constants and fixed quantities (BBN omega_b, Planck theta*).
- **Cell 3**: Pantheon+ data - Downloads and processes supernova data.
- **Cell 4**: BOSS DR12 + DESI DR1 - Loads BAO data.
- **Cell 5**: EEC engine - Defines cosmological functions and growth solver.
- **Cell 6**: Likelihood - Implements combined likelihood function (theta*, SNe, BAO, fsig8).
- **Cell 7**: Checkpoints - Utilities for saving/loading MCMC state and dashboard.
- **Cell 8**: MCMC - Runs burn-in and production sampling.
- **Cell 9**: Results - Displays parameter estimates, derived quantities, and tension analysis.
- **Cell 10**: Equation of state - Computes w_eff(z) and CPL-equivalent (w0, wa) parameters.
- **Cell 11**: Late-time attractor - Full self-consistent engine extended past a=1, verifying the exact fixed point.
- **Cell 12**: Corner plot - Generates parameter corner plot.
- **Cell 13**: Save - Saves results to files.

## Outputs

- MCMC chains (eec_v10_chain.npy, eec_v10_lp.npy)
- Results summary (eec_v10_results.txt)
- Corner plot (eec_v10_corner.png)
- Console output with best-fit parameters, chi2 decomposition, tension summary, attractor verification, and equation-of-state values

## Notes

- The notebook automatically downloads required datasets.
- MCMC sampling may take several hours depending on hardware.
- Checkpoints allow resuming interrupted runs.
- For Google Colab, mount Drive for persistent checkpoints.
- v10 adds the exact late-time attractor analysis and equation-of-state computation (cells 10-11).

## License

Copyright 2026 Ismail Khan. All rights reserved. This notebook is provided for educational and research purposes.