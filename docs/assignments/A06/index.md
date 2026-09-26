# A6 – [BRACKET DRAWING]

## Objective

Create a parametric solid model of the bracket using dimensions driven by the previous stress analysis.

Connect the analytical equations and design variables directly to dimensions in SolidWorks.

Create a fully dimensioned multiview engineering drawing using third-angle projection.

Apply the required sliding-fit tolerances and general drawing tolerances.

Include a tolerance block and all information necessary to manufacture and interpret the bracket.

Reflect on how parametric equations and engineering tolerances affect the final design.

## Analyze

PARAMETRIC DESIGN

I used the stress analysis from the previous assignment to control the dimensions of the bracket. I first entered the known values, material properties, safety factor, feature lengths, and stress equations as global variables in SolidWorks. This allowed the dimensions of the model to reference equations instead of only using manually entered values.

Global variables and analytical equations used to control the bracket dimensions in SolidWorks.
<img width="872" height="666" alt="image" src="https://github.com/user-attachments/assets/c05f01e7-0745-4f84-bc7e-539bdf2a7cb7" />

Feature A was modeled using its calculated diameter and length as parametric dimensions.
<img width="1032" height="560" alt="image" src="https://github.com/user-attachments/assets/23bde030-f7ce-4dc8-942e-e289778c6ebb" />

The connecting geometry was positioned using a dimension related to the surrounding calculated features.
<img width="725" height="647" alt="image" src="https://github.com/user-attachments/assets/b18f0075-a2e4-4af4-b7c0-f737415a2c45" />

Feature B thickness was linked to the calculated width parameter from the stress analysis.
<img width="802" height="610" alt="image" src="https://github.com/user-attachments/assets/b05a1645-bd5e-42d6-95d3-493514095e7d" />

Feature C was created using the calculated length and thickness required by the design.
<img width="706" height="458" alt="image" src="https://github.com/user-attachments/assets/63346072-6ad0-4878-8f91-6cf0b6b3f3d2" />

The width of Feature D was connected to its defined parametric variable.
<img width="881" height="603" alt="image" src="https://github.com/user-attachments/assets/fc6ef5e7-59fb-47bd-9c39-f92db620a593" />

Feature E modeled using its defined parametric length and dimensions.
<img width="676" height="452" alt="image" src="https://github.com/user-attachments/assets/c40c021e-af23-48df-8b42-e5395b2dd6d6" />

Completed parametric bracket model with all features combined.
<img width="777" height="522" alt="image" src="https://github.com/user-attachments/assets/641dcff9-435b-4343-928f-b5a3457e77e8" />

PART LINK: https://drive.google.com/file/d/1dG5lHKyUBEag0YwD6D8eYK0I57zxy31K/view?usp=sharing

## Decide

DRAWING

I created a fully dimensioned multiview drawing using third-angle projection. The drawing includes the important feature dimensions, material information, sliding-fit tolerances, and the required tolerance block.
The three sliding-fit gaps were given their own tolerances because they control how the bracket fits over the rigid T-beam. The remaining dimensions use the general tolerance block.

Final third-angle engineering drawing with dimensions, fit tolerances, and tolerance block.
<img width="925" height="661" alt="image" src="https://github.com/user-attachments/assets/ec56eb43-14ed-4f06-a60d-0e47023ef49a" />

DRAWING LINK: https://drive.google.com/file/d/1Rd9gAOA0MS8MVd1ucFcSmacIvnb_gRYh/view?usp=sharing

## Communicate

Parametric Equation

I used the bending-stress equation to control one of the bracket dimensions. The equation was entered directly into SolidWorks and linked to the sketch dimension instead of manually typing in the final calculated value. This allowed the model to update automatically if the design variables changed.
Drawing Tolerances

I used tighter tolerances on the sliding-fit dimensions because they are functional mating surfaces. A looser tolerance such as X.X ± .02 can be used on non-critical dimensions because small changes will not affect how the bracket fits or functions.
Using unnecessarily tight tolerances on non-critical features can increase manufacturing and inspection cost without improving the performance of the part.

Lessons Learned

This assignment showed me how the engineering calculations, CAD model, and drawing connect together. I also learned that tolerances should be based on the function of each feature instead of applying the tightest tolerance everywhere.

Mistakes / Corrections

I had to make sure the correct variables were linked to the correct sketch dimensions. I also had to separate the sliding-fit tolerances from the general tolerance block so the drawing clearly showed the required fits.

Total time spent: 3.5 hours
