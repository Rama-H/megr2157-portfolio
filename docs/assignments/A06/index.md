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

### Analytical Equation Used in the Parametric Model

One of the main dimensions driven by an analytical equation was the diameter of Feature A.

The stiffness relationship used was:

D_A = ({8(SF)(F)L_A^3} / {(E)pi(delta)})^{1/4}


The equation was entered directly into SolidWorks as:

=((8*"SF"*"F"*"L_A"^3)/("E"*PI()*"def"))^(1/4)

The calculation produced a required diameter of approximately 0.99 in.

Rather than manually calculating the value outside of CAD and entering it as an unrelated dimension, the equation was entered directly into the SolidWorks Global Variables table. This allowed the required diameter to respond to changes in the design inputs

<img width="1398" height="470" alt="image" src="https://github.com/user-attachments/assets/690ec2e6-841a-429f-aa15-d14d04ab6ca4" />

**Parametric Relationships**

Additional relationships were created between dimensions so that the model could update when a parameter changed.

For example:

"W_B" = "D_A"

This makes the width of Feature B dependent on the diameter parameter of Feature A.

The thicknesses were also related:

"t_C" = "t_B"
"t_D" = "t_B"
"t_E" = "t_B"

The height of Feature D was related to the overall height and Feature C height:

"H_D" = "H_total" - "h_C"

Using these relationships made the model easier to modify because related dimensions did not have to be changed individually.

[INSERT IMAGE: Screenshot of the bracket with several dimensions visible]

**Parametric Verification**

After creating the Global Variables, I verified that the model responded to changes in the parameters. A dimension was temporarily changed in the Global Variables table and the model was rebuilt to confirm that the corresponding geometry updated.

After verifying the relationship, the value was returned to the intended design dimension.

[INSERT IMAGE: Before changing a parameter]

[INSERT IMAGE: After changing the parameter and showing the model update]

Mistakes and Corrections

One issue occurred while entering the Feature A stiffness equation. The exponent was initially entered without grouping the entire exponent correctly. This caused SolidWorks to evaluate the equation incorrectly and produce an incorrect diameter.

I corrected the equation by placing the exponent inside parentheses:

=((8*"SF"*"F"*"L_A"^3)/("E"*PI()*"def"))^(1/4)

After correcting the equation, SolidWorks evaluated the required diameter at approximately 0.99 in.

Another design decision was separating the calculated required diameter from the final nominal CAD dimension. The analytical calculation resulted in approximately 0.99 in, while the final model uses a 1.00-in diameter.

This allowed the analytical result to remain documented while using the selected nominal dimension in the final CAD model.

## Analyze


## Decide

### Final CAD Design


## Communicate

