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
After completing the analytical calculations, I created a parametric CAD model of the aluminum bar in SolidWorks. The bar was modeled with a circular cross section using a diameter of 0.50 in. Rather than manually entering the calculated bar length, the length was linked to the design parameters through an equation
The CAD model was created parametrically so that the design dimensions could be modified if the load, diameter, material properties, or allowable deflection were changed. This allowed the model to be used for the later FEA verification and parameter study.
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
After completing the CAD model, I created a static FEA study in SolidWorks Simulation. The final material properties were assigned to the model, and the same 400 lbf tensile load used in the analytical calculations was applied.

One end of the bar was fixed, while the tensile load was applied at the opposite end. The model was then meshed and solved.
<img width="3196" height="1904" alt="image" src="https://github.com/user-attachments/assets/088abab0-dc89-4562-84ac-60db4d22e12d" />
<img width="3200" height="1902" alt="image" src="https://github.com/user-attachments/assets/7436355c-70f9-4134-ac78-662812d30e88" />
The FEA results were examined using:

-Total displacement

-Equivalent (von Mises) stress

-Equivalent strain

The deformation shown in the FEA plots was visually exaggerated by the software to make the deformation easier to see. The actual numerical displacement was taken from the result legend rather than from the visual deformation.

Using the same material, geometry, and loading conditions allows the FEA results to be directly compared with the analytical solution, I created a custom Aluminum material with:

Elastic Modulus: 9.86𝑒6 psi

Density: 0.097504 lb/in^3

Poisson’s Ratio: 0.36

Yield Strength: 40000 psi   and assigned it to the part
<img width="2540" height="1896" alt="image" src="https://github.com/user-attachments/assets/a8b6ea2a-ae35-45a6-80b3-b2b17be9f337" />

Applied load: 400lbs in Tension
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
The maximum von Mises stress was approximately 1.549x10^7 Pa which equals to 2.247 ksi. This is substantially below the specified aluminum yield strength of 40 ksi, resulting in an FEA safety factor of approximately 17.8. Since the safety factor is significantly greater than 1, the FEA indicates that yielding is not expected under the specified loading condition.
<img width="3200" height="1902" alt="image" src="https://github.com/user-attachments/assets/a9a0703b-6e34-41bb-97e9-272dc7a6373c" />
<img width="3200" height="1914" alt="image" src="https://github.com/user-attachments/assets/532e00cb-7fee-4945-bb45-39a9f7c0f386" />

### Design Decision
Based on the FEA results, I decided not to modify the applied load or bar diameter. The maximum displacement is essentially equal to the allowable 0.009 in, while the maximum von Mises stress remains well below the 40 ksi yield strength.
Therefore, the final design satisfies both the deflection requirement and the strength requirement for the loading condition specified in the assignment.

## Communicate
### Analytical vs. FEA
The analytical calculations were compared with the SolidWorks FEA results to verify the final design. The analytical and FEA displacement results were in very close agreement. The FEA maximum displacement was approximately 0.00901 in compared with the analytical value of 0.00900 in.
the difference from the analytical value of 0.009 in is only about: 0.079%
The percent difference was calculated using:

<img width="2337" height="1031" alt="IMG_2421" src="https://github.com/user-attachments/assets/24ae8af6-a2af-456f-a381-e3de4adc3838" />


Therefore, the analytical and FEA displacement results differed by only approximately 0.08%.

The stress results showed a larger difference. The analytical stress was approximately 2.037 ksi, while the FEA maximum von Mises stress was approximately 2.247 ksi. This represents a difference of approximately 10.3%.

<img width="1951" height="951" alt="IMG_2422" src="https://github.com/user-attachments/assets/53a7ae1f-26a5-4282-95b5-20d1eefb8c8f" />


Despite this difference, both methods predict stresses far below the specified 40 ksi yield strength. Both results therefore indicate that the bar should remain elastic under the applied 400 lbf load.

**Interpretation of the Results**
The close agreement between the analytical and FEA displacement results provides confidence that the CAD model, material properties, loading, and boundary conditions were set up correctly.

The analytical calculation assumes a uniform bar under ideal axial tension. FEA evaluates the geometry numerically using a mesh, so the local stress distribution can produce a somewhat higher maximum stress than the simple analytical value.

For this project, I would use the FEA result when evaluating the actual CAD geometry, because it accounts for the modeled geometry and local stress distribution. However, the analytical calculation remains important because it provides a simple independent check of whether the FEA result is reasonable.

### Pin Hole
The final part of the design reflection investigated the effect of adding a substantial pin hole near the left side of the bar. The assignment specifically required this investigation to be completed using a stress concentration factor and stated that the FEA should not be rerun.

Therefore, the original CAD model and FEA study were not modified. Instead, the nominal stress obtained from the completed FEA was used to estimate the peak stress that would occur around a hypothetical hole.

The final bar has a diameter of 0.50 in. For this investigation, I considered a hypothetical circular pin hole with a diameter of 0.25 in. This represents a substantial hole because the hole diameter is one-half of the bar diameter.
d=0.25in      
The geometric ratio used to determine the stress concentration factor was:   0.25/0.50

A Peterson-type stress concentration relationship for a circular hole in a finite-width flat bar under tension was used to determine the theoretical stress concentration factor. Peterson's stress-concentration references include circular holes in finite-width elements under uniaxial tension.
For:  d/W= 0.50

