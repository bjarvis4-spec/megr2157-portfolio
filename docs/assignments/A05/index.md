# A5 – [Bracket Design]

## Objective

- Conduct stress analysis to determine appropriate dimensions for structural features.

- Generate free body diagrams (FBDs) to visualize forces and constraints for each feature.\

- Identify and document known and unknown variables, assumptions, and algebraic models for stress calculations.

- Perform stiffness analysis to establish minimum required dimensions based on deflection constraints.

- Compare stress and stiffness analyses to ensure structural integrity and compliance with given constraints.

- Create detailed multiview sketches illustrating dimensions derived from both stress and stiffness analyses.

- Reflect on and document key engineering lessons learned throughout the process.

## Analyze

STRESS

First, I chose A36 steel and drew out the fbd of the whole bracket so i could visualize better aswell as writng out the constant knowns and assumptions for the whole design. Then, I began the bracket analysis with Feature A, which supports the polyester strap. I identified the known values, assumptions, and loading conditions, then created a free body diagram and modeled the feature as a cantilever beam to determine the required size based on bending stress.
<img width="466" height="660" alt="image" src="https://github.com/user-attachments/assets/35697dc7-7aec-4f81-8c25-b9b2267d8ca6" />

I then analyzed Features B and C using the loading conditions from the bracket. Feature B was treated as an axially loaded member, while Feature C was treated as a simply supported beam. I also included the FBDs, assumptions, knowns, and unknowns for each feature.
<img width="693" height="657" alt="image" src="https://github.com/user-attachments/assets/fb9b7931-ee97-400c-9a8b-5df8b3e0eed6" />

I continued the stress analysis through Features D and E using the forces transferred from the previous sections. Symmetry was used to divide the load between the two sides of the bracket, and each feature was analyzed using the loading model that best represented its behavior.
<img width="735" height="662" alt="image" src="https://github.com/user-attachments/assets/d9898dbf-f52d-4064-a522-392b922a6685" />

STIFFNESS 

I analyzed the stiffness of Features A and B using the maximum allowable deflection from the assignment. Feature A was modeled as a bending member, while Feature B was checked for axial deformation. The required dimensions were determined based on limiting deformation.
<img width="727" height="627" alt="image" src="https://github.com/user-attachments/assets/6528bbf9-c5af-416f-b58b-03f92a1015d7" />

I completed the stiffness analysis for Features C, D, and E. The load path and symmetry from the stress analysis were kept the same, while the dimensions were determined using the deflection requirements for each feature.
<img width="611" height="652" alt="image" src="https://github.com/user-attachments/assets/a9dc5306-313e-4a36-9634-8590e0d4388e" />

## Decide

SKETCHES

I created a multiview sketch of the bracket using the dimensions determined from the stress analysis. The drawing shows the overall geometry and how the calculated feature sizes fit around the required T-beam dimensions.
<img width="937" height="647" alt="image" src="https://github.com/user-attachments/assets/34355f25-a793-44d6-bf6c-a59e8f9b5b0c" />

I created a second multiview sketch using the dimensions determined from the stiffness analysis. This allowed me to directly compare the stress-based and stiffness-based designs before selecting the governing dimensions for the final bracket.
<img width="902" height="600" alt="image" src="https://github.com/user-attachments/assets/a76a6589-4538-43fa-8b75-6bbf35046dfa" />

## Communicate

LESSON LEARNED

Governing Failure Mode - For Feature C, stress governed the final dimension. The stress analysis required about 0.559 in, while the stiffness analysis required about 0.432 in, a difference of about 0.127 in. This showed me that a part can satisfy the deflection requirement but still need to be larger to remain within the allowable stress.

Error Propagation - The reaction forces from Feature C were carried into Features D and E. Because the bracket was treated as symmetric, the load was divided evenly between the two sides. If I had calculated the reactions from C incorrectly, the loads used for both D and E would also have been incorrect, so checking the symmetry and load path before continuing helped prevent that error from propagating.

Assumption Sensitivity - One important assumption was that the bracket and applied load were symmetric. This allowed both sides of the bracket to carry equal portions of the load. If the load were applied off-center, one side would carry more force than the other, which would increase the required dimensions of Features D and E on the more heavily loaded side.

I spent 4.5 hours on this assignment.
