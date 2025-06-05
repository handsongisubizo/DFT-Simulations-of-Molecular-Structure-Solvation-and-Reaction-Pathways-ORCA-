# O···O Interaction in Water Dimers: Energy Profile

This project analyzes the **non-bonded O···O interaction** between two water molecules using **Density Functional Theory (DFT)** in **ORCA**. The interaction energy was computed as a function of the distance between the **oxygen atoms** of the donor and acceptor water molecules.

---

## Methodology

- **System**: H₂O dimer (1 donor, 1 acceptor)
- **Software**: ORCA for quantum calculations, Python (Colab) for analysis
- **Procedure**:
  - Start from an optimized hydrogen-bonded water dimer geometry.
  - Fix atomic positions and vary the **O···O distance** from 2.00 Å to 5.00 Å in 0.01 Å steps.
  - Perform single-point energy calculations for each configuration.
  - Analyze and visualize the interaction energy profile using Python.

---

## O···O Distance Interaction Behavior

This figure illustrates how the total interaction energy evolves with O···O distance:

- Short distances (≤ 2.4 Å): Strong repulsion due to electron cloud overlap
- Intermediate distances (~2.9–3.1 Å): Attractive hydrogen-bonding interactions dominate
- Long distances (≥ 4.5 Å): Interactions vanish; water molecules behave independently

---

## Energy Profile

The interaction energy curve reveals a **minimum near ~2.901 Å**, representing the **equilibrium O···O distance** in the hydrogen-bonded water dimer. Energies rise steeply at short distances and flatten at long distances.

Full analysis and plots are implemented in a Jupyter notebook (`oo_energy_analysis.ipynb`).

---

## Force Constant Estimation

To estimate the **stiffness** of the O···O interaction near the minimum, a harmonic fit was applied:

    E = (1/2) * k * (x - x₀)²

Results:
- Equilibrium distance x₀ ≈ 2.89 Å
- Force constant k ≈ 18.2 N/m  (example value, replace with fitted result)

This characterizes the flexibility of the hydrogen-bonded dimer.

---

## Repository Structure

sample_orca_files/
    ├── OO_scan_2.89.inp
    └── OO_scan_2.89.out

data_analysis/
    ├── oo_energy_analysis.ipynb

oo_energy_profile.png
oo_distance_plot.png
README.txt

---

**Google Colab notebook**: [Open oo_energy_analysis.ipynb](./oo_energy_analysis.ipynb)

> NOTE: The full dataset includes 3000+ ORCA `.inp`, `.out`, `.gbw`, and density files with 0.01 Å spacing. Only samples and summaries are included here. Full data available upon request.

---

Created by: Handsome Gisubizo
GitHub: https://github.com/handsongisubizo