the stress concentration factor was approximately  K_t=2.156



The nominal stress away from the hypothetical hole was taken from the completed FEA:  

<img width="2924" height="1868" alt="image" src="https://github.com/user-attachments/assets/268bf9b8-b18f-41a0-8abc-c2e9d85b1e95" />
<img width="2926" height="1872" alt="image" src="https://github.com/user-attachments/assets/b8a5f1c0-703c-483e-94a8-1971bd35f4b8" />
<img width="850" height="360" alt="image" src="https://github.com/user-attachments/assets/8ee67b8e-4766-4a88-84c0-40dafab085c6" />

The estimated peak stress at the hole was calculated using:
<img width="828" height="134" alt="image" src="https://github.com/user-attachments/assets/d0e3c950-b0af-43f4-88a3-40eaaa6cf528" />

The specified aluminum yield strength is: Sy=40ksi

Therefore, the estimated safety factor against yielding is:
<img width="828" height="166" alt="image" src="https://github.com/user-attachments/assets/43fc0053-e0c9-4192-931d-8ae6dea6d1d5" />



The estimated peak stress of approximately 4.85 ksi remains well below the specified aluminum yield strength of 40 ksi. Therefore, the hypothetical pin hole would still satisfy the yield-strength requirement using this stress-concentration estimate.

This investigation also demonstrated why geometric discontinuities are important in mechanical design. Although the original bar had a relatively low nominal stress, the hole increases the local stress through a stress concentration. Even with this increase, the estimated safety factor remains substantially greater than 1.

No additional FEA was performed for the hole, consistent with the assignment instructions. The result was instead estimated using the existing FEA nominal stress and the appropriate stress concentration factor.


### Obstacles and Corrections

Several challenges occurred during the project, and documenting them helped show how the design developed rather than only presenting the final result.

**1. Understanding the Circular Cross Section**

At the beginning, I needed to determine how the circular cross-section requirement affected the geometry and calculations. For a circular bar, the cross-sectional area is:

Area=π/4 x d^2
 
This was different from using a rectangular width × thickness area, so I had to make sure the CAD model and analytical calculations both represented a round bar.

**2. Initially Assuming Young's Modulus**

The first analytical calculation used an assumed value of:

E=10x10^6 psi


Although this value was within the assignment's allowed aluminum range, I later found the provided MatWeb material data and corrected the value to:

E=9.86x10^6 psi

I updated the analytical calculation and used the corrected value consistently in the final CAD and FEA model.

This taught me that when a specific material-property source is provided, I should use the source data rather than simply choosing a representative value within the allowed range.

**3. Creating a Consistent Parametric CAD Model**

Another challenge was translating the analytical relationship into the CAD model. The length should not simply be treated as an unrelated dimension because it depends on the applied load, material stiffness, diameter, and allowable deflection.

The analytical relationship

L=(delta\pi d^2E)(4F)

was therefore used as the basis for the parametric design.

**4. Setting Up and Interpreting FEA**

The FEA setup required correctly assigning the material, fixing one end, applying the tensile load to the opposite end, creating a mesh, and interpreting the resulting plots.

The deformation displayed by SolidWorks was highly exaggerated visually. I therefore learned to use the numerical result shown in the result legend rather than estimating deformation from the appearance of the deformed bar.

The final FEA results were physically reasonable and closely matched the analytical displacement calculation.

### Lessons Learned

This project helped me understand how analytical equations, parametric CAD, and FEA work together during the engineering design process.

One of the most important lessons was the importance of using consistent material properties. I initially used an assumed Young's modulus, but after locating the provided MatWeb data, I corrected the value and updated the design. I learned that even though an assumed value may satisfy the numerical range given in the assignment, using an actual material property from the provided source makes the design more accurate and better supported. I also learned that material properties used in the analytical calculations should match the properties used in the CAD and FEA models.

I also learned how a circular cross section changes the area calculation and how the diameter affects both stiffness and material usage.

The FEA portion helped me understand that numerical results should be checked against analytical calculations rather than accepted without verification. The close agreement between the analytical and FEA displacement results gave me confidence that the model was set up correctly.

Finally, I learned that a design does not need to have a safety factor close to one to be considered successful. In this case, the design was primarily controlled by the allowable deflection, while the yield-strength requirement provided a much larger safety margin.

### Final Design Summary

The final bar was modeled using a circular aluminum cross section with a diameter of 0.50 in and a calculated length of approximately 43.56 in. The applied tensile load was 400 lbf, and the final Young's modulus used was 9.86 × 10⁶ psi.

The analytical calculation predicted a maximum displacement of 0.00900 in and a nominal stress of approximately 2.037 ksi.

The FEA predicted a maximum displacement of approximately 0.00901 in and a maximum von Mises stress of approximately 2.247 ksi. The corresponding FEA safety factor was approximately 17.8 based on the 40 ksi yield strength.

The close agreement between the analytical and FEA displacement results indicates that the final model provides a reasonable representation of the analytical design.

### CAD File
[Download Parametric and FEA (.SLDPRT)](https://raw.githubusercontent.com/Rama-H/megr2157-portfolio/refs/heads/main/docs/assignments/A03/Parametric%20and%20FEA%20Bar.SLDPRT)


Actual Time Spent: 16 hours


