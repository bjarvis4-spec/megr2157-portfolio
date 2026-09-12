# A4 – [Topic]

## Objective

- Obtain working knowledge designing a motor mount
- Design a motor mount for the specified 24 V DC gear motor that attaches to rigid wall A.
- Analyze both Feature 1 and Feature 2 using beam-bending equations.
- Design each feature for both yield strength and a maximum 0.30 mm deflection.
- Use a required factor of safety of 3 while neglecting the weight of the motor.
- Create FBDs, list knowns and unknowns, and solve the equations both symbolically and numerically.
- Use the calculated dimensions to create an isometric sketch of the final motor mount.
- Build a parametric 3D CAD model with shaft clearance and 3.4 mm bolt clearance holes.
- Document the complete design process, including calculations, CAD progress, mistakes, research, and lessons learned.

## Analyze

FEATURE 1

First, I listed some givens to help me get started. I then determined the moment created by the 300 N force acting at the end of the 18 mm motor shaft. This moment is the load used in the beam analysis for the motor mount.
<img width="1302" height="396" alt="image" src="https://github.com/user-attachments/assets/efa020f6-303e-4d3e-9f24-994233b34c54" />

I reviewed the motor dimensions before choosing the size of the mount. The gearbox is approximately 28 mm in diameter, the shaft is 6 mm in diameter, and the mounting pattern uses four M3 holes on a 22 mm bolt circle. I selected a mount width of 45 mm to give enough room around the motor.
<img width="1465" height="255" alt="image" src="https://github.com/user-attachments/assets/643b4d7c-f314-4221-9f31-eac7c645fbef" />

After some research via sources in the appendix, I chose PETG because it gave me a good balance of strength, stiffness, toughness, and printability for a functional motor mount. PETG is commonly used for mechanical parts, holders, and brackets because it has good layer adhesion, resists cracking better than more brittle materials, and has better temperature resistance than basic PLA. Prusa specifically describes PETG as suitable for technical and mechanical parts because of its toughness and temperature resistance, while UltiMaker describes it as having a useful balance between toughness and stiffness for functional prototypes.
<img width="1380" height="361" alt="image" src="https://github.com/user-attachments/assets/16ad7685-6796-40ac-bcf3-9365ee6a3365" />

I listed all of the known values for Feature 1 before starting the calculations. I selected a 45 mm width and a 30 mm effective beam length, with the required thickness being the main unknown. 
<img width="1280" height="420" alt="image" src="https://github.com/user-attachments/assets/574fde91-0fdd-4f21-a7c6-800c237f4be3" />

Then, for the FBD, I simplified Feature 1 into a cantilever beam with the motor moment acting at the free end. I also represented the feature with a rectangular cross section so I could use the beam-bending equations from lecture.
<img width="662" height="430" alt="image" src="https://github.com/user-attachments/assets/4f8b5f39-79a7-4682-a1a7-7032c12b8142" />

After that, I solved for the thickness required to prevent Feature 1 from yielding. During my first attempt, I forgot to properly include the required safety factor of 3, so I corrected the allowable stress and redid the calculation.
<img width="977" height="613" alt="image" src="https://github.com/user-attachments/assets/99635213-8fe1-4147-8222-158e75b0ace9" />
<img width="817" height="500" alt="image" src="https://github.com/user-attachments/assets/3e392ddd-63e3-44fb-b1f1-2d4816711941" />

After correcting the calculation, the minimum thickness based on yielding was 6.48 mm. This was only the strength requirement, so I still needed to check whether the feature would meet the deflection requirement.
<img width="1117" height="201" alt="image" src="https://github.com/user-attachments/assets/f418ba0f-83bb-4186-a3fe-c5507ddfd992" />

I then analyzed Feature 1 for the maximum allowed deflection of 0.30 mm. I used the cantilever beam conditions from the assignment and solved the beam equation for the required thickness.
<img width="1237" height="661" alt="image" src="https://github.com/user-attachments/assets/8d0aed47-2f10-433e-963f-7ddb4a9ff589" />

The deflection calculation required 8.93 mm, which was larger than the 6.48 mm required for yielding. Because deflection controlled the design, I rounded the thickness upward and selected 10 mm for Feature 1. The final 10 mm thickness stayed below both the allowable stress and the 0.30 mm deflection limit.
<img width="1420" height="345" alt="image" src="https://github.com/user-attachments/assets/7f234eb4-6d32-48e9-963b-2a566194a049" />
<img width="1205" height="305" alt="image" src="https://github.com/user-attachments/assets/c955e6af-03c0-4ada-984a-7d86baea55e3" />

FEATURE 2

I repeated the same process for Feature 2, which attaches the mount to rigid wall A. I used a 45 mm width and modeled 20 mm of the feature as the unsupported cantilever section.


SKETCH



CAD MODEL (PARAMETRIC)



## Decide


## Communicate

