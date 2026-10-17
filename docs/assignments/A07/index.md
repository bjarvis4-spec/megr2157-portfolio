
# A7 - Bracket FEA

## Objective

The objective of this assignment was to use Finite Element Analysis (FEA) in SolidWorks to improve the strength, stiffness, and weight of my bracket from Assignments #5 and #6. I tested three bracket designs using multiple mesh densities to compare maximum von Mises stress, maximum displacement, minimum safety factor, mass, and mesh element count. The goal was to achieve results within a 7% mesh-convergence difference before changing the geometry, or to use the finest available mesh after three unsuccessful refinement attempts.

## Analyze

I began with my existing bracket design, kept the assigned ASTM A36 steel material, and used a static study with a 750 lbf downward load applied at the lower cylinder. I fixed the upper mounting surfaces and began with a coarse mesh. The same basic load and support conditions were kept for the geometry comparisons.

**Material:** ASTM A36 Steel  
**Applied load:** 750 lbf  
**Total time spent:** 4 hours

| Setup | Screenshot | Caption |
|---|---|---|
| Original geometry | [View original bracket](https://i.postimg.cc/Q9LKbRpw/p01.jpg) | Figure 1. Original bracket before modification. |
| Fixtures | [View fixed supports](https://i.postimg.cc/47CH5rzj/p02.jpg) | Figure 2. Fixed upper mounting surfaces. |
| Applied loading | [View 750 lbf force](https://i.postimg.cc/47CH5rzr/p03.jpg) | Figure 3. Downward force applied to the lower cylinder. |
| Initial mesh | [View mesh setup](https://i.postimg.cc/WFRqnQMB/p04.jpg) | Figure 4. Coarse mesh settings used to begin analysis. |

The **inner loop** checks mesh sensitivity by changing the number of elements without changing the geometry. The **outer loop** changes the bracket geometry, after which the mesh studies are repeated. I recorded peak von Mises stress, resultant deflection, mass, minimum safety factor where available, and element counts. The required convergence threshold was 7%.

---

## Decide

### Design I — Original Bracket

#### Initial Analysis

I began with my original design and ran the first static study using a coarse mesh. I then refined the mesh to compare the stresses and displacements. This provided a baseline for later design changes. The greatest displacement occurred at the lower cylindrical section, while the stress plots emphasized the connecting stem.

#### Inner Loop 1: FEA Test 1 vs FEA Test 2

| | FEA Test 1 | FEA Test 2 |
|---|---|---|
| **Max Stress (psi)** | **625,000** | **818,593** |
| Screenshot | [View screenshot](https://i.postimg.cc/mzx1w0Ys/p06.jpg) | [View screenshot](https://i.postimg.cc/N9h24W6f/p12.jpg) |
| **Max Deflection (in)** | **0.2171** | **0.2204** |
| Screenshot | [View screenshot](https://i.postimg.cc/R6rJRj75/p05.jpg) | [View screenshot](https://i.postimg.cc/2bpLwPQy/p13.jpg) |
| **Mass (lb)** | **0.29** | **0.29** |
| Screenshot | [View screenshot](https://i.postimg.cc/HcG82fwH/p08.jpg) | [View screenshot](https://i.postimg.cc/vgRxzprB/p15.jpg) |
| **Min Safety Factor** | **0.058 (SolidWorks plot)** | **0.044 (estimated)** |
| Screenshot | [View screenshot](https://i.postimg.cc/sQFGctYz/p07.jpg) | Not captured |
| **Mesh Elements** | **1,267** | **63,927** |
| Screenshot | [View screenshot](https://i.postimg.cc/XGMB8Tf4/p09.jpg) | [View screenshot](https://i.postimg.cc/R6rJRj7W/p16.jpg) |

*Figure 5. The original bracket was tested with a coarse and refined mesh without changing the geometry.*

| Supporting screenshot | Caption |
|---|---|
| [View image 10](https://i.postimg.cc/xJrNRWv0/p10.jpg) | Adjusted mesh settings for Test 2. |
| [View image 11](https://i.postimg.cc/LYdgTrt9/p11.jpg) | Refined surface mesh for Test 2. |
| [View image 14](https://i.postimg.cc/zbmHj9C3/p14.jpg) | Equivalent strain result from Test 2. |
| [View image 17](https://i.postimg.cc/wyKRVSXy/p17.jpg) | Original convergence calculator screenshot; the calculation must be checked using consistent units. |

**Convergence check (Tests 1–2):** peak stress 23.65%, deflection 1.50%. Peak stress was above the required 7% difference, so I continued mesh testing.

#### Inner Loop 2: FEA Test 3 vs FEA Test 4

| | FEA Test 3 | FEA Test 4 |
|---|---|---|
| **Max Stress (psi)** | **616,265** | **773,486** |
| Screenshot | [View screenshot](https://i.postimg.cc/N9h24W6r/p19.jpg) | [View screenshot](https://i.postimg.cc/LYdgTrtf/p23.jpg) |
| **Max Deflection (in)** | **0.2173** | **Not recorded** |
| Screenshot | [View screenshot](https://i.postimg.cc/xJrNRWvz/p20.jpg) | Not captured |
| **Mass (lb)** | **0.29** | **0.29** |
| Screenshot | Not captured | [View screenshot](https://i.postimg.cc/N919PpDK/p25.jpg) |
| **Min Safety Factor** | **0.059 (estimated)** | **0.047 (estimated)** |
| Screenshot | Not captured | Not captured |
| **Mesh Elements** | **1,323** | **32,434** |
| Screenshot | [View screenshot](https://i.postimg.cc/BLWPgdTF/p22.jpg) | [View screenshot](https://i.postimg.cc/34g4bn14/p26.jpg) |

*Figure 6. Additional mesh adjustments were made because the maximum stress was still mesh-sensitive.*

| Supporting screenshot | Caption |
|---|---|
| [View image 18](https://i.postimg.cc/62s40Dr4/p18.jpg) | Mesh settings for Test 3. |
| [View image 21](https://i.postimg.cc/FdjdnDpH/p21.jpg) | Equivalent strain plot for Test 3. |
| [View image 24](https://i.postimg.cc/FdjdnDp7/p24.jpg) | Equivalent strain plot for Test 4. |

**Convergence check (Tests 3–4):** peak stress 20.33%; this remained above 7%. The displacement screenshot was not captured for Test 4.

#### Inner Loop 3: FEA Test 5 vs FEA Test 6

| | FEA Test 5 | FEA Test 6 |
|---|---|---|
| **Max Stress (psi)** | **657,456** | **738,677** |
| Screenshot | [View screenshot](https://i.postimg.cc/tZhZm2k6/p28.jpg) | [View screenshot](https://i.postimg.cc/KknksJf7/p34.jpg) |
| **Max Deflection (in)** | **0.2178** | **0.2196** |
| Screenshot | [View screenshot](https://i.postimg.cc/xJKJFt5H/p29.jpg) | [View screenshot](https://i.postimg.cc/WFMFfX86/p35.jpg) |
| **Mass (lb)** | **0.29** | **0.29** |
| Screenshot | [View screenshot](https://i.postimg.cc/S2W2tDdC/p31.jpg) | [View screenshot](https://i.postimg.cc/PpmpF2yy/p37.jpg) |
| **Min Safety Factor** | **0.055 (estimated)** | **0.049 (estimated)** |
| Screenshot | Not captured | Not captured |
| **Mesh Elements** | **2,970** | **14,773** |
| Screenshot | [View screenshot](https://i.postimg.cc/2b4bX2G4/p32.jpg) | [View screenshot](https://i.postimg.cc/R6c6bXdg/p38.jpg) |

*Figure 7. The final original-design test pair showed relatively consistent displacement, but peak stress still varied with mesh density.*

| Supporting screenshot | Caption |
|---|---|
| [View image 27](https://i.postimg.cc/YG1GybRm/p27.jpg) | Mesh visualization for Test 5. |
| [View image 30](https://i.postimg.cc/G8k8SqKv/p30.jpg) | Photograph documenting the work area; not used as a numerical result. |
| [View image 33](https://i.postimg.cc/DJqJYB6r/p33.jpg) | Mesh settings for Test 6. |
| [View image 36](https://i.postimg.cc/KknksJf5/p36.jpg) | Simulation solver notification for Test 6. |

**Convergence check (Tests 5–6):** peak stress 11.00%, deflection 0.82%. Stress still exceeded 7%; after the allowed attempts, I proceeded using the finer-mesh results as a reference.

#### Design I — Decision

The original bracket displaced approximately 0.22 in under the applied load. Because the connecting stem showed a large contribution to the deformation and elevated stress, I decided to increase its stiffness in Design II.

---

### Design II — Increasing Stiffness

I modified the vertical connecting stem to resist bending more effectively. My goal was to reduce the load-induced deflection of the lower cylinder. I kept the same material and load while testing the updated geometry at several mesh densities.

**Geometry modification:** [View stem sketch](https://i.postimg.cc/7GgGQm9B/p39.jpg) — Figure 8. Sketch used to change the vertical connecting member.

#### Inner Loop 1: FEA Test 7 vs FEA Test 8

| | FEA Test 7 | FEA Test 8 |
|---|---|---|
| **Max Stress (psi)** | **103,035** | **117,495** |
| Screenshot | [View screenshot](https://i.postimg.cc/G8k8SqKS/p40.jpg) | [View screenshot](https://i.postimg.cc/9wCR3Zgb/p45.jpg) |
| **Max Deflection (in)** | **0.0166** | **Not recorded** |
| Screenshot | [View screenshot](https://i.postimg.cc/cgQg5Xhb/p41.jpg) | Not captured |
| **Mass (lb)** | **0.30** | **0.30** |
| Screenshot | [View screenshot](https://i.postimg.cc/rRM06xZC/p43.jpg) | [View screenshot](https://i.postimg.cc/m1BzxCp8/p47.jpg) |
| **Min Safety Factor** | **0.352 (estimated)** | **0.309 (estimated)** |
| Screenshot | Not captured | Not captured |
| **Mesh Elements** | **2,737** | **Approx. 13,946*** |
| Screenshot | [View screenshot](https://i.postimg.cc/H8dcGXvt/p44.jpg) | [View screenshot](https://i.postimg.cc/BP4LWH7Y/p48.jpg) |

*Figure 9. The stem modification greatly reduced displacement compared with the original bracket.*

| Supporting screenshot | Caption |
|---|---|
| [View image 42](https://i.postimg.cc/HcQcPBzN/p42.jpg) | Equivalent strain plot for Test 7. |
| [View image 46](https://i.postimg.cc/YLMGcYD8/p46.jpg) | Equivalent strain plot for Test 8. |

**Convergence check (Tests 7–8):** peak stress 12.31%; it did not meet the 7% threshold.

#### Inner Loop 2: FEA Test 9 vs FEA Test 10

| | FEA Test 9 | FEA Test 10 |
|---|---|---|
| **Max Stress (psi)** | **105,674** | **113,869** |
| Screenshot | [View screenshot](https://i.postimg.cc/vxbgRf2P/p49.jpg) | [View screenshot](https://i.postimg.cc/qt6C2kC2/p54.jpg) |
| **Max Deflection (in)** | **0.0168** | **0.0170** |
| Screenshot | [View screenshot](https://i.postimg.cc/p5RhNzcc/p50.jpg) | [View screenshot](https://i.postimg.cc/xkNbL0b3/p55.jpg) |
| **Mass (lb)** | **0.30** | **0.30** |
| Screenshot | [View screenshot](https://i.postimg.cc/y3sgqcpb/p52.jpg) | [View screenshot](https://i.postimg.cc/xkNbL0bR/p57.jpg) |
| **Min Safety Factor** | **0.343 (estimated)** | **0.318 (estimated)** |
| Screenshot | Not captured | Not captured |
| **Mesh Elements** | **4,194** | **10,975** |
| Screenshot | [View screenshot](https://i.postimg.cc/jntwVP31/p53.jpg) | [View screenshot](https://i.postimg.cc/DW4b12bc/p58.jpg) |

*Figure 10. An additional pair of mesh densities brought the stress values closer together.*

| Supporting screenshot | Caption |
|---|---|
| [View image 51](https://i.postimg.cc/xNnJrMpF/p51.jpg) | Equivalent strain plot for Test 9. |
| [View image 56](https://i.postimg.cc/wtRsD6s5/p56.jpg) | Equivalent strain plot for Test 10. |

**Convergence check (Tests 9–10):** peak stress 7.20%, deflection 1.18%. Peak stress was close to, but still above, the 7% threshold.

#### Design II — Decision

Increasing the stem stiffness reduced displacement from about 0.22 in to 0.017 in. However, the bracket mass increased from 0.29 lb to 0.30 lb. I then looked for a way to reduce mass without removing the reinforcing material from the stem.

---

### Design III — Weight Reduction

For my final design, I created a 0.40 in diameter circle on the lower cylindrical section and removed material using Extruded Cut. I intended to reduce weight while retaining the stiffened connecting stem.

| Geometry change | Screenshot and caption |
|---|---|
| Circular sketch | [View circle sketch](https://i.postimg.cc/bGS21z2L/p59.jpg) — Figure 11. A 0.40 in diameter circle on the cylinder. |
| Extruded cut | [View cylinder cut](https://i.postimg.cc/Y4LmQpmb/p60.jpg) — Figure 12. Material removed from the cylindrical feature. |

#### Inner Loop 1: FEA Test 11 vs FEA Test 12

| | FEA Test 11 | FEA Test 12 |
|---|---|---|
| **Max Stress (psi)** | **106,472** | **121,368** |
| Screenshot | [View screenshot](https://i.postimg.cc/Mcfj1Wj9/p61.jpg) | [View screenshot](https://i.postimg.cc/Y4LmQpmV/p66.jpg) |
| **Max Deflection (in)** | **0.0167** | **0.0173** |
| Screenshot | [View screenshot](https://i.postimg.cc/LqgZjHZy/p62.jpg) | [View screenshot](https://i.postimg.cc/CZnfbFf9/p67.jpg) |
| **Mass (lb)** | **0.28** | **0.28** |
| Screenshot | [View screenshot](https://i.postimg.cc/hJQ7VS73/p64.jpg) | [View screenshot](https://i.postimg.cc/ns9QqHD8/p69.jpg) |
| **Min Safety Factor** | **0.341 (estimated)** | **0.299 (estimated)** |
| Screenshot | Not captured | Not captured |
| **Mesh Elements** | **1,815** | **20,416** |
| Screenshot | [View screenshot](https://i.postimg.cc/kVRtWntz/p65.jpg) | [View screenshot](https://i.postimg.cc/kVRtWnbP/p70.jpg) |

*Figure 13. Removing material reduced the bracket mass while maintaining a displacement near that of Design II.*

| Supporting screenshot | Caption |
|---|---|
| [View image 63](https://i.postimg.cc/t1nVFXVS/p63.jpg) | Equivalent strain distribution for Test 11. |
| [View image 68](https://i.postimg.cc/Z9vy6Tdt/p68.jpg) | Equivalent strain distribution for Test 12. |

**Convergence check (Tests 11–12):** peak stress 12.27%, deflection 3.47%. The stress difference exceeded 7%.

#### Inner Loop 2: FEA Test 13

| Measurement | FEA Test 13 |
|---|---|
| **Max Stress (psi)** | **105,805** |
| Screenshot | [View stress plot](https://i.postimg.cc/hJQ7VSdq/p71.jpg) |
| **Max Deflection (in)** | **0.0170** |
| Screenshot | [View displacement plot](https://i.postimg.cc/674GC9vX/p72.jpg) |
| **Mass (lb)** | **0.28** |
| Screenshot | [View mass properties](https://i.postimg.cc/YGcL3J1V/p74.jpg) |
| **Min Safety Factor** | **0.343 (estimated)** |
| **Mesh Elements** | **3,440** |
| Screenshot | [View mesh details](https://i.postimg.cc/JyHBj1kM/p75.jpg) |
| **Equivalent Strain** | [View strain plot](https://i.postimg.cc/PLv81twH/p73.jpg) |

*Figure 14. Additional mesh test of Design III to examine the stability of the stress and displacement predictions.*

**Convergence check (Tests 11–13):** peak stress 0.63% and displacement 1.76% between those two results. However, Test 12 used more elements than either and predicted a higher peak stress. Therefore these results do **not** establish consistent convergence of peak stress. I retained the finest-mesh result (Test 12) for the final comparison.

#### Design III — Decision

Removing material reduced mass to 0.28 lb, while maximum displacement remained approximately 0.017 in. The final design improved weight compared with Design II but did not fully solve the high stress or convergence problem.

---

## Communicate

### Final Design Comparison

The selected comparisons below are Test 6 for Design I, Test 10 for Design II, and Test 12 for Design III. They provide captured stress, displacement, mass, and mesh results, but the peak stresses did not consistently converge within 7%. In particular, Design I also included a finer mesh than Test 6; this table should not be described as showing converged results.

| Measurement | Design I | Design II | Design III |
|---|---|---|---|
| **Max Stress (psi)** | **738,677** | **113,869** | **121,368** |
| Screenshot | [View Design I stress](https://i.postimg.cc/KknksJf7/p34.jpg) | [View Design II stress](https://i.postimg.cc/qt6C2kC2/p54.jpg) | [View Design III stress](https://i.postimg.cc/Y4LmQpmV/p66.jpg) |
| **Max Deflection (in)** | **0.2196** | **0.0170** | **0.0173** |
| Screenshot | [View Design I deflection](https://i.postimg.cc/WFMFfX86/p35.jpg) | [View Design II deflection](https://i.postimg.cc/xkNbL0b3/p55.jpg) | [View Design III deflection](https://i.postimg.cc/CZnfbFf9/p67.jpg) |
| **Mass (lb)** | **0.29** | **0.30** | **0.28** |
| Screenshot | [View Design I mass](https://i.postimg.cc/PpmpF2yy/p37.jpg) | [View Design II mass](https://i.postimg.cc/xkNbL0bR/p57.jpg) | [View Design III mass](https://i.postimg.cc/ns9QqHD8/p69.jpg) |
| **Min Safety Factor (estimated)** | **0.049** | **0.318** | **0.299** |
| **Number of Mesh Elements** | **14,773** | **10,975** | **20,416** |
| Screenshot | [View Design I mesh](https://i.postimg.cc/R6c6bXdg/p38.jpg) | [View Design II mesh](https://i.postimg.cc/DW4b12bc/p58.jpg) | [View Design III mesh](https://i.postimg.cc/kVRtWnbP/p70.jpg) |

### Final Design Evaluation

Increasing the connecting stem stiffness was the largest improvement in the recorded simulations. Maximum displacement decreased from approximately 0.22 in to approximately 0.017 in. The final cylinder cut reduced mass from 0.30 lb in Design II to 0.28 lb in Design III without producing a large change in displacement.

These results are not sufficient to certify the bracket as structurally safe: the estimated safety factors remain below 1 and peak stress did not consistently converge with mesh refinement.

---

### Lessons Learned

Throughout this assignment, I became more comfortable using SolidWorks Simulation and interpreting FEA results. Mesh density affected peak stress more than I initially expected. Some tests produced substantially different maximum stresses as the element count increased, even though the maximum displacement changed very little. This showed me why mesh convergence matters before using a simulation to make engineering decisions.

I also saw the tradeoff between stiffness and mass. Modifying the vertical stem reduced the bracket's displacement considerably, but it also increased mass. Creating a hole in the lower cylinder reduced the weight while maintaining most of the stiffness gained in Design II. This helped me understand that geometry changes can improve one characteristic while making another less favorable.

An additional lesson was that simulations do not necessarily support my initial design assumptions. Some changes increased stress or produced little effect on displacement. Comparing repeated analyses gave me a clearer understanding of how stress concentration, load paths, and material distribution influence a component's performance.

**Actual time spent: 4 hours.**

### Conclusion

I evaluated three bracket geometries with multiple static FEA simulations. The original design established the baseline; the second design increased stiffness by modifying the connecting stem; and the third reduced mass by removing material from the cylinder. The final recorded configuration weighed 0.28 lb and showed approximately 0.0173 in maximum displacement, compared with 0.29 lb and 0.2196 in for the selected original-design simulation.

Although the final design showed substantial improvement in displacement and a small weight reduction, the stress sensitivity and low estimated safety factor indicate that further geometry modification and model validation would be required.

**CAD file download:** (https://drive.google.com/file/d/1yt4yYzLLKibAMbxgACzCwTrrfqud2SyW/view?usp=sharing)

### Calculation and Source Notes

- Stress and displacement values are expressed in **psi** and **in**, respectively, including conversions from screenshots that used SI units.
- Safety factors labeled **estimated** are calculated using an approximate ASTM A36 steel yield strength divided by the reported peak von Mises stress; they are **not** separately captured SolidWorks plots. The only captured factor-of-safety plot is in Test 1.
- Percent difference is computed as `ABS(finer - coarser) / ABS(finer) * 100%`; comparisons of mesh pairs do not by themselves guarantee a converged solution, especially when further refinement reverses the trend.
- `*` The Test 8 mesh-element digits are difficult to read in the photographed Mesh Details window; confirm the exact count from [image 48](https://i.postimg.cc/BP4LWH7Y/p48.jpg) if precision is required.

