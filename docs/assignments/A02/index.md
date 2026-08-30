# A2 – Truss Stress Analysis

## Objective
 - Design a lightweight planar truss using A500 steel or an alternative material.
 - Create free body diagrams (FBDs) for joints and critical pins.
 - Calculate the required cross-sectional area of truss elements with a safety factor.
 - Determine pin sizes based on shear forces with a safety factor.
 - Solve equations symbolically and numerically for both truss and pin design.
 - Estimate the total weight of the truss and pins.
 - Create a CAD model with accurate dimensions and connections.
 - Compare CAD weight predictions with hand calculations.
 - Document key engineering lessons learned from the process.

## Analyze
OVERALL TRUSS GEOMETRY

I started with listing out the requirements, loading conditions, support types, material requirements, and safety factors before making any design decisions. The  dimensions provided were a = 0.4 m and b = 0.3 m, with point A being a pin support and B being a roller support. I selected P = 25 kN, Because it was a solid middle ground between the 20-30 range provided.
<img width="1252" height="513" alt="image" src="https://github.com/user-attachments/assets/585d7d0f-54c5-4eac-a928-5ac6e28bab04" />

The first open design choice in the project was designing the geometry of the truss. I chose a five-member layout consisting of AB, BC, CD, DA, and CA, with four joints and the three provided support reactions. After a substaintial amount of research, I selected this geometry because it creates a stable, statically determinate truss with a very low number of members. Using less members reduces total material which also results in a lower overrall weight which is a main objective of the project.
<img width="1063" height="581" alt="image" src="https://github.com/user-attachments/assets/1e5308e3-f7c7-476b-9580-b004bb3db739" />

I checked the number of joints, support reactions, and members to make sure the geometry matched up to successful truss designs.
<img width="760" height="122" alt="image" src="https://github.com/user-attachments/assets/74b9ec85-bcbe-4bd9-a6c1-a4ace8d85f93" />

After choosing the geometry, I calculated the length of every truss member. I used the given values from a and b and used the Pythagorean theorem to find the diagonal members. These lengths were essential for both the structural calculations and for calculating the total truss weight later on.
<img width="1297" height="663" alt="image" src="https://github.com/user-attachments/assets/57376eb7-e1c0-49de-a526-0a954d77fc5e" />

EXTERNAL FORCES

Next, I created a full free body diagram of the truss. I included Ax and Ay at the pin support A, By at the roller support B, the upward 25 kN force at C, and the downward 25 kN force at D. This let me discover all of the external reactions before completing the Method of Joints.
<img width="893" height="433" alt="image" src="https://github.com/user-attachments/assets/30cfe62d-2f9d-40b2-8919-35b85c1babe8" />

Then, I used the equilibrium equations to calculate the support reactions. First, I found Ay = - By using Fx=0 and Fy=0.
<img width="998" height="285" alt="image" src="https://github.com/user-attachments/assets/4aa2576e-91cd-4880-897b-ec278d1c8261" />

Following this i used, moment about A = 0 to find the actual values of Ay and By. 
<img width="1222" height="268" alt="image" src="https://github.com/user-attachments/assets/40ad53b6-5582-4f6a-95c2-4889441dcb6f" />

INTERNAL FORCES

After finding the support reactions, I analyzed the internal forces using the Method of Joints. I began with joints B and D because each of those joints had only two unknown member forces. I then moved to Joint C to solve for the final unknown member force and determine which member controlled the design.
<img width="962" height="671" alt="image" src="https://github.com/user-attachments/assets/faec4c11-483b-41a5-9bca-e96532dd55bc" />
<img width="1197" height="430" alt="image" src="https://github.com/user-attachments/assets/d53c4c0e-1235-4fac-b5e9-7b6eb860e245" />
After completing the Method of Joints, I compared all of the internal member forces. Member CA had the largest force magnitude with approximately 47.47 kN in compression.

## Decide
TRUSS CROSS-SECTIONAL AREA

First, I listed all given, known, and unknown values.
<img width="976" height="330" alt="image" src="https://github.com/user-attachments/assets/38819438-915e-465e-8aee-fcbc0c7b5188" />

Next, with the normal stress and incorporated the required safety factor I solved for the symbolic minimium cross-sectional area. This symbolic equation was then used for the numerical design.
<img width="982" height="242" alt="image" src="https://github.com/user-attachments/assets/50f70c3f-31f6-4094-a6b4-63ca2f6f6051" />

I also found the minimum area value to make the numerical calculations smoother in the next step.
<img width="957" height="152" alt="image" src="https://github.com/user-attachments/assets/31c86618-f412-4c2d-80b6-5305cecf2137" />

Then, I found the numerical values for the cross-sectioanl area using the same formulas from the symbolic equation.
<img width="845" height="255" alt="image" src="https://github.com/user-attachments/assets/232fa992-9f44-4f20-b5e5-3ea30b492e57" />

After the cross-sectional area I checked to make sure it was aligned with the safety factor of 3.5.
<img width="1141" height="325" alt="image" src="https://github.com/user-attachments/assets/e73d0f02-7c95-4f89-9b3b-e4f58301f86f" />

