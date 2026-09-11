# A4 – Motor Mount

## Objective

The objective of this assignment is to design a motor mount for a Brushed 24V DC Gear Motor with a 99.5:1 planetary gearbox. The motor mount consists of two main features: Feature 1, which supports and attaches to the motor, and Feature 2, which attaches the mount to rigid wall A.

Both features are analyzed using beam calculations for bending stress and deflection. The design must account for a safety factor of 3 and a maximum allowable deflection of 0.30 mm at the free end. The weight of the motor is neglected, and the applied shaft load is \(P=300\) N.

The final design will be modeled parametrically in CAD and will include appropriate clearance holes, structural features to reduce deflection, and a downloadable CAD file.

<img width="482" height="254" alt="image" src="https://github.com/user-attachments/assets/03bb26fd-a681-43ee-b9eb-0828c2acb076" />

<img width="1406" height="1250" alt="image" src="https://github.com/user-attachments/assets/f1bbf79b-a108-4f7f-b32d-83be5989578b" />


## Analyze

### Design Requirements

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
<img width="828" height="374" alt="image" src="https://github.com/user-attachments/assets/b5f95509-0bed-4267-9b0f-ccfec7a0ac1a" />

#### Stress Analysis
<img width="725" height="960" alt="image" src="https://github.com/user-attachments/assets/5887438c-8ed8-4e96-8f7a-a01f70352485" />

#### Deflection Analysis
<img width="725" height="960" alt="image" src="https://github.com/user-attachments/assets/148fe8b3-754b-4593-ae2c-cef7904771e4" />

#### Cross-Sectional Geometry
#### Feature 1 Results

### Feature 2 – Wall Mount

#### Known and Unknown Variables
#### Assumptions
#### Free-Body Diagram
#### Stress Analysis
#### Shear Analysis
#### Deflection Analysis
#### Cross-Sectional Geometry
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
