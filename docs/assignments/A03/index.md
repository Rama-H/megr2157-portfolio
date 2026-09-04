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

For a selected diameter of 0.50 in

Therefore, the cross-sectional area used for the initial design was approximately

This area was then used in the axial deflection and stress calculations
### Analytical Calculations
For a uniform bar subjected to direct tension, the axial deflection is calculated using the Axial Deflection Equation

Since the required bar length was unknown, the equation was rearranged to solve for (L):

**Bar Length**
Therefore, the analytical design predicts a required bar length of approximately **L=43.5in**

**Analytical Stress**

Analytical Safety Factor
The calculated tensile stress is significantly below the specified aluminum yield strength of 40 ksi. The resulting analytical safety factor is approximately 19.6, indicating that yielding is not expected under the applied 400-lbf load.
Volume
Weight
<img width="3160" height="1580" alt="Screenshot 2026-09-02 212820" src="https://github.com/user-attachments/assets/a9a8ad55-2e73-4757-ad7a-479ce6d84797" />


## Decide


## Communicate
### Analytical vs. FEA
### Pin Hole
### Lessons Learned
What I learned
I learned that even though an assumed value may satisfy the numerical range given in the assignment, using an actual material property from the provided source makes the design more accurate and better supported. I also learned that material properties used in the analytical calculations should match the properties used in the CAD and FEA models.


Actual Time Spent
CAD Files

