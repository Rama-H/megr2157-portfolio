# A2 – Truss Stress Analysis

## Objective
The objective of this assignment was to design a lightweight planar truss that could support the specified loading while satisfying a required safety factor. I used a load of (P=20 kN), with the geometric constraints (a=0.4 m) and (b=0.3 m), and designed the members using structural steel. The design process included selecting a simple truss geometry, determining the internal member forces, sizing the truss members and connecting pins, estimating the weight analytically, and creating a 3D CAD model to compare the analytical design with the CAD prediction.

<img width="1266" height="612" alt="Screenshot 2026-08-30 163129" src="https://github.com/user-attachments/assets/ce281513-ae34-49cd-82ec-e3f87d1c865f" />

<img width="2076" height="2840" alt="CamScanner 8-30-26 17 15_1 1" src="https://github.com/user-attachments/assets/bac7c27a-21ea-4f1f-a4aa-705b50ffcdd6" />

## Analyze
### Initial Design and Geometry

I began by studying the loading and geometric constraints provided in the assignment. The required dimensions were (a=0.4 m) and (b=0.3 m), and I selected the minimum allowed load of (P=20 kN) to reduce the required material while still satisfying the design requirement. I chose a simple symmetrical truss geometry because it provides a clear load path from the two applied loads toward the supports while keeping the number of members relatively small.

My final geometry contains five joints and seven truss members. The upper chord has two (0.60 m) sections, the lower chord contains a (0.40 m) section, the two outer diagonal members are (0.50 m) long, and the two inner diagonal members are approximately (0.3606 m) long. 

<img width="3200" height="1908" alt="Screenshot 2026-08-30 173639" src="https://github.com/user-attachments/assets/51ad5681-76dc-420d-a9de-2bb1aeb08d41" />

<img width="2152" height="2856" alt="CamScanner 8-30-26 17 30_1" src="https://github.com/user-attachments/assets/2180bc61-dea2-4a34-bd35-262c9b285fde" />

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
### Selected Truss Member
### Analytical Truss Weight


## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._
### Final Truss Geometry
### Member Cross Section
### Pin Design
### Selected Pin
### Pin Weight
### CAD Model and Verification
### CAD vs. Analytical Weight

## Communicate

### Engineering Lessons Learned
### Design Process
### Challenges / Mistakes
### Final Design Summary

