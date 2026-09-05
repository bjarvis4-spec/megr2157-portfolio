# A3 – [Topic]

## Objective

Use axial deflection modeling to design its dimensions

Use parametric design to determine a bars length

Introduce you to FEA (Finite Element Analysis)

Introduce you to linking dimensions to appropriate parameters in CAD.

Compare and contrast the different analysis

## Analyze

HAND CALCULATIONS

The goal of this assignment was to design an aluminum bar under direct axial tension while limiting its maximum axial deflection to 0.009 in. I selected a load of 400 lbf, which is within the required range of 300–500 lbf. A Young’s Modulus of 10,000,000 psi was used. I selected a bar width of 0.500 in and a thickness of 0.250 in. All of these values are a solid middle ground to start from. I also found the area and the length using axial deflection. 
<img width="940" height="666" alt="image" src="https://github.com/user-attachments/assets/f149de6b-ac1b-41a9-a326-ddf9cc339503" />

When I opened solidworks I realized my units where in Newtons so I went ahead and converted the force from lbf to newtons.
<img width="1166" height="195" alt="image" src="https://github.com/user-attachments/assets/f10d3ebe-ad08-44ed-b889-c1dff2ed601f" />

## Decide

PARAMETRIC DESIGN

First, I set up my equations tab, I added all the given values and built my axial-deflection relationship so i could calculate the length instead of manually assigning the final length.
<img width="1498" height="537" alt="image" src="https://github.com/user-attachments/assets/035a1e5d-9628-4c37-acfd-14ca554c1364" />

Then, assigned width to bar using parametrics.
<img width="1225" height="638" alt="image" src="https://github.com/user-attachments/assets/54155395-6813-4587-89d4-a1684ae84af3" />

Did the same with the length using the formula I set up in parametrics.
<img width="1250" height="632" alt="image" src="https://github.com/user-attachments/assets/73889624-c73f-4e34-b505-d5b3d2e711c3" />

Then, turned the sketch into a 3d extrude and assigned the thickness.
<img width="942" height="362" alt="image" src="https://github.com/user-attachments/assets/44b2a50c-9d5e-4725-a847-ad1c46c164c1" />

FEA

First, I added the FEA and assigned the closest material which was Alluminum Alloy - 1060 Alloy.
<img width="358" height="671" alt="image" src="https://github.com/user-attachments/assets/922d51fa-dd3b-49c6-b949-f6cf1f4ae35c" />

To start the FEA I applied a fixed geometrty to the left side.
<img width="752" height="478" alt="image" src="https://github.com/user-attachments/assets/ea8cbccb-111d-4add-9d3c-1368179c5b1c" />

Then, on the opposing side a applied the force in tension and converted to Newtons
<img width="1032" height="427" alt="image" src="https://github.com/user-attachments/assets/affaf5f2-52bf-4a6a-9f6a-97e0663cdf7a" />

Next, I applied a mesh because the bar has a simple constant cross section and axial loading.
<img width="1361" height="451" alt="image" src="https://github.com/user-attachments/assets/369d5b9a-cc81-4be8-957c-41ecd8f1b19e" />

After converting the units to in, I ran a test to get displacement. Max value was very very similar to assignment details, however, the material is slightly different causing these slightly skewed results.
<img width="1362" height="473" alt="image" src="https://github.com/user-attachments/assets/0b72c18a-d256-4c9f-a64b-1abbee723b21" />

Next, I converted the units for the Von Mises Stress. The Von Mises stress remained relatively uniform through most of the bar because the cross-sectional area and axial load were constant. Some variation occurred near the fixed end because of the boundary condition.
<img width="1172" height="490" alt="image" src="https://github.com/user-attachments/assets/993863d5-e5ec-4655-a8e4-dd35f4d02474" />

## Communicate

SAFETY FACTOR

I calculated the safety factor to determine how much stronger the bar is than the stress produced by the applied load. This checks whether the bar will remain below the aluminum yield strength and verifies that the design is safe under the FEA loading condition.
<img width="1406" height="262" alt="image" src="https://github.com/user-attachments/assets/f1e14883-7b45-4b3c-86e9-aa333786716a" />
The safety factor is approximately 11.73. This means the aluminum yield strength is about 11.73 times greater than the maximum stress produced in the FEA. Since the maximum stress is much lower than the 40-ksi yield strength, the bar passes the strength requirement.

AXIAL DEFLECTION

I then compared the hand-calculated axial deflection with the FEA result to determine how closely the analytical equation predicted the behavior of the SolidWorks model. 
<img width="1242" height="260" alt="image" src="https://github.com/user-attachments/assets/1e20544e-0b19-449b-ae59-6b56bfc2edcb" />
The percent difference was only 0.129%, meaning the hand calculation and FEA produced almost the same deflection. This close agreement was expected because the bar has a constant cross section and is subjected to simple axial tension. 

PIN HOLE

Next, I evaluated a hypothetical pin hole to determine how a geometric change would affect the stress in the bar. A hole causes stress to focus around its edges, so the local stress can be much higher than the nominal stress in the original bar.
<img width="788" height="656" alt="image" src="https://github.com/user-attachments/assets/fb7589ef-89fc-404c-97b9-ff585e518ba1" />
The estimated peak stress around the hole was approximately 11.91 ksi. This is still lower than the 40-ksi aluminum yield strength, so the bar would still pass. However, the safety factor decreased from 11.73 to approximately 3.36. This shows that adding a hole can significantly increase local stress and reduce the margin of safety even though the external load remains the same.

LESSONS LEARNED

These calculations helped me understand the difference between simply checking whether a part deflects too much and checking whether the material itself is strong enough to resist yielding. I also learned how FEA can be used to verify analytical calculations. The FEA displacement was extremely close to the hand-calculated value, which gave me more confidence in both methods. 

One of the main challenges was learning the SolidWorks workflow. Before this assignment, I had mainly used Creo and had not previously completed this type of parametric modeling and FEA in SolidWorks. After awhile i found the similarities and it made it a lot easier to navigate. I also initially confused the displacement result with the von Mises stress result. I corrected this by checking the result type, legend, and units and creating separate plots for displacement and stress.

Total time spent: approximately 3 hours.
