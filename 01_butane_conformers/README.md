
# Butane Conformer (+180° Dihedral Angle)

This folder contains files related to the +180° conformer of *n*-butane as part of a conformational analysis project using Density Functional Theory (DFT) with ORCA.

## 📁 Contents

- `butane_+180°.xyz` — Geometry of the +180° conformer in XYZ format.
- `input_+180°.inp` — ORCA input file for single-point energy calculation.
- `output_+180°.out` — ORCA output file with SCF energy and job details.
- `butane_scan_visualization.ipynb` — Google Colab notebook that extracts SCF energies and plots the conformational energy profile.

## 🔬 Method Summary

The butane molecule was built in Avogadro, with the central C–C–C–C dihedral angle explicitly defined. A set of conformers was created by varying this angle from –180° to +180°.

Single-point energy calculations were performed using ORCA (no geometry optimization) to isolate energy changes due to torsional rotation. SCF energies were extracted using Python in Google Colab and used to plot the energy profile. Chemcraft was used to verify the dihedral configurations.

## ▶️ How to Use

1. Open the `butane_scan_visualization.ipynb` notebook in [Google Colab](https://colab.research.google.com/).
2. Upload `.out` files from the dihedral scan.
3. Run the notebook to extract angles and SCF energies.
4. View and analyze the conformational energy plot.

## 🔗 Repository Link

Part of the full project:  
[https://github.com/HandsonGis/orca-dft-analysis](https://github.com/HandsonGis/orca-dft-analysis)
