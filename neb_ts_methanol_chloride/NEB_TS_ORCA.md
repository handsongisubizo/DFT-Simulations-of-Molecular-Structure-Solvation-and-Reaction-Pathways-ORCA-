## Introduction

Chemical reactions don’t jump from “before” to “after” in one step—they travel along an **energy landscape**. The highest point on that path is the **transition state (TS)**, the moment an old bond is breaking as a new one forms. Identifying the TS gives the **activation barrier** and lets us estimate how fast the reaction runs at room temperature.

 ## **NEB–TS demo (20 s): CH₃OH + HCl → CH₃Cl + H₂O. Click to watch**

[![Watch the video](https://img.youtube.com/vi/_lEphD5_RmY/hqdefault.jpg)](https://www.youtube.com/watch?v=_lEphD5_RmY "Watch on YouTube")

*This NEB clip shows the minimum-energy path; the maximum is the transition state.*

## Methodology

**Map the path:** I used the **nudged elastic band (NEB)** method in **ORCA** to connect optimized **reactant** and **product** structures with **10 intermediate images**. NEB relaxes these images onto the **minimum-energy path (MEP)**.  

**Locate the TS:** The energy profile shows a single peak (Image 5), which is the TS candidate.  

**Validate the TS:** A **vibrational frequency calculation** on that structure yields **one imaginary frequency** along the reaction coordinate—confirming a true **first-order saddle point** (a real TS).  

**Get thermodynamics & rate:** The **activation energy** is the energy gap between the TS and the reactant. Adding zero-point and thermal corrections gives the **Gibbs free energy of activation**, \(\Delta G^{\ddagger}\) (298 K). Using **Eyring’s equation**,
\[
k \;=\; \frac{k_B T}{h}\; e^{-\Delta G^{\ddagger}/(RT)},
\]
I estimated the **rate constant at 298 K**.

## Results

- The NEB curve has a single, smooth maximum at **Image 5**, consistent with a **single-step mechanism**.  
- **TS verification:** one imaginary frequency, aligned with motion along the path → **validated TS**.  
- From the energy profile, I computed **Activation Energy (E‡)** and **\(\Delta G^{\ddagger}\)(298 K)**, then **\(k\)(298 K)** via Eyring.  
  *(Insert your numeric values here once finalized, preferably in kJ·mol⁻¹ and s⁻¹.)*

*Figure X. Minimum-energy path from reactant to product computed by NEB (10 images). The red marker shows the transition state (Image 5). Energies are plotted relative to the reactant.*

## Conclusion

The reaction proceeds over a **single, well-defined barrier** with a **validated TS**.  
With **\(\Delta G^{\ddagger}\)(298 K)** and the **Eyring rate**, we obtain a quantitative estimate of **how fast** the reaction runs at room temperature.  
This **TS-first workflow** is **reproducible** and ready for extension to **solvents** or **alternative pathways**.
