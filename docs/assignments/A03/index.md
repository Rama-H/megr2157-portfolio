# A3 – Parametric and FEA 

## Objective
The objective of this project was to design an aluminum bar with a circular cross section under direct tension while maintaining a maximum axial deflection of 0.009 in. The design process combined analytical calculations, parametric CAD modeling, and finite element analysis (FEA).
<img width="1354" height="530" alt="image" src="https://github.com/user-attachments/assets/4b5ce041-3f39-4690-9e18-5331718bb98f" />

The project required selecting appropriate design parameters, including the applied load, Young's modulus, and bar diameter, then using the axial deflection equation to determine the required bar length. The resulting geometry was modeled parametrically in CAD so that the design could be modified by changing the defined parameters.


The completed design was then verified using FEA by examining the axial deflection and von Mises stress. The FEA results were compared with the analytical solution, and the design was evaluated against the specified aluminum yield strength of 40 ksi. A stress concentration investigation was also performed to determine the potential effect of adding a pin hole to the bar.
Finally, the design parameters were investigated to understand how changes in loading and geometry affect the required bar dimensions.

## Analyze
### Initial Design Decisions
The first step was to identify the requirements that controlled the design. The bar had to have a circular cross section and be made from aluminum. The applied tensile load had to be between 300 and 500 lbf, while the Young's modulus had to fall within the specified range of (8.5x10^6) to (11.5x10^6) psi. The maximum allowable axial deflection was 0.009 in, and the specified aluminum yield strength was 40 ksi.
<img width="2004" height="1388" alt="CamScanner 9-2-26 20 25_1" src="https://github.com/user-attachments/assets/dc859b95-2c46-4ae7-89b6-1b785338f2e4" />
The main design variables were the bar diameter and length. The cross-sectional area was determined from the diameter using the area equation for a circle.

**Force**- I selected an applied load of 400 lbf because it is approximately in the middle of the required 300–500 lbf range. This provided a representative loading condition without selecting either extreme of the allowable range.

**For Young's modulus**, at the beginning, I initially used:      E=10x10^6 psi

as an assumed representative value within the aluminum range given in the assignment. I later realized that the assignment provided a specific MatWeb material-property resource, so instead of assuming a value, I should use an actual material property from the provided source.

I checked the provided MatWeb data and found:
<img width="3139" height="1652" alt="image" src="https://github.com/user-attachments/assets/b65a721f-5780-48ea-809c-9b86b08d7118" />

E=9860 ksi

Therefore: I finally **selected E=9.86x10^6 psi** and used it in my calculations, since this value is within the required range of (8.5–11.5x10^6) psi.

**Bar Diameter**- The initial bar diameter was selected as 0.50 in. The assignment does not specify a minimum or maximum diameter, so a practical diameter had to be selected as part of the design process. I chose 0.50 in as a reasonable starting geometry and then used the deflection requirement to determine the corresponding bar length.

The maximum allowable deflection of 0.009 in was used as the design target. Designing to the maximum allowable deflection allows the selected geometry to use the available deformation limit rather than unnecessarily restricting the bar.
<img width="2304" height="1022" alt="CamScanner 9-3-26 21 48_1" src="https://github.com/user-attachments/assets/cbedaee7-d1b7-4c0f-8bbd-a3c070fa245a" />

### Circular Cross-Section Calculation
Because the assignment specifies a circular cross section, the cross-sectional area was calculated using
<img width="1338" height="503" alt="CamScanner 9-3-26 21 48_1 1" src="https://github.com/user-attachments/assets/fe5f7e47-6a8b-4350-9f02-7bb30854b59b" />

For the selected diameter of 0.50 in, the cross-sectional area used for the initial design was approximately 0.196 in^2, this area was then used in the axial deflection and stress calculations

### Analytical Calculations
For a uniform bar subjected to direct tension, the axial deflection is calculated using the Axial Deflection Equation δ = (F × L) / (A × E)

Since the required bar length was the unknown, the equation was rearranged to solve for (L):
<img width="2304" height="716" alt="CamScanner 9-3-26 21 48_1 2" src="https://github.com/user-attachments/assets/f23f646f-495c-422b-9e76-3e313812a59b" />

Therefore: the analytical design predicts a required **bar length** of approximately **L=43.5in**

**Analytical Stress**
<img width="2304" height="379" alt="CamScanner 9-3-26 21 48_1 3" src="https://github.com/user-attachments/assets/39c05490-cd4b-4816-9f22-64a731b48151" />

**Analytical FOS or Factor Of Safety**
<img width="2280" height="370" alt="CamScanner 9-3-26 22 09_1" src="https://github.com/user-attachments/assets/f087c0f2-a8e1-439a-9397-ed02bc243cd0" />

The calculated tensile stress is significantly below the specified aluminum yield strength of 40 ksi. The resulting analytical safety factor is approximately 19.6, indicating that yielding is not expected under the applied 400-lbf load.

**Volume**
<img width="1706" height="370" alt="CamScanner 9-3-26 22 09_1 1" src="https://github.com/user-attachments/assets/02725199-6854-40b7-a12f-23b4df6ec0e3" />

