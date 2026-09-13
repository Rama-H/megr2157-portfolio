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
p=300 N 
	
L_1=50 mm

H=50 mm

b=40 mm

E=1790 MPa

S_y=29.6 MPa

n=3

Delta_max=0.30 mm 

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
The primary unknown is the required wall-mount thickness (t). The required cross-sectional area moment of inertia, bending stress, shear stress, and deflection will also be determined.


#### Assumptions
To make the analysis manageable using the beam equations discussed in lecture, Feature 2 was approximated as a rectangular cantilever beam attached to a rigid wall. The wall is assumed to be sufficiently rigid that its deformation can be neglected. The motor weight is neglected as instructed in the assignment. The bolts are assumed to provide a rigid attachment to the wall.

ABS is used for both features, with the lower-bound material properties selected for a conservative design. The width of Feature 2 is initially assumed to be 40 mm and its effective beam height is assumed to be 50 mm. The connection between Feature 1 and Feature 2 is assumed to transfer both the 300 N force and the bending moment generated by that force.

These assumptions are preliminary and will be revisited when the final CAD geometry is created.


#### Free-Body Diagram

The free-body diagram for Feature 2 shows the loading transferred from Feature 1 to the vertical wall mount. Feature 1 applies a 300 N vertical force to Feature 2. Because the 300 N force acts 50 mm from the wall, it also produces a bending moment at the Feature 1–Feature 2 connection. Feature 2 transfers these loads into the rigid wall through the bolted connection.

<img width="828" height="606" alt="image" src="https://github.com/user-attachments/assets/4602710b-6064-4b9b-ada5-1f96cd7e1557" />


The 300 N motor force acting at the end of Feature 1 creates a bending moment at the connection between the two features. This moment is transferred into Feature 2 and must therefore be included in the wall-mount analysis.


#### Stress Analysis

<img width="828" height="343" alt="image" src="https://github.com/user-attachments/assets/8dbed333-609e-407e-98a1-ce2e2658e9c1" />

The maximum bending moment occurs at the fixed connection to the wall. Feature 2 experiences the moment transferred from Feature 1 as well as the moment produced by the 300 N force acting over the assumed height of the wall mount. Therefore, the two moment contributions are combined to determine the maximum bending moment used for the stress design

<img width="832" height="606" alt="image" src="https://github.com/user-attachments/assets/c50c0d42-f016-41e5-8c95-de33e0873739" />

Allowable Stress

<img width="1274" height="788" alt="image" src="https://github.com/user-attachments/assets/049310ce-ca5e-43d0-b69a-1ab6f7ddc1ba" />

So the stress requirement alone gives:   t_stress ≈ 21.35 mm


#### Shear Analysis

In addition to bending, the wall mount experiences transverse shear from the 300 N motor load. I used the maximum shear-stress equation for a rectangular beam to check that the wall-mount cross-section has sufficient shear capacity

<img width="828" height="840" alt="image" src="https://github.com/user-attachments/assets/f3a85c36-b264-46e1-854d-209b9f4bb886" />

The shear calculation requires a minimum thickness of approximately 1.97 mm, which is much smaller than the thickness required by the bending-stress calculation. Therefore, bending stress controls the preliminary wall-mount thickness.


#### Deflection Analysis

Because Feature 2 is subjected to both a force and a transferred moment, the total deflection can be approximated by adding the deflections caused by each load.

For a cantilever with a point force at the free end:

<img width="828" height="162" alt="image" src="https://github.com/user-attachments/assets/b15421f7-c2eb-4d2d-9686-e41b85564ee7" />

For a cantilever with an applied end moment:

<img width="828" height="162" alt="image" src="https://github.com/user-attachments/assets/ca7ddd19-3677-42db-9f71-663d32267833" />

<img width="828" height="162" alt="image" src="https://github.com/user-attachments/assets/0039bdc8-f6d3-4716-8c72-b9cb0995f399" />

The deflection of Feature 2 was evaluated using superposition. The first term represents the deflection caused by the 300 N force, while the second term represents the deflection caused by the bending moment transferred from Feature 1. The combined deflection must remain below the assignment limit of 0.30 mm

<img width="826" height="556" alt="image" src="https://github.com/user-attachments/assets/8d713f78-50b5-414b-b34f-1f22b972eea6" />



#### Cross-Sectional Geometry

<img width="828" height="450" alt="image" src="https://github.com/user-attachments/assets/4d117a36-bdf5-44c3-aa59-8f4a9484577b" />

