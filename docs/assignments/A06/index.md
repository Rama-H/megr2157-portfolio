# A6 – Parametric Design and Engineering Drawing

## Objective

The objective of this assignment was to continue the bracket design from A5 by converting the model into a parametric CAD model and creating a detailed multi-view engineering drawing.

The main goals were to:

- Create a parametric solid model using SolidWorks Global Variables and equations
  
- Connect important CAD dimensions to the design calculations from A5
  
- Allow dimensions to update automatically when a related parameter changes
  
- Create a fully dimensioned engineering drawing of the bracket
  
- Apply appropriate tolerances to the drawing

- Use third-angle projection
  
- Document the design process, including calculations, CAD work, mistakes, and lessons learned
  
- Provide a downloadable CAD file for the completed design

The bracket was carried forward from the previous assignment, where strength and stiffness requirements were analyzed. For A6, those design decisions were incorporated into the CAD model so that important dimensions could be controlled parametrically instead of being entered only as fixed values

<img width="1290" height="826" alt="image" src="https://github.com/user-attachments/assets/9abbc736-dcb4-4ff0-b0d6-a47c787bc6bf" />

My A5 finished CAD design 

<img width="2850" height="1896" alt="image" src="https://github.com/user-attachments/assets/a77cdd38-36d6-442a-ae2a-3ae016f292b1" />


### Parametric Design Process

I began A6 by continuing from the bracket model created in A5. Instead of keeping the important dimensions as independent values, I created Global Variables in SolidWorks to control the major dimensions of the bracket

The main design inputs used in the parametric model were the total applied force, safety factor, allowable deflection, material properties, and the dimensions selected during the previous assignment

The main design inputs were:

| Parameter | Value |
|---|---:|
| Total applied force, F | 600 lbf |
| Symmetric half-load, P | 300 lbf |
| Safety factor, SF | 4 |
| Yield strength, Sy | 40,000 psi |
| Modulus of elasticity, E | 10,000,000 psi |
| Maximum allowable deflection | 0.005 in |


### Parametric Variables

I created Global Variables for the major dimensions of the bracket. These variables control the geometry instead of requiring each dimension to be manually changed.

The main geometric variables include:

- `L_A = 2.00 in`
- `D_A = 1.00 in`
- `W_B = D_A`
- `t_B = 0.50 in`
- `h_B = 2.00 in`
- `L_C = 4.00 in`
- `h_C = 0.625 in`
- `t_C = t_B`
- `L_D = 1.50 in`
- `W_D = 0.25 in`
- `H_total = 1.50 in`
- `H_D = H_total - h_C`
- `L_E = 1.50 in`
- `h_E = 0.375 in`
- `t_E = t_B`

The relationships between the thickness variables allow several features to remain connected. For example, `t_C`, `t_D`, and `t_E` are linked to `t_B`. Therefore, changing the main thickness parameter can update the other corresponding features automatically.

<img width="1772" height="894" alt="image" src="https://github.com/user-attachments/assets/ce2c0d08-a224-4165-9af3-eeb5119f2ca7" />

<img width="1820" height="1036" alt="image" src="https://github.com/user-attachments/assets/2c21554f-c0ae-427d-8c88-2e222730e82e" />




## Analyze


## Decide


## Communicate

