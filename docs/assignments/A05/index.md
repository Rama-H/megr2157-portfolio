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
Direct shear failure was neglected as instructed.
Shear deflection was assumed to be negligible.

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

1) Stress analysis to determine the minimum dimension required to prevent yielding.
2) Stiffness analysis to determine the minimum dimension required to keep deflection below 0.005 in.

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
Feature A behaves as a cantilever.
One end is fixed to Feature B.
The 300-lbf load acts at the free end.
Circular cross section.
Static loading.
Bending stress controls the design.
Direct shear failure is ignored.

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
Feature A behaves as a cantilever.
The load acts at the free end.
Small-deflection beam theory applies.
Shear deflection is negligible.
The maximum deflection occurs at the free end.

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
Feature B carries an axial load.
The load is centered.
The material remains elastic.
Shear deformation is negligible

**FBD**

<img width="718" height="302" alt="image" src="https://github.com/user-attachments/assets/d2b829e5-9c88-4af5-9da4-9a70eaee7e09" />


**Algebraic Solution**

<img width="828" height="337" alt="image" src="https://github.com/user-attachments/assets/e529ebd1-fe4d-4290-87ed-dca3abcd717c" />


**Numerical Solution**

<img width="830" height="474" alt="image" src="https://github.com/user-attachments/assets/6a6f59d8-7ec8-4beb-b360-e8c044ec60b1" />

**Feature B Decision**

<img width="826" height="440" alt="image" src="https://github.com/user-attachments/assets/7ad3ad65-8a3f-410b-8b9e-9ea5a192469b" />

Therefore, Feature B passes both requirements.


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

| Feature | Stress Minimum | Stiffness Minimum | Final Dimension      | Governing Requirement |
|---------|----------------|-------------------|-----------------------|------------------------|
| A       | 0.849 in       | 0.756 in          | 1.000 in diameter     | Stress                 |
| B       | 0.030 in       | 0.012 in          | 0.125 in              | Stress                 |
| C       | 0.600 in       | 0.577 in          | 0.625 in              | Stress                 |
| D       | 0.015 in       | 0.0045 in         | 0.125 in              | Stress                 |
| E       | 0.367 in       | 0.343 in          | 0.375 in              | Stress                 |

The final dimensions were rounded upward from the theoretical minimum dimensions to provide practical CAD dimensions and additional margin

## Decide
### Final Design

Based on the stress and stiffness calculations, the final dimensions selected for the preliminary CAD model are:

Feature A: 1.000-in diameter

Feature B: 0.125-in thickness

Feature C: 0.625-in height

Feature D: 0.125-in thickness

Feature E: 0.375-in height

The final dimensions were selected by comparing the minimum dimensions required by stress and stiffness and choosing the larger value

**Final Stress Check**

| Feature | Final Maximum Stress | Allowable Stress | Result |
|---------|-----------------------|------------------|--------|
| A       | 6.11 ksi              | 10 ksi           | PASS   |
| B       | 2.40 ksi              | 10 ksi           | PASS   |
| C       | 5.76 ksi              | 10 ksi           | PASS   |
| D       | 1.20 ksi              | 10 ksi           | PASS   |
| E       | 9.60 ksi              | 10 ksi           | PASS   |


**Final Stiffness Check**

| Feature | Final Deflection | Maximum Allowed | Result |
|---------|-------------------|------------------|--------|
| A       | 0.00163 in        | 0.005 in         | PASS   |
| B       | 0.00048 in        | 0.005 in         | PASS   |
| C       | 0.00313 in        | 0.005 in         | PASS   |
| D       | 0.00018 in        | 0.005 in         | PASS   |
| E       | 0.00384 in        | 0.005 in         | PASS   |

The calculations show that all five features satisfy both the allowable stress and maximum deflection requirements



## Communicate