The required thickness was determined independently from the bending-stress and deflection requirements. The stress analysis required approximately 21.35 mm, while the deflection analysis required approximately 27.56 mm. Since the design must satisfy both requirements, the larger value controls the preliminary design.

Therefore, round upward to a practical CAD dimension:  t=30 mm

So our preliminary Feature 2 cross-section is:

**40 mm wide × 30 mm thick**

**Moment of Inertia Check**
After determining the minimum thickness from the deflection requirement, I selected a practical thickness of 30 mm. The resulting moment of inertia was then checked against the required value.

<img width="828" height="666" alt="image" src="https://github.com/user-attachments/assets/198d79c7-4122-4f7c-847b-84cce2584797" />

**Stress Check**

The bending stress was recalculated using the selected 40 mm × 30 mm cross-section. The resulting stress was compared with the allowable ABS stress of 9.87 MPa.

<img width="2283" height="1249" alt="IMG_2477" src="https://github.com/user-attachments/assets/601fa26a-95f8-48c8-8216-293b4b530b69" />


**Shear Check**
The selected cross-section was also checked for transverse shear. The calculated maximum shear stress was compared with the conservative allowable shear stress estimated from the ABS yield strength using the von Mises criterion.

<img width="2794" height="1040" alt="IMG_2478" src="https://github.com/user-attachments/assets/058d18b0-f1b4-48f3-b135-daf7acdca61b" />


**Deflection Check**
Finally, the deflection of the selected 40 mm × 30 mm cross-section was calculated. The total deflection includes the contribution from both the 300 N force and the moment transferred from Feature 1.

<img width="2200" height="1714" alt="IMG_2479" src="https://github.com/user-attachments/assets/f4614f4a-9683-49c2-895d-65587c84b97c" />


#### Feature 2 Results

The preliminary analysis of Feature 2 resulted in a 40 mm wide × 30 mm thick rectangular cross-section. The design was evaluated for bending stress, transverse shear, and deflection using the conservative lower-bound ABS material properties. The selected geometry produces a maximum bending stress of 5.00 MPa, a maximum shear stress of 0.375 MPa, and an estimated total deflection of approximately 0.233 mm. All three values are below their respective allowable limits. Therefore, the preliminary Feature 2 geometry satisfies the analytical requirements.


| Design Check                | Requirement   | Calculated     | Result |
|-----------------------------|--------------:|---------------:|:------:|
| Bending stress              | ≤ 9.87 MPa    | **5.00 MPa**   |  PASS |
| Shear stress                | ≤ 5.70 MPa    | **0.375 MPa**  |  PASS |
| Moment of inertia           | ≥ 69,832 mm⁴  | **90,000 mm⁴** |  PASS |
| Deflection                  | ≤ 0.30 mm     | **0.233 mm**   |  PASS |
| Final preliminary thickness | —             | **30 mm**      |  PASS |


## Decide

### Material Selection
ABS was selected as the material for the motor mount because it is one of the materials permitted by the assignment and provides sufficient strength and stiffness for the calculated loading. For a conservative design, the lower-bound values of the provided material-property ranges were used. The Young's modulus was taken as 1.79 GPa and the tensile yield strength as 29.6 MPa. With a safety factor of 3, the allowable tensile stress is 9.87 MPa.

### Final Dimensions
Right now the analytical preliminary dimensions are

| Feature   | Width | Thickness |
|---------- |------:|----------:|
| Feature 1 | 40 mm |     20 mm |
| Feature 2 | 40 mm |     30 mm |

The beam calculations provided the starting dimensions for the CAD model. Feature 1 was analytically sized to 40 mm × 20 mm, while Feature 2 was sized to 40 mm × 30 mm. These dimensions will be incorporated into the CAD model and adjusted where necessary to accommodate the motor geometry, mounting bolts, shaft clearance, and structural reinforcement


### Design Decisions
After completing the analytical calculations, I converted the beam dimensions into a practical motor-mount design.

The final design uses an L-shaped bracket. Feature 1 supports the motor, while Feature 2 attaches the mount to the wall.

I added the motor mounting-hole pattern based on the motor's mounting geometry. The motor mounting holes were modeled as 3.4 mm diameter clearance holes.

I also added a central shaft opening to provide clearance for the motor shaft.

The wall plate was designed with four mounting holes. The four holes were positioned using a Linear Sketch Pattern, with:

20 mm horizontal spacing
20 mm vertical spacing
3.4 mm hole diameter

This made the hole layout easier to control and helped keep the wall mounting pattern symmetric.