Finally, I did the truss weight calculations. I calculated the truss weight before making the CAD model because this gave me a reference value to compare with the final Creo mass. I used the selected cross-sectional area and the total member length to calculate the approximate volume. I then used the steel density and gravitational acceleration to determine the estimated weight.
<img width="1086" height="648" alt="image" src="https://github.com/user-attachments/assets/c5cfb6d8-b71d-4c96-add9-d2e8cde2c1c5" />

PIN CROSS-SECTIONAL AREA

The assignment required a single-shear connection, a safety factor of 4, a yield shear strength of 170 ksi, and a density of 0.278 lb/in³ for the pins. I used these values to determine the required pin area and diameter. Fist, listing the given, known, and unknown.
<img width="1226" height="637" alt="image" src="https://github.com/user-attachments/assets/ac243061-2c32-4542-a45e-9aec6d834c4f" />

I then created a free-body diagram of the critical pin connection to show how the member forces were transferred through the pin. I made it look accurate to how the model would in CAD so I could visulaize it better.
<img width="797" height="455" alt="image" src="https://github.com/user-attachments/assets/928b9788-d16d-456b-ace8-a114072f7979" />

Then, to find the symbolical pin area I used the shear-stress equation and included the required safety factor. I rearranged the equation symbolically before substituting the numerical values.
<img width="1042" height="441" alt="image" src="https://github.com/user-attachments/assets/21052796-a5dc-4493-b050-633fb4432cf6" />

Next, using the equations from the symbolic cross-sectional area, I filled in the values I had previously to get the numerical equation.
<img width="965" height="326" alt="image" src="https://github.com/user-attachments/assets/5d039417-697c-4a74-9fa3-95a0f764cf2f" />

After that, I solved for the pin diameter using the area forumla of a circle. This ended up being different when i designed it in CAD for geometrical reasons.
<img width="1380" height="358" alt="image" src="https://github.com/user-attachments/assets/3e76cfc1-c9b7-4632-b730-3b60d8c63375" />

Finally, I estimated the combined pin weight by modeling each pin as a cylinder. The area, pin length, and hardened tool-steel density were used to determine the volume and mass. 
<img width="1156" height="667" alt="image" src="https://github.com/user-attachments/assets/c6a0afbe-ea9f-4829-b2ed-aae7e8483469" />

CAD DESIGN

I modeled the  truss minus the pins as one solid part, which matched the assignment requirements. The member dimensions and pin locations were based directly on the hand calculations. 
I started by building each member and setting meausurments. I used a standard member size of 22 mm × 22 mm throughout the main truss sections.
<img width="1200" height="502" alt="image" src="https://github.com/user-attachments/assets/7b91fdd5-45d5-441f-a4f4-d2e21c99c5d3" />
<img width="1217" height="477" alt="image" src="https://github.com/user-attachments/assets/784acc94-ca85-4633-bad7-cc252ca6cc6d" />

At the joints, I made sure the members merged into one continuous solid while maintaining enough material around the pin holes.
<img width="1201" height="487" alt="image" src="https://github.com/user-attachments/assets/8620fd03-4da0-4a3f-87dc-68e8e299bb2c" />
<img width="1182" height="495" alt="image" src="https://github.com/user-attachments/assets/bd97320e-1ee9-4d42-965c-0b04f9af3a1b" />
<img width="1191" height="467" alt="image" src="https://github.com/user-attachments/assets/b491903d-2728-422e-b88d-17fc9845b4ac" />

After some adjustments, I centered each pin hole at the location where the centerlines intersected. At joints where multiple members met, I used one common pin location rather than separate pin holes for each member. The final pins were modeled as cylinders with the revised 11 mm diameter. This was changed from the original 15 mm so that the pin could be at the centerlines while still having a large enough diameter. This was also changed to avoid the material surrounding the pin holes being too thin.
<img width="1173" height="492" alt="image" src="https://github.com/user-attachments/assets/269dc5f7-3849-46a4-b0d9-d6cc3bd23c89" />

Once I finished the sketch for the extrude I amde it 22mm thick to satisy the calculations made in the design process.
<img width="1386" height="597" alt="image" src="https://github.com/user-attachments/assets/8716d686-2925-4a45-98dc-e8148694a382" />

Then, I filled in the pin holes with a second extrude made up of 4 pins. 
<img width="1112" height="655" alt="image" src="https://github.com/user-attachments/assets/61b01ccc-51f8-48d0-9499-721b175b8865" />
<img width="1057" height="438" alt="image" src="https://github.com/user-attachments/assets/f3274f12-00ab-4dfa-8a0b-2425789cd231" />

A500 structural steel was not available in my Creo material library. I then instead used Creo's generic STEEL material, which had a density of approximately 7827 kg/m³. This was the material with the most similair qualities. After correcting the units and assigning the steel material, I ran the Creo Mass Properties analysis. Creo predicted a final truss mass of around 12.44 kg. Converting this value to weight gave me 122.0 N.
<img width="857" height="397" alt="image" src="https://github.com/user-attachments/assets/da2d07f5-a006-478c-92f3-ba8e19e693c6" />
<img width="420" height="462" alt="image" src="https://github.com/user-attachments/assets/c22a893f-cd14-438b-89a5-7d0e752391e0" />
The 22 mm × 22 mm member size produced a safety factor of approximately 3.52, which is only slightly above the required 3.5 and therefore avoids excessive material. I also had reduced the pin diameter to 11 mm, which also decreased overall weight.

## Communicate

