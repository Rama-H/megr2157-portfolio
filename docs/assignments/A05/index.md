# A5 – [Topic]

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

S_allow=10,000 psi

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

<img width="828" height="368" alt="image" src="https://github.com/user-attachments/assets/02db6069-17a8-4268-b3cd-8a792e7e9396" />

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

<img width="828" height="368" alt="image" src="https://github.com/user-attachments/assets/02db6069-17a8-4268-b3cd-8a792e7e9396" /> 

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

<img width="830" height="538" alt="image" src="https://github.com/user-attachments/assets/0ebf23de-ffea-4f13-96bf-56c6b1bf3ec3" />


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

<img width="830" height="538" alt="image" src="https://github.com/user-attachments/assets/0ebf23de-ffea-4f13-96bf-56c6b1bf3ec3" />

**Algebraic Solution**

<img width="828" height="337" alt="image" src="https://github.com/user-attachments/assets/e529ebd1-fe4d-4290-87ed-dca3abcd717c" />


**Numerical Solution**

<img width="830" height="474" alt="image" src="https://github.com/user-attachments/assets/6a6f59d8-7ec8-4beb-b360-e8c044ec60b1" />

**Feature B Decision**

<img width="826" height="440" alt="image" src="https://github.com/user-attachments/assets/7ad3ad65-8a3f-410b-8b9e-9ea5a192469b" />

Therefore, Feature B passes both requirements.


### Feature C – Stress Analysis

## Decide


## Communicate

