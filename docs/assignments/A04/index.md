# A4 – Motor Mount

## Objective

The objective of this assignment is to design a motor mount for a Brushed 24V DC Gear Motor with a 99.5:1 planetary gearbox. The motor mount consists of two main features: Feature 1, which supports and attaches to the motor, and Feature 2, which attaches the mount to rigid wall A.

Both features are analyzed using beam calculations for bending stress and deflection. The design must account for a safety factor of 3 and a maximum allowable deflection of 0.30 mm at the free end. The weight of the motor is neglected, and the applied shaft load is \(P=300\) N.

The final design will be modeled parametrically in CAD and will include appropriate clearance holes, structural features to reduce deflection, and a downloadable CAD file.

<img width="482" height="254" alt="image" src="https://github.com/user-attachments/assets/03bb26fd-a681-43ee-b9eb-0828c2acb076" />

<img width="1406" height="1250" alt="image" src="https://github.com/user-attachments/assets/f1bbf79b-a108-4f7f-b32d-83be5989578b" />


## Analyze

### Design Requirements
| Requirement                  | Value               |
|-----------------------------|---------------------|
| Applied force               | P = 300 N           |
| Safety factor               | n = 3               |
| Maximum allowable deflection| 0.30 mm             |
| Motor shaft diameter        | Ø6 mm               |
| Motor mounting holes        | 4 × M3              |
| Motor mounting-hole pattern | Ø22 mm bolt circle  |
| Bolt clearance holes        | Ø3.4 mm             |
| Allowed materials           | ABS, PETG, or PLA   |
| Motor weight                | Neglected           |

The motor mount was simplified into two beam-like features so that beam bending equations could be used to determine the required cross-sectional geometry

### Motor Dimensions

<img width="1518" height="688" alt="image" src="https://github.com/user-attachments/assets/276b3c02-80e2-4ddf-96b7-62838b775b54" />

The motor dimensions were taken from Appendix A of the assignment. Important dimensions for the motor mount include the Ø6 mm diameter shaft, four M3 mounting holes located on a Ø22 mm diameter bolt circle, and the Ø28 mm motor body.

### Material Properties

For the preliminary design, **ABS was selected** as the motor-mount material because it is one of the materials permitted by the assignment.

The provided ABS properties are ranges, so the lower-bound values were selected for a conservative analysis:
<img width="1670" height="906" alt="image" src="https://github.com/user-attachments/assets/4b0ee011-e1bb-40b0-bee1-609caa52a261" />

<img width="828" height="424" alt="image" src="https://github.com/user-attachments/assets/295e485a-f1f4-4d9d-baff-1b5cdec4f419" />


### Feature 1 – Motor Support

#### Known and Unknown Variables
**Known**: P = 300 N     n=3     δmax =0.30 mm       E = 2350 MPa       Sy = 45.2 MPa

**Unknown**:   b = beam width       h = beam thickness/height       I = area moment of inertia      sigma_max = maximum bending stress

δ = maximum deflection

<img width="828" height="147" alt="image" src="https://github.com/user-attachments/assets/bdccaf30-a8c7-4d99-bd9b-31a3a57cfaf1" />

Preliminary beam length:  L=50 mm

Why 50 mm?
Because the motor is relatively small, and a 50-mm-long supporting feature gives us enough room to mount the motor while keeping the beam reasonably compact

#### Assumptions
To simplify the analysis, Feature 1 was modeled as a rectangular cantilever beam. The fixed end was assumed to have zero deflection and zero slope. The motor weight was neglected as instructed. The applied force was modeled as a 300 N point load at the free end of the cantilever. An initial beam length of 50 mm was assumed for the preliminary analysis.

#### Free-Body Diagram
To simplify the analysis of Feature 1, I modeled the horizontal motor-supporting plate as a cantilever beam. The end attached to Feature 2 is treated as fixed, while the 300 N force from the motor is applied at the free end. The fixed support produces a vertical reaction force and a reaction moment.

<img width="828" height="374" alt="image" src="https://github.com/user-attachments/assets/b5f95509-0bed-4267-9b0f-ccfec7a0ac1a" />

From the free-body diagram, the vertical reaction at the fixed end is equal to the applied load. Taking moments about the fixed end gives the maximum bending moment, which occurs at the fixed end of the cantilever.

<img width="828" height="246" alt="image" src="https://github.com/user-attachments/assets/87a6d147-18e1-4f52-bcfa-91b6fcf1040d" />


