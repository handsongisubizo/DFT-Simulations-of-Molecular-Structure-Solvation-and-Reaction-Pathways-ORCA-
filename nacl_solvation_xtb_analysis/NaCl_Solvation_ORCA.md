<h2>Why this study</h2>
<p><strong>Question.</strong> How does stabilization build as water surrounds an NaCl ion pair—and when are hydration shells essentially complete?</p>

 ## **Watch stabilization grow (NaCl + H₂O) steps here**:

[![Watch the video](https://img.youtube.com/vi/_lEphD5_RmY/hqdefault.jpg)](https://www.youtube.com/watch?v=_lEphD5_RmY "Watch on YouTube")


## Solvation of NaCl with Water Molecules (ORCA + xTB + ALPB)

A **hybrid solvation** approach was used to study the progressive hydration of a neutral **NaCl ion pair**. The system was solvated with **1–41 explicitly placed water molecules**, and each configuration was **geometry‑optimized**. To capture long‑range bulk effects, the **ALPB (Analytical Linearized Poisson–Boltzmann)** implicit solvent model for water was applied **alongside the explicit molecules**. Calculations were performed in **ORCA** using the **xTB (GFN2‑xTB)** semiempirical Hamiltonian, which balances computational efficiency and accuracy for larger molecular systems. The number of explicit solvent molecules was controlled via the **%solvator** block in ORCA. Post‑processing and visualization were done in **Python** (Google Colab).

## Methodology

- **System sizes:** NaCl solvated by *n* water molecules, with *n* = 1…41.  
- **Level of theory:** xTB (GFN2‑xTB) in ORCA; implicit solvent **ALPB (water)**.  
- **Optimization:** Full geometry optimization for each *n*.  
- **Incremental stabilization metric**

  $$\Delta E_n = E(\mathrm{NaCl}\cdot n\,\mathrm{H_2O}) - E(\mathrm{NaCl}\cdot (n-1)\,\mathrm{H_2O}) - E(\mathrm{H_2O})$$

  Negative $\Delta E_n$ means the added water further stabilizes the complex.

- **Analysis:** Extract $\Delta E_n$ and plot it vs. $n$ to reveal stabilization trends and hydration-shell completion.




## Results — Stabilization Behavior During NaCl Solvation

> 
![NaCl Hydration Snapshots (n = 1, 15, 30, 41)](nacl_hydration_snapshots.png)
>
> *Figure.* Snapshots ($n = 1, 15, 30, 41$). Panels show how solvation builds around the ion pair (Na⁺ = green, Cl⁻ = magenta; dotted lines = H-bonds).

- **n = 1:** Bare ion pair with a single water—no network yet.  
- **n ≈ 15:** First hydration shell largely formed: water oxygens point toward Na⁺; hydrogens toward Cl⁻; several bridging waters connect the ions.  
- **n ≈ 30:** Second shell growing; more continuous H-bond network; interior appears saturated.  
- **n ≈ 41:** Compact, quasi-spherical two-shell cluster; added waters mainly reinforce the outer network, so incremental stabilization diminishes (small $\Delta E_n$).


![Total Energy vs Iteration (Hartree)](total_energy_vs_iteration.png)
>
> *Figure.* Total electronic energy, $E$ (Hartree), of $\mathrm{NaCl}\!\cdot\! n\,\mathrm{H_2O}$ vs. iteration ($n=1\ldots41$).
>

The curve goes down (more negative) almost perfectly in a straight line.
which means each extra water contributes about the same amount of energy: its own internal energy plus a similar interaction with the rest.

> 
![Energy Change vs Iteration](nacl_solvation_stabilization.png)

The incremental interaction energy $\Delta E_n$ was monitored as water molecules were sequentially added to the NaCl ion pair. The profile shows an **overall trend toward stabilization**, with the **largest energy drop** occurring after the **second water molecule**, suggesting strong initial ion–solvent interactions. As additional water molecules are added, the **energy changes fluctuate around zero**, indicating **reduced incremental stabilization** and the **progressive saturation of the first hydration shell**.

> *Figure.* Incremental stabilization energy, $\Delta E_n$ (kcal·mol$^{-1}$), per added water molecule during NaCl hydration. The dashed line at $\Delta E_n = 0$ marks the no-stabilization baseline. *(Replace the placeholder below with your plot path.)*
> 
## Conclusion

- The NaCl ion pair stabilizes rapidly with the **first few waters**, dominated by strong ion–dipole interactions.  
- Beyond the initial additions, **\(\Delta E\)** fluctuates near zero, consistent with **hydration‑shell completion** and the onset of **bulk‑like behavior**.  
- This **hybrid explicit–implicit** protocol (xTB + ALPB in ORCA) provides a **computationally efficient** pathway to map solvation growth while retaining key physical trends.


##  Links
-  **GitHub profile**: [HandsonGisubizo](https://github.com/handsongisubizo) please make give me my markdown withgout changing anything at all for my github
