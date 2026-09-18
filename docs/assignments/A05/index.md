# A5 – Bracket Design

## Objective
The objective of this assignment was to design a bracket by analyzing its strength and stiffness
The goal was to determine the minimum dimensions required for each feature so that the bracket can safely support the applied load while keeping deflection below the required limit.

<img width="1180" height="910" alt="image" src="https://github.com/user-attachments/assets/e8bb5c71-9f9f-4460-801a-99f761d6877c" />

The bracket was divided into five features, labeled A through E. Each feature was analyzed separately using a free-body diagram, assumptions, algebraic equations, and numerical calculations.

<img width="1230" height="814" alt="image" src="https://github.com/user-attachments/assets/5f83baf0-fe55-416e-af7b-9863e0923544" />

The design requirements used for this analysis were:

Applied load: (F=600) lbf

Safety factor: (SF=4)

Maximum allowable deflection: (delta_{max}=0.005) in

Material: 6061-T6 aluminum

Yield strength: (S_y=40) ksi

Elastic modulus: (E=10,000,000) psi

Direct shear failure was neglected as instructed

Shear deflection was assumed to be negligible

Because the bracket is symmetric, the 600-lbf load was divided equally between the two sides:

<img width="721" height="960" alt="image" src="https://github.com/user-attachments/assets/786d3d77-fe5d-4644-92c8-3f853e4ec9a0" />


The material properties were obtained from Machinery's Handbook. The Handbook lists a typical yield strength of approximately 40 ksi for 6061-T6/T651 aluminum and gives aluminum's modulus of elasticity as approximately (10^7) psi. 

## Analyze
**Design Approach**
The bracket was separated into Features A, B, C, D, and E as shown in Appendix C. Appendix D provides the simplified strength-of-materials models for the first three features:
 
Feature A -> cantilever beam

Feature B -> axially loaded bar

Feature C -> simply supported beam with a concentrated load at the center

The load was transferred through the features so that the reaction from one feature became the loading condition for the next feature.

For each feature, I performed two analyses:

1) Stress analysis to determine the minimum dimension required to prevent yielding

3) Stiffness analysis to determine the minimum dimension required to keep deflection below 0.005 in


The final dimension for each feature was selected by comparing the stress-controlled and stiffness-controlled dimensions and choosing the larger value.


### Feature A – Cylindrical Cantilever

Feature A was modeled as a circular cantilever beam
Appendix D tells us to treat Feature A as a cantilever beam

I am designing Feature A as a cylindrical shaft with:

L_A=2.00 in

The 300-lbf half-load acts at the free end.


### A — Stress Analysis

**1. Known Values**

P=300 lbf  

L_A=2.00 in 

S_allow=10,000,000 psi

For a circular cross section:

<img width="846" height="360" alt="image" src="https://github.com/user-attachments/assets/c144d5c2-8d21-48d9-ab47-58054906653e" />


**2. Unknown**

Find the minimum diameter:  d_A


**3. Assumptions**

Feature A behaves as a cantilever

One end is fixed to Feature B

The 300-lbf load acts at the free end

Circular cross section

Static loading

Bending stress controls the design

Direct shear failure is ignored

**4. FBD**

<img width="828" height="452" alt="image" src="https://github.com/user-attachments/assets/e659499e-70f1-498f-ba46-389ce02db1e7" />


At the fixed end:  R=300 lbf

<img width="830" height="372" alt="image" src="https://github.com/user-attachments/assets/dad938af-e926-4576-bb45-f542df37fc28" />

**5.Algebraic Solution**

<img width="830" height="398" alt="image" src="https://github.com/user-attachments/assets/ff8a407d-236e-4563-90fa-c6e18932cf77" />

**6. Numerical Solution**

<img width="828" height="240" alt="image" src="https://github.com/user-attachments/assets/96ba29ab-4012-45e6-bcff-257411bc5ca9" />



### Feature A – Stiffness Analysis

**1. Known Values**

P=300 lbf  

L_A=2.00 in 

E=10,000 psi

Delta_max= 0.005 in

**2. Unknown**    d_A

**3. Assumptions**

Feature A behaves as a cantilever

The load acts at the free end

Small-deflection beam theory applies

Shear deflection is negligible

The maximum deflection occurs at the free end

**4. FBD**

<img width="488" height="300" alt="image" src="https://github.com/user-attachments/assets/d6402a74-6e2d-42de-a11a-a6ba7e70983c" />