<img width="2906" height="1908" alt="image" src="https://github.com/user-attachments/assets/a4c55d08-4ef7-4245-a448-7eb9442939d6" />



### Deflection-Minimizing Features
To improve the stiffness of the mount, I added two triangular gussets between the horizontal motor-supporting section and the vertical wall plate.

**Gusset Design – Initial Attempt**

One of the mistakes I made during the CAD process was how I created the gussets.

My first approach was to manually draw a right triangle using individual sketch lines on both sides of the mount. I then extruded the triangular profiles to create the supports.

After doing this, I realized that SOLIDWORKS already has a dedicated Gusset feature that can create this type of reinforcement much more directly.

I changed my approach and used the Gusset tool instead.

The final gussets were:

25mm horizontal x 25mm vertical x 5mm thick

This made the modeling process cleaner and more appropriate for the intended design.

<img width="2922" height="1910" alt="image" src="https://github.com/user-attachments/assets/623507bd-9ae9-47d0-9503-e5f212ef09d5" />

The purpose of the gussets is to provide additional support at the region where the horizontal and vertical sections meet. This reduces bending of the horizontal section and increases the stiffness of the bracket.

**Fillets**

I added small fillets to the mount to remove sharp edges and improve the transition between surfaces.

The fillet radius used was: R=0.50 mm

The fillets also provide a smoother transition at the corners and help reduce sharp geometric discontinuities.

### Clearance Holes
Clearance holes were included for the motor-mounting bolts. The assignment specifies 3.4 mm diameter clearance holes for the bolts, so Ø3.4 mm holes were used in the CAD model. The shaft opening was also sized according to the motor dimensions provided in Appendix A

<img width="1532" height="730" alt="image" src="https://github.com/user-attachments/assets/3167c32a-00f8-44ac-8dcb-6584b3223928" />


**Motor Mounting Holes**
I created the motor mounting-hole pattern.

The motor mounting holes were modeled as: 3.4 mm diameter

This provides clearance for the required M3 bolts

The holes were positioned according to the motor's mounting-hole pattern

A central opening was also added for the motor shaft:  6.3 mm diameter. This provides clearance around the motor shaft

<img width="2912" height="1896" alt="image" src="https://github.com/user-attachments/assets/e68f87ac-a110-4203-8706-63d7fcd7ba9f" />

<img width="2914" height="1802" alt="image" src="https://github.com/user-attachments/assets/1d86a6e9-a7a9-4de2-9c09-99b2d107790e" />


**Wall Mounting Holes**

The wall plate was then modified to include four mounting holes.

Each hole has a diameter of: 3.4 mm

I used a Linear Sketch Pattern to create the four holes instead of manually sketching each hole.

The horizontal spacing was:

20 mm 

and the vertical spacing was:

20 mm

This helped maintain consistent spacing between the holes and made the design more parametric.

<img width="2916" height="1904" alt="image" src="https://github.com/user-attachments/assets/c305c95b-dfcc-43ef-bda8-a1764a56011f" />

### Design Changes / Mistakes
During the CAD process, I encountered several issues that required me to make changes.

**1. Wall Plate Extrusion**

My first wall-plate sketch was created with the incorrect orientation, which caused the 30 mm extrusion to extend in the wrong direction.

I corrected this by creating the sketch on the appropriate vertical face and reversing the extrusion direction.

**2. Manual Gusset Creation**

Initially, I created the gussets manually by drawing right triangles with sketch lines on both sides of the mount and extruding them.

After realizing that SOLIDWORKS has a dedicated Gusset feature, I changed the design and used the built-in tool instead.

This was faster and produced a cleaner feature.

**3. Fillets**

After creating the main geometry and gussets, I added 0.50 mm fillets to smooth the sharp edges and improve the final appearance of the mount.

**4. Material Setup for FEA**

Initially, the material properties shown in the simulation did not match the conservative ABS values I intended to use. I corrected the material definition so that the simulation used:

E=1790 MPa  and   S_y=29.6 MPa

I then reran the FEA with the corrected material

## Communicate

### Initial Concept Sketch
### Isometric Sketch
### CAD Model

**FEA Validation**
After completing the CAD model, I used SOLIDWORKS Simulation to validate the design. The simulation was set up as a static study using ABS as the assigned material.

The applied force was: F=300N

<img width="2922" height="1902" alt="image" src="https://github.com/user-attachments/assets/b2f4344b-29d2-4cb8-a614-0d4ab23c7ccf" />


The wall side of the mount was fixed to represent attachment to a rigid wall.