#### Stress Analysis
The first design requirement was to make sure that Feature 1 can withstand the applied load without yielding. I used the beam bending stress equation to determine the required cross-sectional geometry. The design uses a safety factor of 3, so the allowable stress is the material yield strength divided by the safety factor.

<img width="725" height="960" alt="image" src="https://github.com/user-attachments/assets/5887438c-8ed8-4e96-8f7a-a01f70352485" />

For the rectangular cross-section, the area moment of inertia and the distance from the neutral axis to the outer surface were substituted into the bending stress equation. This resulted in an equation relating the beam width and thickness to the maximum bending stress.


#### Deflection Analysis
After checking the strength of the beam, I analyzed the deflection of Feature 1. The assignment limits the maximum deflection at the free end to 0.30 mm. I modeled Feature 1 as a cantilever beam with a point load at the free end and used the standard cantilever beam deflection equation.

<img width="725" height="960" alt="image" src="https://github.com/user-attachments/assets/148fe8b3-754b-4593-ae2c-cef7904771e4" />

I solved the deflection equation for the required area moment of inertia. This allowed me to determine how much bending stiffness the cross-section needs in order to keep the free-end deflection below the 0.30 mm requirement.

#### Numerical solution

The symbolic equations were then evaluated using the known loading, material properties, safety factor, and the assumed 50 mm cantilever length. I selected an initial beam width of 40 mm and solved for the minimum thickness required to satisfy the deflection requirement.

<img width="712" height="960" alt="image" src="https://github.com/user-attachments/assets/79220e86-bb72-45e3-ba00-cd555b3c71ef" />

The calculated minimum thickness was approximately 19.11 mm. Since this value is a calculated minimum, I rounded up to a practical dimension of 20 mm for the preliminary design. Rounding up provides additional stiffness and keeps the design above the minimum calculated requirement

#### Cross-Sectional Geometry
A rectangular cross-section was selected for the initial Feature 1 design because it provides a simple geometry that can be directly analyzed using the beam bending equations. The width was selected as 40 mm, which provides enough space for the motor mounting pattern, while the thickness was determined from the deflection requirement.

<img width="828" height="276" alt="image" src="https://github.com/user-attachments/assets/603dcd3b-e4f5-499e-9d52-945ee4292c86" />

The preliminary cross-sectional geometry for Feature 1 is therefore 40 mm wide by 20 mm thick. This geometry was then checked for bending stress, moment of inertia, and deflection to verify that it satisfies the design requirements.

**Moment of Inertia check:**

The calculated moment of inertia of the selected 40 mm × 20 mm rectangular section was compared with the minimum moment of inertia required from the deflection analysis. The actual value must be greater than or equal to the required value.

<img width="1564" height="292" alt="image" src="https://github.com/user-attachments/assets/4ddcc122-5338-4fa8-868c-e09f5be42d69" />

The selected cross-section satisfies the required moment of inertia for the deflection limit.

_Moment of Inertia: PASS_
	​


**Stress check:**

The selected cross-section was then checked to determine the maximum bending stress produced by the 300 N load. The calculated stress was compared with the allowable ABS stress after applying the required safety factor of 3.

<img width="828" height="254" alt="image" src="https://github.com/user-attachments/assets/2e0e2db8-9f6f-47ce-8b6d-a198b301b5d3" />

The maximum bending stress is below the allowable stress for ABS. Therefore, the preliminary Feature 1 design satisfies the yield-strength requirement.

_Stress: PASS_
	​

**Deflection check:**

Finally, I checked the actual free-end deflection of the selected 40 mm × 20 mm cross-section. The calculated deflection was compared with the maximum allowable deflection of 0.30 mm specified in the assignment.

<img width="828" height="254" alt="image" src="https://github.com/user-attachments/assets/15b2061b-8589-4641-8c83-050c29a8de04" />

The calculated deflection is below the maximum allowable deflection of 0.30 mm. Therefore, the preliminary Feature 1 design satisfies the deflection requirement.

_Deflection: PASS_

#### Feature 1 Results
| Parameter | Value |
|----------|--------|
| Material | ABS |
| Applied force, P | 300 N |
| Safety factor, n | 3 |
| Beam length, L | 50 mm* |
| Beam width, b | 40 mm |
| Beam thickness, h | 20 mm |
| Young’s modulus, E | 1790 MPa |
| Yield strength, Sy | 29.6 MPa |
| Allowable stress | 9.87 MPa |
| Max bending moment | 15,000 N·mm |
| Required I | 23,277.5 mm⁴ |
| Actual I | 26,666.7 mm⁴ |
| Max bending stress | 5.625 MPa |
| Max deflection | 0.262 mm |
| Stress requirement | PASS |
| Deflection requirement | PASS |