**Algebraic Solution**

<img width="824" height="464" alt="image" src="https://github.com/user-attachments/assets/e76fe9e7-2e48-41d7-8f0b-6f50e5bb3fff" />


**Numerical Solution**

<img width="828" height="244" alt="image" src="https://github.com/user-attachments/assets/58d45b4c-6069-401d-b329-4798e27ba167" />

**Feature A Decision**

<img width="828" height="626" alt="image" src="https://github.com/user-attachments/assets/bbe23270-48b7-4413-9ce4-94caf22763db" />

Therefore, Feature A passes both the strength and stiffness requirements.

### Feature B – Stress Analysis

Appendix D says:

Treat Feature B as an axial loaded bar.

The 300-lbf reaction from Feature A is transferred into Feature B.

I'll use:  L_B=2.00 in

and a width of:

b_B=1.00 in

The unknown will be the thickness t_B


### B — Stress Analysis

**Known**

P_B=300 lbf

L_B=2.00 in

b_B=1.00 in

S_{allow}=10,000 psi

**Unknown**: tB  thickness of B

	​
​**Assumptions**

B is an axially loaded rectangular bar

Load is centered

Uniform cross section

No bending

Direct shear failure ignored

**FBD**

<img width="828" height="362" alt="image" src="https://github.com/user-attachments/assets/153d61d8-a35f-45ad-934e-a9c5dbdc0d6b" />



**Algebraic solution**

<img width="828" height="272" alt="image" src="https://github.com/user-attachments/assets/4b2437b9-d343-4030-a8ba-20ae2f67a5dd" />

**Numrical solution**

<img width="828" height="522" alt="image" src="https://github.com/user-attachments/assets/ba4dbab1-1733-45d9-b9b5-c63bc2fe8a6b" />

### B — Stiffness Analysis

**Known**

P_B=300 lbf

L_B=2.00 in

b_B=1.00 in

E=10,000 psi

Delta=0.005 in

**Unknown**   tB  thickness of B


**Assumptions**

Feature B carries an axial load

The load is centered

The material remains elastic

Shear deformation is negligible

**FBD**

<img width="718" height="302" alt="image" src="https://github.com/user-attachments/assets/d2b829e5-9c88-4af5-9da4-9a70eaee7e09" />


**Algebraic Solution**

<img width="828" height="337" alt="image" src="https://github.com/user-attachments/assets/e529ebd1-fe4d-4290-87ed-dca3abcd717c" />


**Numerical Solution**

<img width="830" height="474" alt="image" src="https://github.com/user-attachments/assets/6a6f59d8-7ec8-4beb-b360-e8c044ec60b1" />

**Feature B Decision**

<img width="826" height="440" alt="image" src="https://github.com/user-attachments/assets/7ad3ad65-8a3f-410b-8b9e-9ea5a192469b" />

Therefore, Feature B passes both requirements


### Feature C – Stress Analysis

Appendix D specifically says to treat C as:

a simply supported beam with a concentrated load at the center.

I'll use:

L_C=4.00 in 

b_C=1.00 in

and use the 300-lbf load at the center.


**Known**

P=300 lbf

L=4.00 in

b=1.00 in

S_allow=10,000 psi


**Unknown**   h_C

**Assumptions**

Feature C is simply supported

The concentrated load acts at the center

The beam has a rectangular cross section

The cross section is uniform

Direct shear failure is neglected

Shear deflection is negligible

**FBD**

<img width="828" height="396" alt="image" src="https://github.com/user-attachments/assets/882328df-9a10-4b5d-9228-09ac80966adf" />



**Algebraic & Numerical solution**

<img width="830" height="806" alt="image" src="https://github.com/user-attachments/assets/6ab4067a-8255-40ef-ba68-2f64d6f8173b" />


### C — Stiffness Analysis

**Known Values**


P=300 lbf

L=4.00 in

b=1.00 in

E=10,000,000 psi

delta=0.005 in

**Unknown**   h_C=?



**Assumptions**

The beam is simply supported

The load acts at the center

The cross section is rectangular

Shear deflection is negligible

Maximum deflection occurs at the center


**FBD**

<img width="482" height="246" alt="image" src="https://github.com/user-attachments/assets/f92be008-a3c1-4b8e-a6f5-159d9f168c2e" />


**Algebraic & Numerical Solution**