<img width="1898" height="1342" alt="image" src="https://github.com/user-attachments/assets/c7429639-e89b-48ab-bd5f-d5c35d5f1ddf" />


**FEA Material Setup**

The ABS material was assigned using:

E=1790 MPa    S_y=29.6 MPa

The material properties were manually entered into the SOLIDWORKS material definition so that the simulation matched the values used in the analytical calculations.

<img width="2926" height="1900" alt="image" src="https://github.com/user-attachments/assets/590b0726-0603-43ff-af06-530e37fc644c" />


**Von Mises Stress Result**

The maximum Von Mises stress from the FEA was:

$$ \boxed{\sigma_{VM,max}=6.884\text{ MPa}} $$

The allowable stress based on the safety factor of 3 was:

$$ \sigma_{allow}= \frac{29.6}{3} $$ $$ \boxed{\sigma_{allow}=9.87\text{ MPa}} $$

Comparing the results:

$$ 6.884<9.87\text{ MPa} $$

Therefore:

$$ \boxed{\text{PASS}} $$

The highest stress occurred near the transition between the horizontal section and the reinforced wall region, which is reasonable because this is where the bending load is transferred through the bracket.

<img width="3200" height="1904" alt="image" src="https://github.com/user-attachments/assets/bfb73fe7-438a-4edd-ab98-327e38c4f967" />

<img width="3200" height="1908" alt="image" src="https://github.com/user-attachments/assets/dbf64a01-6f1e-4cf4-a9f7-93701aba01de" />

<img width="3182" height="1902" alt="image" src="https://github.com/user-attachments/assets/4585b1c5-9e11-4820-9728-4c917cd5b0a8" />


**FEA Displacement Result**

The maximum displacement reported by SOLIDWORKS was:

$$ 0.00017825\text{ m} $$

Converting to millimeters:

$$ 0.00017825(1000) $$ $$ \boxed{\delta_{max}=0.17825\text{ mm}} $$

The assignment limit was:

$$ \boxed{0.30\text{ mm}} $$

Therefore:

$$ 0.17825<0.30 $$ $$ \boxed{\text{PASS}} $$

The deformation displayed in the SOLIDWORKS screenshot is visually exaggerated so that the deformation can be seen. The displayed deformation shape is not the actual physical amount of deformation.

<img width="3200" height="1904" alt="image" src="https://github.com/user-attachments/assets/a1e37512-de65-4859-aaed-b336700e4e90" />


**Factor of Safety**

The minimum factor of safety can be calculated from the maximum Von Mises stress:

$$ FOS=\frac{S_y}{\sigma_{VM,max}} $$ $$ FOS=\frac{29.6}{6.884} $$ $$ \boxed{FOS\approx4.30} $$

The required factor of safety was:

$$ \boxed{FOS\geq3} $$

Since:

$$ 4.30>3 $$

the final design satisfies the required safety factor.


### Parametric Modeling
The model was created using dimensions and features that can be edited in SOLIDWORKS.

Important dimensions were defined parametrically, including:

<img width="2908" height="1904" alt="image" src="https://github.com/user-attachments/assets/b34228d7-7acd-4e3b-a775-868add7ccfbf" />

Using parametric dimensions allows the model to be modified without rebuilding the entire part

### Engineering Drawing
### CAD File Download
### Time Log
### Lessons Learned

This project helped me understand how analytical engineering calculations can be translated into an actual CAD design.

One of the main things I learned was that the dimensions calculated from beam equations provide a starting point, but the final design also has to consider practical features such as mounting holes, motor clearance, wall attachment, gussets, and fillets.

I also learned that CAD problems are sometimes caused by the way a sketch is created rather than by the dimension itself. For example, I initially created the wall plate on the wrong orientation, which caused the extrusion to go in the wrong direction.

Another thing I learned was how to use built-in SOLIDWORKS features more effectively. I originally created the gussets manually using triangular sketches and extrusions. After realizing that SOLIDWORKS has a dedicated Gusset feature, I changed my approach and used that tool instead.

The FEA portion also showed me the importance of using the correct material properties. I had to make sure that the ABS material in SOLIDWORKS matched the conservative values used in my calculations before trusting the simulation results.

Finally, I learned that the analytical calculations and FEA serve different purposes. The beam equations allowed me to determine reasonable starting dimensions, while FEA allowed me to evaluate the actual CAD geometry, including the holes, gussets, and fillets.

Overall, the final design satisfied the required stress, deflection, and safety-factor constraints.

