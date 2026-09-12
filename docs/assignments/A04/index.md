# A4 – [Motor Mount]

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
<img width="1420" height="345" alt="image" src="https://github.com/user-attachments/assets/7f234eb4-6d32-48e9-963b-2a566194a049" />

The deflection calculation required 8.93 mm, which was larger than the 6.48 mm required for yielding. Because deflection controlled the design, I rounded the thickness upward and selected 10 mm for Feature 1. The final 10 mm thickness stayed below both the allowable stress and the 0.30 mm deflection limit.
<img width="907" height="127" alt="image" src="https://github.com/user-attachments/assets/e3264f52-9691-46b2-bc6c-2672d818e248" />
<img width="1205" height="305" alt="image" src="https://github.com/user-attachments/assets/c955e6af-03c0-4ada-984a-7d86baea55e3" />

FEATURE 2

I repeated the same process for Feature 2, which attaches the mount to rigid wall A. I used a 45 mm width and modeled 20 mm of the feature as the unsupported cantilever section. I also listed the rest of the known and unknown values.
<img width="1396" height="367" alt="image" src="https://github.com/user-attachments/assets/c0441890-0600-4710-9ef9-2ab1fd622116" />

When drawing the FBD, I treated the wall as a rigid support and modeled the lower section of Feature 2 as a cantilever. The same 5400 N·mm motor moment was used because the load is transferred through the mount. 
<img width="1245" height="412" alt="image" src="https://github.com/user-attachments/assets/7d0bb1bb-f82e-40f8-bbb7-9ab0bc56d0e5" />

I then used the beam-bending stress equation to determine the minimum thickness for Feature 2. The yield calculation resulted in a required thickness of 6.48 mm.
<img width="1185" height="305" alt="image" src="https://github.com/user-attachments/assets/a3020e61-2a6f-48ce-9e2c-970797707274" />

I then checked for deflection for Feature 2 using the 0.30 mm maximum deflection requirement. This calculation required approximately 6.82 mm, which was slightly greater than the thickness required for yielding.
<img width="1337" height="462" alt="image" src="https://github.com/user-attachments/assets/9a5ba7bf-335b-47e1-9a89-357bf9137320" />

Since deflection again controlled the design, I rounded the required thickness upward and selected 8 mm. I checked the final design and found a stress of 11.25 MPa, a safety factor of about 4.57, and a deflection of about 0.186 mm, so the selected size met the requirements.
<img width="1322" height="506" alt="image" src="https://github.com/user-attachments/assets/cf317c6b-e301-4d85-a896-9e64c9687ef0" />

## Decide

SKETCH

After completing the calculations, I made an isometric sketch to turn the two beam features into one motor-mount design. I used the calculated 10 mm thickness for Feature 1 and 8 mm thickness for Feature 2. I also made approximations of the size needed for the other holes where the motor would sit.
<img width="1367" height="642" alt="image" src="https://github.com/user-attachments/assets/80963e66-da6d-4f44-89de-382fcff53863" />

## Communicate

CAD MODEL (PARAMETRIC)

(Forgot to take pictures throughout process so I went back and took them after.)
I added the main dimensions that I planned to carry into Creo. I selected a 45 mm width, 50 mm base length, and 60 mm wall height to provide enough room for the motor and mounting holes while keeping the overall bracket compact. 
<img width="1235" height="605" alt="image" src="https://github.com/user-attachments/assets/a2b5e07b-c448-4c80-8834-b5c8aa79cc47" />

Initially when creating the shape I forgot to create parametrics. So I created Creo parameters for the important dimensions of the mount, including the 45 mm width, 50 mm base length, 10 mm Feature 1 thickness, 60 mm wall height, and 8 mm Feature 2 thickness. These parameters allow the main geometry to be changed without manually editing every related dimension.
<img width="446" height="167" alt="image" src="https://github.com/user-attachments/assets/8cebf512-e676-4e79-a94e-2fd21241e63b" />