<img width="709" height="960" alt="image" src="https://github.com/user-attachments/assets/af05f83e-001e-4476-8e6b-f3277ea06aec" />


For a simply supported beam with a center load, the Handbook gives

<img width="1482" height="970" alt="image" src="https://github.com/user-attachments/assets/9574a1f8-15b0-41d9-bc7c-167d3ffaaa91" />

**Feature C Decision**

<img width="830" height="790" alt="image" src="https://github.com/user-attachments/assets/3fd0a9af-7ef7-4147-b00d-fc46dec3133a" />

Therefore, Feature C passes both requirements.


### Feature D – Stress Analysis

Feature D transfers the reaction from Feature C into the upper portion of the bracket.

Because the loading is symmetric, the reaction transferred from Feature C is:

P_D=150 lbf

For the preliminary model:

L_D=1.50 in


b_D=1.00 in

S_allow=10,000 psi

The unknown is the thickness (t_D)

**Assumptions**

Feature D is modeled as an axially loaded rectangular member

The load is centered

The cross section is uniform

Direct shear failure is neglected

Bending effects are neglected in this simplified model


**FBD**

<img width="828" height="524" alt="image" src="https://github.com/user-attachments/assets/8c0567fc-8232-482f-b69d-fdc930ad1d84" />


**Algebraic and Numerical Solution**

<img width="826" height="616" alt="image" src="https://github.com/user-attachments/assets/75a9dba0-47c2-41b4-9f25-74421ebbe607" />


### Feature D – Stiffness Analysis

**Known Values**

P=150 lbf

L=1.50 in

b=1.00 in

E=10,000,000 psi

delta=0.005 in

**Unknown**  t_D=?

**FBD**

<img width="458" height="278" alt="image" src="https://github.com/user-attachments/assets/2d908eb4-6ed9-4246-972c-53989c86d355" />



**Assumptions**

The same axial-bar assumptions used for Feature D stress analysis are used here.

**Algebraic Solution & Numerical Solution**

<img width="826" height="486" alt="image" src="https://github.com/user-attachments/assets/8f939148-df7d-4dca-9833-047736a4b4ae" />

**Feature D Decision**

Feature D passes both requirements
<img width="826" height="486" alt="image" src="https://github.com/user-attachments/assets/8f3d396a-250e-493b-a3cd-2da980018510" />


### Feature E – Stress Analysis

Feature E represents the upper bracket member that transfers the load from the support into the main bracket.

For the simplified model

P_E=150 lbf

L_E=1.50 in

b_E=1.00 in

S_allow=10,000 psi

The unknown dimension is (h_E)

**Assumptions**

Feature E is modeled as a rectangular cantilever

The load acts at the end of the member

The cross section is uniform

The material remains elastic

Direct shear failure is neglected

**FBD**

<img width="828" height="704" alt="image" src="https://github.com/user-attachments/assets/306a6537-b331-4a08-8ef2-f5bfc3c0d7ef" />



**Algebraic & Numerical Solution**

<img width="830" height="946" alt="image" src="https://github.com/user-attachments/assets/c171600f-bce5-4cc4-ac02-534f67ce90a1" />

### Feature E – Stiffness Analysis

**Known Values**

P=150 lbf

L=1.50 in

b=1.00 in

E=10,000,000 psi

delta=0.005 in

**Unknown** h_E=?


**Assumptions**

Feature E behaves as a cantilever.

The load acts at the free end.

The cross section is rectangular.

Shear deflection is negligible.

Small-deflection beam theory applies.


**FBD**

<img width="436" height="378" alt="image" src="https://github.com/user-attachments/assets/cdd95027-6591-471d-9be1-593191689568" />


**Algebraic & Numerical Solution**

<img width="757" height="960" alt="image" src="https://github.com/user-attachments/assets/e5a85cfd-e562-4af4-99ab-b19efd4d930b" />


**Feature E Decision**

<img width="822" height="434" alt="image" src="https://github.com/user-attachments/assets/7d9aceab-eff4-4381-9ca9-6235988e8a74" />


### Overall Stress and Stiffness Comparison

The calculated minimum dimensions were compared to determine which requirement controlled the design

