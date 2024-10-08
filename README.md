# NNP-nonstoichiometric-chromium-sulfides
This repository contains the data and codes utilized in this paper **"Modeling Chemical Exfoliation of Non-van der Waals Chromium Sulfides by Machine Learning Interatomic Potentials and Monte Carlo Simulations"**. For further details, please refer to the published paper [here](https://pubs.acs.org/doi/abs/10.1021/acs.jpcc.3c06168).

## SA.py (Simulated Annealing)

### Overview
`simulated_annealing/SA.py` is a Python script for optimizing vacancy defects in a lattice-based supercell using simulated annealing. It utilizes LAMMPS-MPI with n2p2 NNP for energy calculations and ASE for structural manipulations.

### Features
- Initializes a bulk supercell with random vacancy defects in a certain sublattice.
- Employs cyclic simulated annealing with Monte Carlo atom/vacancy swaps and cell perturbations to identify the ground-state and meta-stable defect distributions.
- Outputs optimized structures and energy metadata for each annealing cycle.

## MC.py (Vacancy Diffusion Monte Carlo Simulation)

### Overview
`MC_vacancy_diffusion/MC.py` performs nearest-neighbor vacancy diffusion Monte Carlo simulations on laterally-strained lattice-based supercells of finite-thickness slabs. It utilizes LAMMPS-MPI with n2p2 NNP for energy minimizations.

### Features
- Initializes a finite-thickness slab supercell with random vacancy defects in a certain sublattice.
- Employs nearest-neighbor vacancy diffusion between vacancies and their nearby atoms, and tracks structural evolution.
- Outputs structure evolution trajectories, inter-layer/intra-layer vacancy migration statistics, energy/force profiles across the simulated slab sample, etc.

## Dependencies
- Python 3.x
- MPI (mpi4py)
- LAMMPS
- ASE (Atomic Simulation Environment)
- NumPy, Pandas, SciPy
- Pymatgen

## Configuration
Modify the input parameters in the scripts to align with your system and simulation settings.

## Modeling Strain-Induced van der Waals Gaps
The following visual illustrates the strain-induced vdW gaps (non-vdW to vdW phase transition) in CrS2 slabs.
<p align="center">
  <img src="https://github.com/user-attachments/assets/24029920-fb02-4b09-953b-4c8d5295e562" width="100%">
</p>