**Weight**
<img width="2282" height="489" alt="CamScanner 9-3-26 22 09_1 2" src="https://github.com/user-attachments/assets/04bc4164-8ffc-46da-b40b-d1d1d8303a83" />
I used the density given from the Matweb Material Property Data
<img width="3145" height="1652" alt="image" src="https://github.com/user-attachments/assets/57b4303a-bf1f-43f8-af51-3da72ca99be8" />

## Decide
### Parametric CAD
The next step was to convert the analytical design into a parametric CAD model. Rather than manually entering the calculated bar length, the length was linked to the design parameters through an equation.
**Setup**
CAD parameter/equation table:
<img width="1610" height="778" alt="image" src="https://github.com/user-attachments/assets/1ba27585-2a91-4c95-a38c-24377b723d48" />

The circular cross-sectional area was defined as  A="Diameter D" ^ 2 * pi / 4

and the required length was defined as L="Max Deflection" * "Area" * "Young's Modulus E" / F

The CAD model produced a calculated bar length of approximately 43.56 in, which agrees with the analytical calculation. This confirms that the parametric equation was correctly implemented.

Here I sketched the circle using the global variable of the Diameter D= 0.50, I chose the Right Plane for sketcing
<img width="3198" height="1910" alt="image" src="https://github.com/user-attachments/assets/c36d68d8-f15b-415b-b556-42af71834651" />
and then extruded the circle, using the global variable of the Length = 43.56 in
<img width="3198" height="1850" alt="image" src="https://github.com/user-attachments/assets/bc09e83d-a966-44f1-bc12-a1020f570197" />
This is the final shape of the bar
<img width="3200" height="1904" alt="image" src="https://github.com/user-attachments/assets/ce9bb127-a363-44b9-8d77-9262092716e5" />

### FEA Setup
After completing the parametric CAD model, the geometry was used for finite element analysis. The same 400-lbf tensile load and aluminum material properties used in the analytical calculation were applied to the FEA model.

The bar was constrained at one end and loaded in tension at the opposite end. A mesh was generated over the bar before solving the study.
<img width="3196" height="1904" alt="image" src="https://github.com/user-attachments/assets/088abab0-dc89-4562-84ac-60db4d22e12d" />

Using the same material, geometry, and loading conditions allows the FEA results to be directly compared with the analytical solution, I created a custom Aluminum material with:

Elastic Modulus: 9.86𝑒6 psi

Density: 0.097504 lb/in^3

Poisson’s Ratio: 0.36

Yield Strength: 40000 psi   and assigned it to the part
<img width="2540" height="1896" alt="image" src="https://github.com/user-attachments/assets/a8b6ea2a-ae35-45a6-80b3-b2b17be9f337" />

Applied load
<img width="3200" height="1902" alt="image" src="https://github.com/user-attachments/assets/7436355c-70f9-4134-ac78-662812d30e88" />
And here I clicked Mesh and Run
<img width="3200" height="1904" alt="image" src="https://github.com/user-attachments/assets/f748ab6d-7aeb-47df-ab87-229e549066bb" />

### FEA Deflection
After I ran FEA, the FEA produced a maximum axial displacement of 0.000228781 m which converts to 0.009007 in. 
<img width="2256" height="835" alt="IMG_2415" src="https://github.com/user-attachments/assets/5f85a9a3-eba8-4638-b808-9b042d17cc9c" />
That's extremely close to the required 0.009 in.

The maximum displacement occurred at the loaded end of the bar, while the constrained end remained approximately fixed.
<img width="3198" height="1906" alt="image" src="https://github.com/user-attachments/assets/ea2f693b-7d14-495c-9857-f7af46c01ac0" />


### FEA Stress- Von Mises stress
The maximum von Mises stress obtained from the FEA was 2.247 ksi. This value was compared with the specified aluminum yield strength of 40 ksi.
<img width="2744" height="1384" alt="IMG_2416" src="https://github.com/user-attachments/assets/422bf41e-2d47-4a54-8d75-9e81a53e3878" />
The maximum von Mises stress was approximately 1.549x10^7 Pa which equals to 2.247 ksi. This is substantially below the specified aluminum yield strength of 40 ksi, resulting in an FEA safety factor of approximately 17.8
<img width="3200" height="1902" alt="image" src="https://github.com/user-attachments/assets/a9a0703b-6e34-41bb-97e9-272dc7a6373c" />
<img width="3200" height="1914" alt="image" src="https://github.com/user-attachments/assets/532e00cb-7fee-4945-bb45-39a9f7c0f386" />


## Communicate
### Analytical vs. FEA
the difference from the analytical value of 0.009 in is only about: 0.079%
### Pin Hole
### Lessons Learned
What I learned
I learned that even though an assumed value may satisfy the numerical range given in the assignment, using an actual material property from the provided source makes the design more accurate and better supported. I also learned that material properties used in the analytical calculations should match the properties used in the CAD and FEA models.


Actual Time Spent
CAD Files