| Feature | Stress Minimum | Stiffness Minimum | Initial Dimension      | Governing Requirement |
|---------|----------------|-------------------|-----------------------|------------------------|
| A       | 0.849 in       | 0.756 in          | 1.000 in diameter     | Stress                 |
| B       | 0.030 in       | 0.012 in          | 0.125 in              | Stress                 |
| C       | 0.600 in       | 0.577 in          | 0.625 in              | Stress                 |
| D       | 0.015 in       | 0.0045 in         | 0.125 in              | Stress                 |
| E       | 0.367 in       | 0.343 in          | 0.375 in              | Stress                 |

The final dimensions were rounded upward from the theoretical minimum dimensions to provide practical CAD dimensions and additional margin


### Initial CAD Design

After completing the initial calculations, I began creating the bracket in SolidWorks.

I created the model feature-by-feature instead of creating the entire bracket as one sketch. This allowed each feature to correspond to the calculations in the analysis
I used parameters 

<img width="1586" height="736" alt="image" src="https://github.com/user-attachments/assets/5fe30cc7-0468-4b3c-aba3-7beca35ebe64" />

**CAD Step 1 – Feature A**
I started with Feature A, the cylindrical portion of the bracket.

I created a sketch on the appropriate plane and drew a circle centered at the origin.

The initial diameter was:  D_A= 1.00in

<img width="3192" height="1902" alt="image" src="https://github.com/user-attachments/assets/2c33569f-3bb2-4321-adca-2f0a568fd5da" />

I then used Boss-Extrude to create the cylinder with a length of: 2.00in

<img width="3200" height="1906" alt="image" src="https://github.com/user-attachments/assets/dabb89c7-211a-4756-a82a-33635f831f69" />


**CAD Step 2 – Feature B**

After creating Feature A, I created the vertical support

I started a sketch on the appropriate face and created the rectangular profile for Feature B

The initial dimensions were:

t_B=0.125 or 0.13 in

h_B= 2.00in

W_B= 1.00in

<img width="3192" height="1900" alt="image" src="https://github.com/user-attachments/assets/695cc4d7-3aab-431b-928c-b2605ae361dd" />

<img width="3198" height="1902" alt="image" src="https://github.com/user-attachments/assets/7118328c-0944-4d47-a573-7b8a57d1f408" />


**CAD Step 3 – Feature C**
Next, I created the lower horizontal portion of the bracket.

The initial dimensions were:   L_C=4.00in    h_C=0.63in

The feature was created using a rectangular sketch and Boss-Extrude

<img width="3200" height="1908" alt="image" src="https://github.com/user-attachments/assets/5d922fd7-680b-41cf-90c5-75589c88fcbd" />

<img width="3196" height="1908" alt="image" src="https://github.com/user-attachments/assets/626e2d25-2392-4b5a-89fc-de073729ed6b" />


**CAD Step 4 – Feature D**

I then created the vertical end feature.

The initial dimensions were:  L_D= 1.50 in     t_D=0.13 in 

The sketch was placed on the appropriate face and then extruded to form the vertical end of the bracket

<img width="3164" height="1904" alt="image" src="https://github.com/user-attachments/assets/d57fd915-9fe7-4764-8c67-682517abcf73" />

<img width="3200" height="1896" alt="image" src="https://github.com/user-attachments/assets/029fdc96-f831-45dc-af8d-e908ef235df9" />


**CAD Step 5 – Feature E**

Finally, I created the upper horizontal feature.

The initial dimensions were

L_E= 1.50 in

h_E=0.38 in

This feature was created with another rectangular sketch and extrusion

<img width="3200" height="1902" alt="image" src="https://github.com/user-attachments/assets/8ac1d670-be15-429a-ac83-f5d26de3c3d0" />

<img width="3196" height="1914" alt="image" src="https://github.com/user-attachments/assets/1c79c488-80a5-49c8-a6e9-9a05d8106ad8" />


### Initial CAD Evaluation

After completing the first CAD model, I inspected the overall geometry.

Although the calculated dimensions satisfied the stress and stiffness requirements, the model appeared thinner than I expected, particularly at the 0.13-in-thick sections.

The initial model was technically based on the calculated minimum dimensions, but the visual inspection made me question whether the geometry provided enough practical structural margin.

<img width="3196" height="1910" alt="image" src="https://github.com/user-attachments/assets/d08b956f-e89a-40f3-a083-e9ed8436d109" />

<img width="3200" height="1906" alt="image" src="https://github.com/user-attachments/assets/f5ebcbaf-1ac4-4055-8347-da0f3e2c88cb" />


