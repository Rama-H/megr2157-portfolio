# A2 – Truss Stress Analysis

## Objective
The objective of this assignment was to design a lightweight planar truss that could support the specified loading while satisfying a required safety factor. I used a load of (P=20 kN), with the geometric constraints (a=0.4 m) and (b=0.3 m), and designed the members using structural steel. The design process included selecting a simple truss geometry, determining the internal member forces, sizing the truss members and connecting pins, estimating the weight analytically, and creating a 3D CAD model to compare the analytical design with the CAD prediction.

<img width="1266" height="612" alt="Screenshot 2026-08-30 163129" src="https://github.com/user-attachments/assets/ce281513-ae34-49cd-82ec-e3f87d1c865f" />

<img width="2076" height="2840" alt="CamScanner 8-30-26 17 15_1 1" src="https://github.com/user-attachments/assets/bac7c27a-21ea-4f1f-a4aa-705b50ffcdd6" />


## Analyze
### Initial Design and Geometry

I began by studying the loading and geometric constraints provided in the assignment. The required dimensions were (a=0.4 m) and (b=0.3 m), and I selected the minimum allowed load of (P=20 kN) to reduce the required material while still satisfying the design requirement. I chose a simple symmetrical truss geometry because it provides a clear load path from the two applied loads toward the supports while keeping the number of members relatively small.

My final geometry contains five joints and seven truss members. The upper chord has two (0.60 m) sections, the lower chord contains a (0.40 m) section, the two outer diagonal members are (0.50 m) long, and the two inner diagonal members are approximately (0.3606 m) long. 

<img width="2152" height="2856" alt="CamScanner 8-30-26 17 30_1" src="https://github.com/user-attachments/assets/2180bc61-dea2-4a34-bd35-262c9b285fde" />

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

The completed truss was evaluated using SolidWorks Mass Properties to determine the predicted mass and weight. The model was assigned a steel density of 7850 kg/m³, resulting in a predicted truss mass of 9.44 kg, corresponding to a weight of approximately 92.6 N. This CAD result provides a direct check of the physical dimensions and material selection used in the analytical design.

<img width="3190" height="1904" alt="Screenshot 2026-08-29 192740" src="https://github.com/user-attachments/assets/1452defa-a95a-4abc-bce5-907b26bb52e7" />


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

