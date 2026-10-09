# Thermal Properties of MOF MIRO-101

Data and simulation inputs accompanying:

> Gastón A. González, M. González, R. Blukis, C. Kränkel, Juan M. García-Garfido, F. Herrera, "Understanding Thermal Conductivity in Metal-Organic Framework MIRO-101"

This repository contains the crystal structure of MIRO-101, the classical (LAMMPS) and first-principles (Quantum ESPRESSO, Phonopy, Phono3py) simulation inputs used to compute its thermal properties, and the tabulated data behind each figure of the manuscript (heat capacity, thermal conductivity, phonon dispersion/PDOS and spectral conductivity).

## Repository structure
- `Miro-101.cif` — crystal structure of MIRO-101
- `Simulations/`
  - `LAMMPS/EMD/` — equilibrium MD inputs and data files (UFF and UFF4MOF force fields)
  - `LAMMPS/NEMD/` — non-equilibrium MD inputs and supercell data files (35×3×3 and 3×3×35)
  - `DFT/QE/` — Quantum ESPRESSO workflows: `DFT Convergence Tests/`, `Relax/`, `Phonopy/`, `Phono3py/`, `pseudo/`
- `Figures/` — tabulated data underlying each manuscript figure
  - `Fig1-TGA-CV/` — TGA and heat capacity (DFT and experimental)
  - `Fig3-kappa/` — thermal conductivity vs. temperature (DFT, EMD, NEMD, experiment)
  - `Fig4-Dispersion-PDOS/` — phonon DOS, including the Zn–tetrazolate node
  - `Fig5-K_vs_Freq/` — thermal conductivity vs. frequency

## Requirements (simulations)
- LAMMPS ≥ 2Aug2023
- Quantum ESPRESSO ≥ 7.2
- Phonopy ≥ 2.21 / Phono3py ≥ 2.8
- lammps-interface
- Python ≥ 3.10: numpy, scipy, ase, pymatgen

## Contact
Gastón A. González 
email: gaston.gonzalez@usach.cl