Based on the preliminary beam analysis, Feature 1 was designed using ABS and modeled as a rectangular cantilever beam. The selected preliminary cross-section is 40 mm wide and 20 mm thick. The calculated maximum bending stress is 5.625 MPa, which is below the allowable stress of 9.87 MPa. The calculated free-end deflection is approximately 0.262 mm, which is below the required maximum of 0.30 mm. Therefore, the preliminary Feature 1 geometry satisfies both the strength and deflection requirements


### Feature 2 – Wall Mount

#### Known and Unknown Variables
Feature 2 is the vertical portion of the motor mount that attaches to the rigid wall A using bolts. To simplify the analysis, the wall mount is modeled as a rectangular cantilever beam fixed at the wall. The loading transferred from Feature 1 consists of the 300 N motor load and the bending moment generated by the load acting through Feature 1.

Since the assignment does not specify the exact dimensions of Feature 2, reasonable dimensions were assumed for the preliminary beam analysis. These dimensions will be refined during the CAD design.

**Known variables:**
<p align="center"> p=300 N </p>
	
<p align="center">L_1=50 mm

<p align="center">H=50 mm

<p align="center">b=40 mm

<p align="center">E=1790 MPa

<p align="center">S_y=29.6 MPa

<p align="center">n=3

<p align="center">Delta_max=0.30 mm 

Where:

P = applied motor force

L_1 = Feature 1 length

H = assumed height of Feature 2

b = width of Feature 2

E = Young's modulus of ABS

S_y = ABS yield strength

n = safety factor

delta_max = maximum allowable deflection

**Unknown variables:**
The primary unknown is the required wall-mount thickness \(t\). The required cross-sectional area moment of inertia, bending stress, shear stress, and deflection will also be determined.

#### Assumptions
To make the analysis manageable using the beam equations discussed in lecture, Feature 2 was approximated as a rectangular cantilever beam attached to a rigid wall. The wall is assumed to be sufficiently rigid that its deformation can be neglected. The motor weight is neglected as instructed in the assignment. The bolts are assumed to provide a rigid attachment to the wall.

ABS is used for both features, with the lower-bound material properties selected for a conservative design. The width of Feature 2 is initially assumed to be 40 mm and its effective beam height is assumed to be 50 mm. The connection between Feature 1 and Feature 2 is assumed to transfer both the 300 N force and the bending moment generated by that force.

These assumptions are preliminary and will be revisited when the final CAD geometry is created.

#### Free-Body Diagram

The free-body diagram for Feature 2 shows the loading transferred from Feature 1 to the vertical wall mount. Feature 1 applies a 300 N vertical force to Feature 2. Because the 300 N force acts 50 mm from the wall, it also produces a bending moment at the Feature 1–Feature 2 connection. Feature 2 transfers these loads into the rigid wall through the bolted connection.

IMAGE

The 300 N motor force acting at the end of Feature 1 creates a bending moment at the connection between the two features. This moment is transferred into Feature 2 and must therefore be included in the wall-mount analysis.

#### Stress Analysis
The maximum bending moment occurs at the fixed connection to the wall. Feature 2 experiences the moment transferred from Feature 1 as well as the moment produced by the 300 N force acting over the assumed height of the wall mount. Therefore, the two moment contributions are combined to determine the maximum bending moment used for the stress design

#### Shear Analysis

In addition to bending, the wall mount experiences transverse shear from the 300 N motor load. I used the maximum shear-stress equation for a rectangular beam to check that the wall-mount cross-section has sufficient shear capacity


#### Deflection Analysis
The deflection of Feature 2 was evaluated using superposition. The first term represents the deflection caused by the 300 N force, while the second term represents the deflection caused by the bending moment transferred from Feature 1. The combined deflection must remain below the assignment limit of 0.30 mm

#### Cross-Sectional Geometry

The required thickness was determined independently from the bending-stress and deflection requirements. The stress analysis required approximately 21.35 mm, while the deflection analysis required approximately 27.56 mm. Since the design must satisfy both requirements, the larger value controls the preliminary design.


#### Feature 2 Results

## Decide

### Material Selection
### Final Dimensions
### Design Decisions
### Deflection-Minimizing Features
### Clearance Holes
### Design Changes / Mistakes

## Communicate

### Initial Concept Sketch
### Isometric Sketch
### CAD Model
### Parametric Modeling
### CAD Images
### Engineering Drawing
### CAD File Download
### Time Log
### Lessons Learned
### Appendix – Research
