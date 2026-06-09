# Electric Go-Kart Chassis Design & Structural Optimization 🏎️⚡

This repository contains the conceptual design, mechanical engineering calculations, and Finite Element Analysis (FEA) of a handling-oriented electric go-kart chassis. 

![Chassis Assembly](Results_and_Images/completeimage3.JPG)

![Chassis Assembly](Results_and_Images/chassicimage2.JPG)

## 🎯 Project Overview
Unlike standard automobiles, go-karts lack a suspension system. This requires the chassis itself to act as the suspension. This project focuses on optimizing the torsional rigidity of the chassis to successfully achieve the **"jacking effect"** (lifting the inner rear wheel during cornering) to prevent understeer, effectively compensating for the added weight of an EV battery pack.

## ⚙️ Technical Specifications
* **Chassis Material:** S355 Structural Steel Tubing (32x2mm for main rails, 25x2mm for supports)
* **Powertrain:** 1.7 kW 48V Brushless DC (BLDC) Motor
* **Energy Storage:** 14S10P Li-Ion Battery Pack (18650 NMC cells, ~1.5 kWh) managed by a 60A BMS
* **Top Speed:** ~60 km/h (Optimized via 3.69 gear ratio)
* **Wheelbase / Track Width:** 1160 mm / 1400 mm

## 🔬 Engineering Methodology & Analysis
All design and simulation phases were executed using **SolidWorks 2024**. The engineering workflow includes:

1. **Vehicle Dynamics:** Quasi-Static Load Transfer calculations to determine cornering forces and theoretical load shifts.
2. **Global FEA (Beam Elements):** Initial displacement and rigidity tests under dynamic cornering loads (up to 550N lateral shock).
3. **Sub-Modeling (Solid Elements):** High-stress regions, particularly the steering knuckle connections (stub axles), were isolated and detailed using sub-modeling techniques. 
   * *Result:* Max Von Mises stress of **283 MPa** (Safely below the 355 MPa yield limit of S355 steel).
4. **Fatigue Analysis:** The 25mm rear axle was verified for infinite life under dynamic loads using the **Soderberg Criterion**.
5. **Stability:** Buckling analysis confirmed a critical load factor of 1.6.

![FEA Stress Distribution](Results_and_Images/analysis-vonmises.JPG)

![FEA Substitution](Results_and_Images/analysis-substitution.JPG)

## 📂 Repository Structure
* `/CAD_Models`: Contains SolidWorks native parts/assemblies (.sldprt, .sldasm) and exported .STEP files for universal access.
* `/Results_and_Images`: High-resolution CAD renders and FEA stress distribution contour plots.
* `/Documentations`: The comprehensive engineering design report (in Turkish) detailing all mathematical models, material selection, and cost analysis.

---
*Designed by Erdoğan Kır as a senior Mechatronics Engineering design project.*
