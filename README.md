# Testing Theory Against Reality  
## A DFT-Based Analysis of Molecular Structure, Solvation, and Reactivity

**Handson Gisubizo**  
**EN.540.658 – Modeling and Design of Sustainable Chemical Processes**  
Johns Hopkins University – Spring 2025

---

###  Project Overview

This project applies **Density Functional Theory (DFT)** using **ORCA 6.0.0** to simulate and analyze:

- Molecular structure and conformational energy (e.g., butane)
- IR spectra and vibrational modes of water clusters
- Thermodynamic behavior of (H₂O)₁₅ across temperatures
- Hydrogen bonding energy and O–H force constants
- Progressive solvation of NaCl with 1–41 water molecules
- Reaction mechanisms via NEB-TS for CH₃OH + HCl → CH₃Cl + H₂O

All computations were post-processed using Python in Google Colab, with structural inputs from **Avogadro** and visualizations in **Chemcraft**.

---

###  Project Structure 

```
orca-dft-analysis/
├── 01_butane_conformers/         # Dihedral scan of butane conformers
├── 02_water_cluster/             # (H₂O)₁₅ geometry and IR spectrum
├── 03_thermo_water/              # Thermodynamic properties of water cluster
├── 04_hbond_dimer/               # Hydrogen bond energy scan
├── 05_oh_bond_force/             # O–H bond force constant calculation
├── 06_nacl_solvation/            # NaCl + water solvation shell analysis
├── 07_neb_ts_methanol/           # NEB-TS for methanol + HCl → CH₃Cl + H₂O
├── report/                       # Final PDF report and notes
│   └── orca_dft_project_report.pdf
└── README.md
```
