# A6 – Parametric Design and Engineering Drawing

## Objective

The objective of A6 was to continue the bracket design from A5 and turn the previous design into a parametric CAD model and a detailed engineering drawing

In A5, I analyzed the bracket using strength and stiffness calculations and selected dimensions that satisfied the design requirements. In A6, I used those dimensions to build and organize the bracket in SolidWorks using Global Variables and equations. I then used the completed model to create a multi-view engineering drawing with dimensions and tolerances

The main goals for this assignment were to:

-Continue the bracket design from A5

-Create the bracket as a parametric SolidWorks model

-Use equations and Global Variables to control important dimensions

-Document the modeling process for each feature

-Verify that the model responds correctly when parameters are changed

-Create a fully dimensioned multi-view engineering drawing

-Apply appropriate tolerances to functional and non-critical features

-Document the design process, mistakes, and lessons learned

-Provide downloadable CAD files


<img width="1230" height="794" alt="image" src="https://github.com/user-attachments/assets/2c4fbfea-9542-408b-b658-e99f4e8d615e" />


## Analyze

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

<img width="2938" height="1908" alt="image" src="https://github.com/user-attachments/assets/d478e591-5e39-4a76-be96-8c761c77a1fa" />



**Creating Feature A**

I began the CAD modeling process with Feature A. I created the sketch for the first section of the bracket and used the dimensions determined from A5 to define the geometry.

The main dimensions controlling Feature A were the diameter and length.

The diameter was especially important because it was connected to the stiffness requirement from the previous assignment.

The initial diameter used in the parametric calculation was determined using the stiffness equation. The calculated required diameter was approximately 0.99 in, and the final nominal CAD dimension was selected as 1.00 in.

After completing the sketch, I used a Boss-Extrude feature to create the solid geometry.

<img width="3200" height="1900" alt="image" src="https://github.com/user-attachments/assets/f7d594ab-bc64-48c0-837c-90ffbc326ad9" />

<img width="2906" height="1898" alt="image" src="https://github.com/user-attachments/assets/d96c1cfe-2f55-4504-92d3-5c459ba0ba9d" />


**Creating Feature B**

After creating Feature A, I created the next sketch for Feature B.

Feature B was modeled to connect to the first section of the bracket. I used the dimensions selected during the A5 design process and constrained the sketch before creating the solid feature.

The main dimensions for Feature B were:

Width = 1.00 in
Height = 2.00 in
Thickness/extrusion = 0.50 in

The width of Feature B was later connected parametrically to the Feature A diameter using the relationship:

W_B = D_A

This means that the width of Feature B can automatically follow the diameter parameter of Feature A which is 0.99

After completing the sketch, I created the solid geometry using Boss-Extrude.

<img width="2938" height="1906" alt="image" src="https://github.com/user-attachments/assets/4e181259-1898-44b6-8a83-2f80b2022ecf" />

<img width="2936" height="1910" alt="image" src="https://github.com/user-attachments/assets/a34a084e-9e5a-44fa-8b3f-f2f7a280b7bb" />


**Creating Feature C**

Next, I created the sketch for Feature C. This feature forms the main horizontal portion of the bracket.

The main dimensions used for Feature C were:

Length = 4.00 in
Height = 0.625 in
Thickness/extrusion = 0.50 in

I added the necessary sketch dimensions and constraints before creating the solid feature.

After the sketch was completed, I used Boss-Extrude to create the three-dimensional Feature C.

The thickness of Feature C was also linked to the main thickness parameter:

t_C = t_B

<img width="2912" height="1900" alt="image" src="https://github.com/user-attachments/assets/7962d131-4013-438f-8379-c03615e126ab" />


This allows the thickness of Feature C to update automatically if the main thickness parameter is changed.

<img width="2932" height="1906" alt="image" src="https://github.com/user-attachments/assets/d2af68ed-df73-404d-9fc1-4eade3c4795a" />

<img width="2916" height="1892" alt="image" src="https://github.com/user-attachments/assets/b8903c8a-3403-44ed-b1f9-f0841cbea9a5" />