This was an important part of my design process because the first calculated solution was not automatically treated as the final CAD design. I used the initial model to evaluate the physical proportions and identify areas where additional material could be beneficial.


### Final Design Revision

After completing the initial CAD model, I reviewed the overall geometry and compared the physical appearance of the model with the calculated dimensions.

Although the initial dimensions satisfied the analytical calculations, some of the sections appeared very thin in the CAD model. In particular, the 0.13-in extrusion thickness made several features appear narrow compared with the rest of the bracket.

Rather than changing the entire design, I made a targeted geometry revision.

The following dimensions were changed:

| Feature      | Initial   | Final   |
|------------- |----------:|--------:|
| B thickness  | 0.13 in   | 0.50 in |
| C thickness  | 0.13 in   | 0.50 in |
| D thickness  | 0.13 in   | 0.50 in |
| D width      | 0.13 in   | 0.25 in |
| E thickness  | 0.13 in   | 0.50 in |


The other major dimensions remained unchanged.

The purpose of this revision was to increase the structural cross section without changing the overall design concept.

Increasing the thickness of the members increases the available cross-sectional area and, for bending members, increases the section modulus and moment of inertia. Therefore, the change provides additional resistance to stress and deflection compared with the thinner initial geometry.

I retained the original analytical calculations as the initial sizing basis rather than completely repeating the analysis for every feature after the CAD revision. The final geometry uses equal or larger structural thicknesses than the initial calculated design.

initial CAD Model:

<img width="3200" height="1906" alt="Screenshot 2026-09-17 225515" src="https://github.com/user-attachments/assets/ae64c6f5-eaaa-4f58-8997-22c486b214ed" />

Final CAD Model:

<img width="3160" height="1904" alt="image" src="https://github.com/user-attachments/assets/3579ef3e-0a00-405c-9fad-ce01cc5332e4" />

Final CAD Dimensions

The final bracket was modeled using the following dimensions

<img width="1754" height="854" alt="image" src="https://github.com/user-attachments/assets/764a9741-a415-434a-a0a8-ff307edad5ff" />


## Decide

### Final Design

After completing the stress and stiffness calculations and creating the CAD model, I selected the following final dimensions:

Feature A: 1.00-in diameter, 2.00-in length

Feature B: 1.00-in width, 2.00-in height, 0.50-in thickness

Feature C: 4.00-in length, 0.63-in height, 0.50-in thickness

Feature D: 1.50-in length, 0.25-in width, 0.50-in thickness

Feature E: 1.50-in length, 0.38-in height, 0.50-in thickness

The analytical calculations showed that the original design dimensions satisfied the stress and stiffness requirements. During CAD development, I increased the thickness of Features B, C, D, and E and increased the width of Feature D. These changes provided additional structural material while maintaining the original design concept

The final design was therefore selected based on both the analytical results and the physical review of the CAD model

### Final Stress Check

The original analytical stress calculations produced the following results:

|Feature	|Maximum Stress | Allowable Stress	| Result|
|-----------|---------------|-------------------|-------|
|A			|6.11 ksi		|10 ksi				|PASS	|
|B			|2.40 ksi		|10 ksi				|PASS	|
|C			|5.76 ksi		|10 ksi				|PASS	|
|D			|1.20 ksi		|10 ksi				|PASS	|
|E			|9.60 ksi		|10 ksi				|PASS	|


All calculated stresses were below the allowable stress.

The final CAD model also uses increased thicknesses for Features B–E, providing additional cross-sectional material compared with the initial geometry.

### Final Stiffness Check

The original stiffness calculations produced:

| Feature | Deflection   | Maximum Allowed | Result |
|--------|--------------:|----------------:|:------:|
| A      | 0.00163 in    | 0.005 in        | PASS   |
| B      | 0.00048 in    | 0.005 in        | PASS   |
| C      | 0.00313 in    | 0.005 in        | PASS   |
| D      | 0.00018 in    | 0.005 in        | PASS   |
| E      | 0.00384 in    | 0.005 in        | PASS   |


All calculated deflections were below the required maximum of 0.005 in.

The final CAD revision increased the thickness of Features B, C, D, and E, which increases their available cross-sectional stiffness relative to the initial 0.13-in-thick geometry


## Communicate

### Final Design Communication

The final bracket was created in SolidWorks using a feature-by-feature modeling approach. I started with the cylindrical Feature A and then built Features B, C, D, and E around it.

