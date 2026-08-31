# A2 – Truss Stress Analysis

## Objective
The objective of this assignment was to design a lightweight planar truss that could support the specified loading while satisfying a required safety factor. I used a load of (P=20 kN), with the geometric constraints (a=0.4 m) and (b=0.3 m), and designed the members using structural steel. The design process included selecting a simple truss geometry, determining the internal member forces, sizing the truss members and connecting pins, estimating the weight analytically, and creating a 3D CAD model to compare the analytical design with the CAD prediction.

<img width="1266" height="612" alt="Screenshot 2026-08-30 163129" src="https://github.com/user-attachments/assets/ce281513-ae34-49cd-82ec-e3f87d1c865f" />

The assignment also specifies A500 structural steel for the truss; however, A500 was not available in my SolidWorks material library. The assignment allows another type of steel to be used when the specified material is unavailable, so I selected ASTM A36 Steel as the equivalent material for my CAD model. For the connecting pins, I used AISI Type A2 Tool Steel, following the assignment requirement for hardened tool steel with a yield shear strength of (170 ksi) and a density of (0.278 lb/in^3).

## Analyze
### Initial Design and Geometry
I began by identifying the fixed parameters provided in the assignment, point A was modeled as a pin support and point B as a roller support. I then developed a simple symmetrical five-joint truss containing seven members so that the loading could be transferred to the two supports while keeping the geometry relatively simple. 

<img width="2076" height="2840" alt="CamScanner 8-30-26 17 15_1 1" src="https://github.com/user-attachments/assets/bac7c27a-21ea-4f1f-a4aa-705b50ffcdd6" />

I studied the loading and geometric constraints provided in the assignment. The required dimensions were (a=0.4 m) and (b=0.3 m), and I selected the minimum allowed load of (P=20 kN) to reduce the required material while still satisfying the design requirement. I chose a simple symmetrical truss geometry because it provides a clear load path from the two applied loads toward the supports while keeping the number of members relatively small.

My final geometry contains five joints and seven truss members. The upper chord has two (0.60 m) sections, the lower chord contains a (0.40 m) section, the two outer diagonal members are (0.50 m) long, and the two inner diagonal members are approximately (0.3606 m) long. 

<img width="2152" height="2856" alt="CamScanner 8-30-26 17 30_1" src="https://github.com/user-attachments/assets/2180bc61-dea2-4a34-bd35-262c9b285fde" />

and then I sketched it in SolidWorks

<img width="2096" height="1030" alt="Screenshot 2026-08-30 201022" src="https://github.com/user-attachments/assets/7e164041-97e2-449b-b136-440792f02e00" /> 

### Support Reactions

Point A was modeled as a pin support and point B as a roller support, as required by the assignment. The pin at A provides horizontal and vertical reactions, while the roller at B provides a vertical reaction. I first solved for the external support reactions before calculating the forces in individual truss members, I solved symbolically first and then plugged in the numbers and then solved numerically using statics.

The unknown reactions were: Ax​,Ay​,By​

<img width="1675" height="964" alt="CamScanner 8-30-26 17 48_1" src="https://github.com/user-attachments/assets/8a561f76-260a-4cc4-9e05-793faf5f3f5e" />

and then I plugged in numbers :

<img width="2000" height="1412" alt="CamScanner 8-30-26 18 01_1" src="https://github.com/user-attachments/assets/47e7d803-53ef-4a80-a4d0-500a2d87702c" />


and here I used statics to calculate the internal forces which gave me the same answers as the symbolic solution:

<img width="1904" height="1252" alt="CamScanner 8-30-26 17 43_1" src="https://github.com/user-attachments/assets/5c8829fc-e3df-454c-8afd-8e656fdc59c3" />


### Free Body Diagrams and Internal Member Forces

After finding the support reactions, I used the method of joints to determine the internal force in every truss member. Each member was initially assumed to be in tension, and the sign of the calculated force was then used to determine whether the member was actually in tension or compression. This process allowed me to identify the most highly loaded member, which was then used to size the cross section. I solved symbolically first and then numerically as shown below

Symbolic 
<img width="2160" height="2812" alt="CamScanner 8-30-26 17 55_1" src="https://github.com/user-attachments/assets/ea0717c9-c18b-4fac-bcc6-c8a8af2f5ec5" />