I originally built most of the part by entering the numerical dimensions directly. After finishing the main shape, I realized that although I had created parameters, I had not actually assigned them to the corresponding CAD dimensions.I went back through the model and connected the important dimensions to their parameters. For example, the 8 mm wall thickness was assigned to the F2_THICK parameter. This corrected my mistake and made the final model properly parametric.
<img width="1236" height="632" alt="image" src="https://github.com/user-attachments/assets/73821feb-c0fc-4491-a4e6-997353ad6b54" />

I used the 28 mm motor/gearbox diameter as reference geometry when locating the motor. I centered the motor across the 45 mm mount width, placing its centerline 22.5 mm from either side so the motor would sit evenly on Feature 1.
<img width="1251" height="620" alt="image" src="https://github.com/user-attachments/assets/2d2c5c5a-6173-4071-9054-80ee4b64f94e" />

I then created the center opening for the motor shaft at the same center point as the motor. This allows the shaft to pass through the mounting feature without interfering with the bracket.
<img width="1162" height="558" alt="image" src="https://github.com/user-attachments/assets/249f183f-158b-4fd2-82b1-be030bd909a8" />

I created four 3.4 mm clearance holes for attaching Feature 2 to rigid wall A. I placed the hole columns one-fourth of the 45 mm plate width from each side, giving an 1/4 of the side length offset and keeping the pattern symmetric.
<img width="1017" height="487" alt="image" src="https://github.com/user-attachments/assets/fe540cf3-1d83-4474-8dba-b5199d2b4edc" />

I cut the four 3.4 mm holes completely through the wall feature. These holes provide the attachment points between the motor mount and rigid wall A as required by the assignment. <img width="1025" height="471" alt="image" src="https://github.com/user-attachments/assets/3cd3324b-6557-4383-b288-2ccd643a0722" />

I originally overlooked the motor mount holes, I added the required 3.4 mm clearance holes for the motor mounting screws using the mounting pattern from the supplied motor dimensions. These holes allow the motor to be fastened directly to Feature 1.
<img width="1081" height="550" alt="image" src="https://github.com/user-attachments/assets/a9355936-6fab-416a-b27d-6a75fe141923" />
<img width="1236" height="596" alt="image" src="https://github.com/user-attachments/assets/cc4e30ac-1717-473a-927c-b4bdac6e0cac" />

This assignment showed me that a design can meet the yield-strength requirement but still deflect too much. Deflection controlled the thickness of both features, which is why I selected dimensions larger than the minimum required for yielding. I also learned that it is better to set up CAD parameters before building the model instead of adding them afterward, because it makes changes much easier and keeps the design organized.

During the assignment, I made a few mistakes that I corrected as I worked. In my first Feature 1 yield calculation, I forgot to properly include the factor of safety of 3, so I corrected the allowable stress and redid the calculation. In Creo, I also forgot to take pictures during some of the modeling process and initially used direct dimensions instead of connecting my parameters to the model, so I went back and fixed both. I also originally overlooked the motor mounting holes and later added the required 3.4 mm clearance holes using the supplied motor mounting pattern.

Actual Time: 9 hrs

CAD Download Link: https://drive.google.com/file/d/1lNJxbY5zvmMehi_i_ix9Rhbq3UfN7BDM/view?usp=sharing

APPENDIX

Material Source

PETG Material Properties – MatWeb

I used the PETG source provided in the assignment for the material properties used in my calculations. The values I used were an elastic modulus of 3.03 GPa and a yield strength of 51.4 MPa.

[MatWeb PETG Material Properties](https://www.matweb.com/search/datasheettext.aspx?matguid=4de1c85bb946406a86c52b688e3810d0&utm_)

Motor Mount Research

Pololu 25D Gearmotor Bracket

I used this as a reference for how a compact gearmotor can be mounted using multiple fastener locations around the motor. The bracket also shows a simple design that keeps the motor supported without making the mount overly large.

[Pololu 25D Gearmotor Bracket](https://www.pololu.com/product/2676?utm_)

Adafruit L-Bracket Motor Mount

I used this as a reference for the basic L-shaped bracket layout. It shows how one surface can support the motor while the other surface attaches the bracket to another structure.

[Adafruit L-Bracket Motor Mount](https://www.adafruit.com/product/3768?utm_)