The CAD model was developed directly from the dimensions obtained from the stress and stiffness analysis.

One important part of the design process was recognizing that a mathematically acceptable dimension does not always produce a CAD model that looks structurally appropriate. The initial 0.13-in-thick sections technically satisfied the original calculations, but they appeared very thin in the CAD model

Instead of completely redesigning the bracket, I made a targeted revision by increasing the extrusion thicknesses to 0.50 in and increasing the width of Feature D to 0.25 in.

This allowed me to preserve the original calculations and design concept while producing a more substantial final CAD model

Isometrics View:

<img width="3166" height="1906" alt="image" src="https://github.com/user-attachments/assets/a5da5cfc-a25a-41e9-9ff6-fce0b83a64cd" />

Front View:

<img width="3200" height="1910" alt="image" src="https://github.com/user-attachments/assets/31de8a0f-40e8-4ccc-8f54-dddee6c6608f" />


Right View:

<img width="3200" height="1914" alt="image" src="https://github.com/user-attachments/assets/2fe87944-4f3f-427e-a6d1-72dd691b5ee6" />


Top View:

<img width="3200" height="1910" alt="image" src="https://github.com/user-attachments/assets/da33eba3-d486-4706-9080-87ca1e63c747" />


### Multiview Drawings

Two multiview drawings were created to communicate the final design.

**Stress Analysis Drawing**
The stress-analysis sketch shows the important dimensions used to determine the required structural sizes.

[INSERT IMAGE: Hand-drawn stress multiview sketch]

**Stiffness Analysis Drawing**
The stiffness-analysis sketch shows the dimensions used in the deflection calculations.

[INSERT IMAGE: Hand-drawn stiffness multiview sketch]


### Lessons Learned
#### Governing Failure Mode

The stress and stiffness calculations showed that the bracket satisfied both requirements. The largest calculated stress was associated with Feature E:

sigma_E=9.60 ksi

compared with the allowable stress of:

sigma_allow=10 ksi


The largest calculated deflection was also associated with Feature E:

delta_E=0.00384 in


compared with the maximum allowable deflection:

delta_max=0.005 in


Therefore, Feature E was one of the most critical features in the original analytical design because it had the highest calculated stress and deflection.

#### Error Propagation

The bracket features were not independent

The reaction force from one feature became the loading condition for another feature

This means that an error in an earlier calculation can affect the dimensions and calculations of later features

For example, an incorrect reaction force at Feature A could change the loading used for Feature B and then continue through the remaining bracket features

This showed me why it is important to check the FBD and equilibrium equations before moving on to the next feature.

#### Assumption Sensitivity

One important assumption was that direct shear failure could be neglected, as allowed by the assignment.

If shear were significant in the actual design, the calculated dimensions could change because the component would need to be checked for both bending/normal stress and shear stress.

Another important assumption was the use of simplified beam models. The actual bracket contains several connected features and is more complicated than an ideal beam. The beam models were useful for developing a first-order design, but a more detailed analysis such as FEA could be used to evaluate the final geometry more accurately.

### What I Learned

This assignment helped me understand the connection between strength calculations, stiffness calculations, and CAD design.

One of the main things I learned was that passing a stress calculation does not automatically mean that the CAD model looks or feels like a practical design. My first CAD version used thin 0.13-in sections, which were acceptable according to the initial calculations but appeared very thin when I looked at the completed model

I learned that increasing the cross-sectional dimensions can improve both strength and stiffness. For bending members, the moment of inertia and section modulus have a strong effect on the resulting stress and deflection

I also learned the importance of modeling the load path correctly. The force does not simply act on one feature; it travels through the bracket, meaning that the features must be analyzed in sequence

Finally, I learned how to connect an analytical model to an actual SolidWorks model. The calculations provided the starting dimensions, while the CAD model allowed me to visually evaluate and refine the final design

### Final CAD File

[A5 Bracket Design.SLDPRT](https://raw.githubusercontent.com/Rama-H/megr2157-portfolio/refs/heads/main/docs/assignments/A5%20Bracket%201.SLDPRT)


### Final Result
The final design satisfies the original analytical stress and stiffness requirements. The final CAD model also incorporates a geometry revision in which the thickness of Features B, C, D, and E was increased to 0.50 in and the width of Feature D was increased to 0.25 in

The final design therefore maintains the original analytical design basis while providing a more substantial physical geometry