<img width="1364" height="784" alt="CamScanner 8-30-26 17 55_2" src="https://github.com/user-attachments/assets/c82fa9af-cc51-467f-ba69-3eab42db8086" />

and here I plugged the numbers in and found Fmax:

<img width="2096" height="2928" alt="CamScanner 8-30-26 18 05_1" src="https://github.com/user-attachments/assets/d0698821-736f-4e0a-b7f5-e5bf6ff86861" />
and here's my statics work solving using method of joints 

<img width="2412" height="1380" alt="CamScanner 8-30-26 20 50_1" src="https://github.com/user-attachments/assets/3ee2a530-f064-4f7d-b87a-07b97b35cf92" />

<img width="2024" height="252" alt="CamScanner 8-30-26 20 50_2" src="https://github.com/user-attachments/assets/11adfb60-a62f-454f-ae0d-d219ff7e60e9" />

and I made this internal forces table to compare which is the max force:

<img width="1788" height="732" alt="CamScanner 8-30-26 18 08_1" src="https://github.com/user-attachments/assets/40e380f0-755e-4c17-8a3d-96f7e5b4d53b" />

Therefore the largest internal force is:  Fmax=16.02kN
	​
### Truss Member Cross-Sectional Area
The largest internal force (Fmax=16.02kN) was used to determine the minimum required cross-sectional area of the truss members. I used a safety factor of 3.5 and the yield strength of the selected structural steel (Grade B yield strength). The purpose of this calculation was to ensure that the working stress remained below the allowable stress while keeping the truss as lightweight as reasonably possible.

Known values

F_max=16.02kN   SF=3.5    sigma_y 317 MPa 

Unknown: A_min
	​
<img width="2004" height="2296" alt="CamScanner 8-30-26 18 57_1" src="https://github.com/user-attachments/assets/039da16b-5de8-4828-be2b-6a3e289a3fd9" />

### Truss Material Selection
The assignment specifies A500 structural steel for the truss. However, A500 structural steel was not available in the SolidWorks material library I was using. Since the assignment specifically states that another type of steel may be used when the required material is unavailable, I selected ASTM A36 Steel for the truss. I used the material properties associated with the selected material when evaluating the design and assigned ASTM A36 to the truss CAD model. 

<img width="3200" height="1778" alt="Screenshot 2026-08-30 205456" src="https://github.com/user-attachments/assets/6bd09036-36d9-47c2-8641-2ad15d767f84" />

### Selected Truss Member
For the CAD model, I selected a rectangular tube with dimensions: 

<img width="2144" height="1964" alt="CamScanner 8-30-26 19 13_1" src="https://github.com/user-attachments/assets/d270253f-542e-48c6-bbd5-76375b11b385" />

I selected this geometry because it provides sufficient cross-sectional area while remaining relatively simple to model and manufacture. Using the same cross section for every member also follows the assignment constraint that all truss elements must have identical cross-sectional geometry. 

<img width="3114" height="1906" alt="Screenshot 2026-08-30 192353" src="https://github.com/user-attachments/assets/dd832201-f6a9-40e8-8332-82a290914109" />

<img width="3200" height="1908" alt="Screenshot 2026-08-30 173639" src="https://github.com/user-attachments/assets/51ad5681-76dc-420d-a9de-2bb1aeb08d41" />


### Analytical Truss Weight

After determining the member cross section, I estimated the mass of the truss by adding the lengths of all members and multiplying the resulting volume by the density of steel.

The total member length is: 3.3211 m

<img width="1860" height="1948" alt="CamScanner 8-30-26 19 29_1" src="https://github.com/user-attachments/assets/27654b2a-fe6b-4357-8b12-e0cf5d1f296e" />

The completed truss was evaluated using SolidWorks Mass Properties to determine the predicted mass and weight. The model was assigned a steel density of 7850 kg/m³, resulting in a predicted truss mass of 9.44 kg, corresponding to a weight of approximately 92.6 N, the difference is approximately (6.9%) which can be attributed to differences between the simplified analytical volume calculation and the actual CAD geometry at the member intersections. This CAD result provides a direct check of the physical dimensions and material selection used in the analytical design.

<img width="3190" height="1904" alt="Screenshot 2026-08-29 192740" src="https://github.com/user-attachments/assets/1452defa-a95a-4abc-bce5-907b26bb52e7" />