**Creating Feature D**

After Feature C, I created the sketch for Feature D.

Feature D is the vertical section located between the upper and lower portions of the bracket. I used the dimensions from the design and constrained the sketch before extruding it.

The main dimensions associated with Feature D were:

Length = 1.50 in
Width = 0.25 in
Thickness/extrusion = 0.50 in

The vertical height of Feature D was also represented parametrically.

The overall height of this portion of the bracket was set to 1.50 in, while Feature C has a height of 0.625 in. Therefore, the height of Feature D was represented by:

H_D = H_total - h_C

With the current dimensions:

H_D = 1.50 - 0.625

which gives approximately:

H_D = 0.875 in

This relationship allows the height of Feature D to update if the related dimensions change

After completing the sketch, I used Boss-Extrude to create Feature D.

<img width="2930" height="1906" alt="image" src="https://github.com/user-attachments/assets/e71c4acc-abbd-431e-9982-0d8f08d10f14" />

<img width="2908" height="1894" alt="image" src="https://github.com/user-attachments/assets/f6682d05-2cc0-4761-854f-41f8cdc540d3" />


**Creating Feature E**

The final major section was Feature E.

I created the sketch for the upper section of the bracket and used the dimensions selected from the previous design.

The main dimensions for Feature E were:

Length = 1.50 in
Height = 0.375 in
Thickness/extrusion = 0.50 in

After adding the required sketch dimensions and constraints, I used Boss-Extrude to create the solid feature.

The thickness was linked to the main thickness parameter using:

t_E = t_B

This keeps the thickness of Feature E connected to the other major thickness dimensions.

<img width="2928" height="1904" alt="image" src="https://github.com/user-attachments/assets/de63dfc1-f229-4d3b-a69c-f46476ccd014" />

<img width="2938" height="1900" alt="image" src="https://github.com/user-attachments/assets/ebabbc0c-26d2-4a73-b880-4279c1255e6a" />



### Parametric Verification

After entering the Global Variables, I tested the model to make sure the relationships were actually controlling the geometry.

For the test, I temporarily changed one of the parameters and rebuilt the model. The corresponding feature changed with the parameter instead of requiring the geometry to be manually redrawn.

For example, the thickness relationship between Features B, C, D, and E means that changing the main thickness variable can update the other features automatically.


### Mistakes During Modeling

One mistake occurred while entering the Feature A stiffness equation.

I initially entered the exponent without correctly grouping the entire expression. SolidWorks therefore evaluated the equation incorrectly and produced an incorrect diameter.

I corrected the equation by placing the entire expression inside parentheses before applying the (1/4) exponent:

=((8*"SF"*"F"*"L_A"^3)/("E"*PI()*"def"))^(1/4)

After correcting the equation, SolidWorks produced the expected result of approximately 0.99 in.

This showed me that equation formatting is important when using CAD software because a small syntax error can change the calculated result.

## Decide

### Final CAD Design

After completing the sketches, extrusions, and parametric relationships, I reviewed the complete bracket to make sure the features were connected correctly and the final dimensions matched the design selected from A5.

The final model uses the following main dimensions:

`Feature A diameter: 1.00 in`
`Feature A length: 2.00 in`
`Feature B width: 1.00 in`
`Feature B height: 2.00 in`
`Feature B thickness: 0.50 in`
`Feature C length: 4.00 in`
`Feature C height: 0.625 in`
`Feature C thickness: 0.50 in`
`Feature D length: 1.50 in`
`Feature D width: 0.25 in`
`Feature D thickness: 0.50 in`
`Feature E length: 1.50 in`
`Feature E height: 0.375 in`
`Feature E thickness: 0.50 in`

The final CAD model was kept connected to the Global Variables so that the important dimensions could be modified without rebuilding the entire part manually.

<img width="2930" height="1894" alt="image" src="https://github.com/user-attachments/assets/88b3a916-9706-4cd5-81d8-fd02042f5eb6" />

<img width="2922" height="1910" alt="image" src="https://github.com/user-attachments/assets/7f747fc0-2fc9-4396-be22-2d987fd75d06" />


