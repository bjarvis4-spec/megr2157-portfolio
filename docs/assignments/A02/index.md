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

CROSS-SECTIONAL AREA

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



## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

## Communicate