### Pin Material and Design
The next part of the design was determining the required cross-sectional area of the connecting pins. The assignment requires the connecting pins to be made from hardened tool steel with a yield shear strength of (170 ksi), a safety factor of 4, a density of (0.278 lb/in^3) and a single-shear connection.
For the CAD model, I selected AISI Type A2 Tool Steel as the pin material because it is a hardened tool steel and was available in the SolidWorks material library. The specified shear yield strength and density from the assignment were used for the pin design calculation.

<img width="1904" height="1500" alt="CamScanner 8-30-26 20 15_1" src="https://github.com/user-attachments/assets/367aefa3-f2ad-43ee-b90d-f769da6fb5c3" />

### Pin Area Calculation

<img width="2268" height="2888" alt="CamScanner 8-30-26 20 20_1" src="https://github.com/user-attachments/assets/052384db-ea26-43c7-9ae0-55b8ef0f20c9" />


### Pin CAD Design
I first sketched a circle in the front plan with a 10 mm diameter
<img width="3188" height="1906" alt="Screenshot 2026-08-30 211556" src="https://github.com/user-attachments/assets/cef52e02-b34a-4bca-9afd-cf8bf8aa7bf7" />

Then selected the AISI Type A2 Tool Steel material
<img width="3196" height="1890" alt="Screenshot 2026-08-30 212049" src="https://github.com/user-attachments/assets/a44c2d87-05b5-4524-9a65-916aca8bd19d" />

I extruded the Circle with a 50 mm thickness so it spans with the truss thickness 
<img width="3198" height="1902" alt="Screenshot 2026-08-30 212219" src="https://github.com/user-attachments/assets/da301939-0b80-4b9b-8928-e66c19e1e2e4" />

I added a fillet at one of the edges of the circle faces with a 0.50mm radius 
<img width="3194" height="1702" alt="Screenshot 2026-08-30 212402" src="https://github.com/user-attachments/assets/96f3b9b6-02bc-4324-ba4a-e5e7173a2e5c" />
<img width="2822" height="1478" alt="Screenshot 2026-08-30 212512" src="https://github.com/user-attachments/assets/54ed3c3a-c59a-453f-9f94-d27533760f62" />

and then I added a head to the shaft with a 16mm diameter and 2mm thickness so that the pin could retain the truss members in the assembly, and prevent the pin shaft from sliding 
<img width="3200" height="1906" alt="Screenshot 2026-08-30 212808" src="https://github.com/user-attachments/assets/9737320b-fa58-426e-ad8a-f0c58f33f338" />
<img width="3186" height="1900" alt="Screenshot 2026-08-30 212915" src="https://github.com/user-attachments/assets/a15cf478-3014-4d6d-9aba-435f647c3fd4" />

### Pin Weight

## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._
### Final Truss Geometry
I decided to use the five-joint, seven-member truss because it provides a simple and relatively compact load path while satisfying the required dimensions. The geometry uses symmetry around the center of the structure and places the inner diagonal members between the loaded lower joints and the upper chord. This design was chosen before creating the CAD model so that the analytical calculations and the physical model represented the same geometry. 


### Member Cross Section
The analytical calculation showed that the minimum required area was approximately (176.8 mm^2). I selected a (50 x 30 x 2.6 mm) rectangular tube with an actual cross-sectional area of approximately (388.96 mm^2), which is greater than the required minimum. The larger available section was selected because it provides additional margin above the theoretical minimum and could be modeled consistently for every truss member. 

### Pin Design
The next part of the design was determining the required cross-sectional area of the connecting pins. The assignment specifies hardened tool steel with a yield 
shear strength of (170 ksi), a safety factor of 4, and a single-shear connection.

<img width="1904" height="1500" alt="CamScanner 8-30-26 20 15_1" src="https://github.com/user-attachments/assets/367aefa3-f2ad-43ee-b90d-f769da6fb5c3" />

<img width="2268" height="2888" alt="CamScanner 8-30-26 20 20_1" src="https://github.com/user-attachments/assets/052384db-ea26-43c7-9ae0-55b8ef0f20c9" />


### Selected Pin

### Pin Weight
### CAD Model and Verification
### CAD vs. Analytical Weight

## Communicate

### Engineering Lessons Learned
### Design Process
### Challenges / Mistakes
### Final Design Summary

