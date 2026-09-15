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


## Decide


## Communicate