### Engineering Drawing Plan

After completing the parametric model, the next step was to create the engineering drawing.

I planned to use a third-angle projection layout and include the necessary orthographic views to communicate the complete geometry of the bracket.

The drawing will include:

Front view
Top view
Right-side view
Additional view if necessary to clearly communicate the geometry
Complete dimensions
Functional gap dimensions
Tolerances
Tolerance block
Third-angle projection symbol
Title block

The tolerance block required for the drawing is:

X.X     ± .02
X.XX    ± .01
X.XXX   ± .005

The tolerances will be selected based on the function of each feature. Dimensions associated with mating or sliding-fit surfaces require more control than dimensions that do not affect assembly or function.

[IMAGE 18 – Drawing layout before dimensioning]

## Communicate

### Engineering Drawing

I created the engineering drawing from the completed parametric SolidWorks model. The drawing communicates the geometry and manufacturing dimensions of the bracket through multiple orthographic views.

The drawing uses third-angle projection and includes the dimensions required to fully define the bracket.

Here's the completed engineering drawing

<img width="2122" height="1564" alt="image" src="https://github.com/user-attachments/assets/a36b0c5a-6499-484c-807e-adee13301a16" />


### Drawing Features

The completed drawing includes:

Third-angle projection

Multiple orthographic views

Overall dimensions

Feature dimensions

Functional gap dimensions

Appropriate dimensional tolerances

Tolerance block

Title block

The tolerance block specifies:

- X.X ± 0.02
- X.XX ± 0.01
- X.XXX ± 0.005 

The drawing was created from the final parametric model so that the dimensions shown on the drawing correspond to the CAD geometry.


### CAD File Submission

**CAD Part File:**  

(Parametric Bracket Part)[https://raw.githubusercontent.com/Rama-H/megr2157-portfolio/refs/heads/main/docs/assignments/A5%20Bracket%201.SLDPRT]

**Engineering Drawing:**  

(Bracket Drawing)[https://raw.githubusercontent.com/Rama-H/megr2157-portfolio/refs/heads/main/docs/assignments/A6_Bracket%20drw.SLDDRW]

The part file contains the final parametric model, including the Global Variables and equations used to control the design. SolidWorks allows global variables and equations to control dimensions and relationships between features, so changing a linked variable can update the dependent dimensions and geometry. 

### Lessons Learned

One of the main things I learned from A6 was how parametric modeling connects engineering calculations to CAD geometry. Instead of treating every dimension as an independent number, I was able to create relationships between dimensions using Global Variables and equations.

The Feature A diameter was the clearest example. I entered the stiffness equation into SolidWorks, which produced a required diameter of approximately 0.99 in. I then selected a final nominal CAD diameter of 1.00 in.

I also learned how parametric relationships can reduce the amount of manual work required when a design changes. For example, the thicknesses of Features C, D, and E were connected to the Feature B thickness. This allows a change to the main thickness parameter to propagate to the related features.

Another lesson was the importance of checking equations carefully. During the modeling process, I initially had an incorrect exponent format in the Feature A equation. After correcting the equation, SolidWorks evaluated the calculation correctly. This showed me that CAD equations need to be checked just like calculations done by hand.

The drawing portion also helped me understand how dimensions and tolerances communicate design intent. More important or functional dimensions require more control, while noncritical dimensions can use a looser tolerance. Using unnecessarily tight tolerances on every dimension can make manufacturing more difficult without providing a functional benefit.

### Tolerance Reflection

For the drawing, I used a tighter tolerance of **±0.005 in** on the three-decimal dimension **0.630 in**. This dimension was given tighter control because it is more important to maintaining the intended geometry of the bracket.

A looser tolerance of **±0.02 in** was used on the **0.50 in** dimension. This dimension does not require the same level of precision as the more closely controlled feature, so the looser tolerance is appropriate.

This showed me that tolerances should be selected based on the function of the feature rather than making every dimension as precise as possible.

### Time Spent

Total time spent on A6: 3 days




