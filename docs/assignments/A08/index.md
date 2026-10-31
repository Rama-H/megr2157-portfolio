# A8 – Gears

## Objective

The objective of this assignment was to design and analyze a two-piece gearbox that can be assembled and disassembled. The gearbox uses an 18-tooth pinion and a 48-tooth spur gear to transmit rotational motion and torque between two parallel shafts.

The design process included evaluating the strength of the input and output shafts, calculating journal bearing pressure, sliding velocity, and PV values, determining the required bearing wall thickness, selecting appropriate components, and designing a gearbox housing using SOLIDWORKS.

The final design was intended to provide sufficient clearance for the gears, proper support for the rotating shafts, and a practical method for assembling and disassembling the gearbox

<img width="1446" height="1092" alt="image" src="https://github.com/user-attachments/assets/d7b53928-f7af-44bf-867e-7c2b6797fbeb" />

**Design Specifications**


Gear ratio: 48:18 (equivalent to 24:9)

Output torque: 1.25 in·lbf

Output speed: 1100 rpm

Input shaft diameter: 0.125 in

Output shaft diameter: 0.250 in

Shaft length: 1.00 in for both shafts

Gear pressure angle: 20°

Gear train: Ideal, with negligible power losses

The shafts were designed to be press-fitted into their respective gear hubs and supported by sleeve bearings with an appropriate running or sliding fit.


## Analyze

<img width="762" height="960" alt="image" src="https://github.com/user-attachments/assets/1ff3c7b9-cb26-453e-a25c-3b95f606d2e7" />

The free-body diagram represents the torque transmitted through the input shaft and the opposing reaction torque. Using equilibrium and the torsion equation for a solid circular shaft:

<img width="763" height="960" alt="image" src="https://github.com/user-attachments/assets/dac29102-8d92-4ee4-95f2-98ebcccc833c" />

Using the von Mises yield criterion, the allowable shear stress is:

<img width="960" height="324" alt="image" src="https://github.com/user-attachments/assets/ae34a2c7-e2e2-4e16-be45-74338fc38ea5" />

**Result**: The calculated maximum shear stress is less than the allowable shear stress. Therefore, the specified 0.125-inch input shaft diameter is sufficient for the assumed material and torsional loading.

### Part 1(b): Output Shaft Strength Analysis

**Knowns:**  

Output shaft diameter: (d_{out}=0.250) in

Output shaft length: (L=1.00) in

Output torque: (T_{out}=1.25) in·lbf

Output speed: (N_{out}=1100) rpm

Assumed material: 1018 cold-drawn steel

Assumed yield strength: (S_y=53,700) psi

Factor of safety: (FS=2)

**Unknowns:** 

Maximum torsional shear stress

Allowable shear stress

Whether the output shaft diameter is sufficient


The free-body diagram shows the applied output torque and opposing reaction torque. The shaft is analyzed under pure torsion, consistent with the assignment's assumption that bending effects from the gear loading can be neglected

<img width="942" height="868" alt="image" src="https://github.com/user-attachments/assets/52e51a5b-3d50-4ebe-828b-434f4854db39" />

<img width="828" height="518" alt="image" src="https://github.com/user-attachments/assets/89935696-13df-488e-a981-fa7e5e3fb69f" />

**Result:** 407.44 psi < 15502 psi (PASS)

The specified 0.250-inch output shaft is sufficient under the assumed torsional loading. No increase in shaft diameter is required based on this analysis.


### Part 2(a): Journal Bearing Design and Performance

**Knowns:**

Input shaft diameter = 0.125 in

Output shaft diameter = 0.250 in

Bearing length = 0.250 in

Input shaft speed = 2933.33 rpm

Output shaft speed = 1100 rpm

Output torque = 1.25 in-lbf

Output gear pitch diameter = 1.000 in

Gear pressure angle = 20° 

**Unknowns:**

Tangential gear force (Ft)

Radial gear force (Fr)

Resultant gear force (F)

Bearing reaction force (R)

Bearing pressure (P)

Sliding velocity (V)

PV rating

Appropriate bearing material



**Free-Body Diagram and Gear Forces:**

The free-body diagram shows a shaft supported by two journal bearings, with the gear force acting between them. For this analysis, the gear load is assumed to act midway between the two bearings, so each bearing supports half of the total load

<img width="828" height="1041" alt="image" src="https://github.com/user-attachments/assets/d354b176-4afe-413a-abd7-a93a4f16c667" />


**Calculate the tangential gear force**

Ft = (2 × Torque) / Pitch Diameter

Ft = (2 × 1.25) / 1.000

Ft = 2.50 lbf

**Calculate the radial gear force**

Fr = Ft × tan(20°)

Fr = 2.50 × tan(20°)

Fr = 0.910 lbf

**Calculate the resultant gear force**

F = √(Ft² + Fr²)

F = √(2.50² + 0.910²)

F = 2.660 lbf

**Calculate the bearing reaction forces**

Reaction at Bearing A = Reaction at Bearing B = F / 2

R = 2.660 / 2

R = 1.330 lbf per bearing

#### Projected Bearing Pressure

The bearing pressure is calculated by dividing the bearing reaction force by the projected contact area.

P = Reaction Force / (Shaft Diameter × Bearing Length)

**Input Bearing:**

P_input = 1.330 / (0.125 × 0.250)

P_input = 42.56 psi

**Output Bearing:**

P_output = 1.330 / (0.250 × 0.250)

P_output = 21.28 psi

#### Sliding Velocity 
Sliding velocity represents the surface speed of the rotating shaft inside the bearing.

V = (π × Shaft Diameter × Rotational Speed) / 12

**Input Bearing:**

V_input = (3.1416 × 0.125 × 2933.33) / 12

V_input = 95.99 ft/min

**Output Bearing:**

V_output = (3.1416 × 0.250 × 1100) / 12

V_output = 71.99 ft/min

<img width="740" height="960" alt="image" src="https://github.com/user-attachments/assets/4fc637b2-08cb-4df6-b28a-ddd17a951c9b" />

#### PV Calculation

The PV value is the product of bearing pressure and sliding velocity. It is used to evaluate the operating conditions of a journal bearing.

PV = Pressure × Velocity

**Input Bearing:**

PV_input = 42.56 × 95.99

PV_input ≈ 4085 psi·ft/min

**Output Bearing:**

PV_output = 21.28 × 71.99

PV_output ≈ 1532 psi·ft/min

<img width="764" height="960" alt="image" src="https://github.com/user-attachments/assets/182d712a-0164-48e5-a935-05985751468b" />

#### Bearing Material Selection

Oil-embedded 841 bronze was selected as the proposed journal bearing material.

This material is commonly used for sleeve bearings because it contains oil within its porous structure, providing lubrication during shaft rotation.

The calculated pressure, velocity, and PV values must be compared with the allowable limits for the selected McMaster-Carr bearings and the material-selection table provided in lecture before confirming that the material is suitable

### Part 2(b): Journal Bearing Wall Thickness

**Knowns:** 

Input shaft diameter = 0.125 in

Output shaft diameter = 0.250 in

Input bearing outside diameter = 0.250 in

Output bearing outside diameter = 0.375 in

Input bearing pressure = 42.56 psi

Output bearing pressure = 21.28 psi

Proposed bearing material = Oil-embedded 841 bronze

**Unknowns:**

Required minimum bearing wall thickness

Actual bearing wall thickness

Whether the selected bearing wall thickness is sufficient

**Free-Body Diagram and Stress Analysis**

The free-body diagram shows the forces acting on the journal bearing as the shaft rotates inside it. The shaft applies contact pressure to the inner surface of the bearing, while the surrounding housing supports the outside of the bearing.

The bearing must have sufficient wall thickness to withstand the applied pressure without excessive deformation or failure.

The handwritten calculations show the preliminary stress analysis and the method used to investigate the required wall thickness.

<img width="763" height="960" alt="image" src="https://github.com/user-attachments/assets/f7bec588-da65-4b05-a6ab-5139ae1f29c0" />

<img width="743" height="960" alt="image" src="https://github.com/user-attachments/assets/7c4fe986-36c9-44ae-aa4c-506246d15329" />

Both proposed sleeve bearings have a nominal wall thickness of 0.0625 inches based on their dimensions.

The wall thickness calculation establishes the actual geometry of the selected bearings. However, the minimum thickness required to resist the applied stresses must be confirmed using the appropriate stress equation and material properties before the design can be considered fully verified.

### Part 3: Gear Geometry and Center Distance

**Knowns:**

Number of teeth on input pinion = 18

Number of teeth on output gear = 48

Diametral pitch = 48 teeth/in

Input pinion pitch diameter = 0.375 in

Output gear pitch diameter = 1.000 in

Pressure angle = 20°

**Unknowns:**

Required center distance between the two gears

Correct positioning of the shafts inside the gearbox

<img width="1406" height="1058" alt="image" src="https://github.com/user-attachments/assets/4afbbb6d-8743-4fc0-9a33-2bdebbf3e94e" />

The center distance is the distance between the centers of the input and output shafts.

For two external spur gears, the center distance is calculated by adding the pitch diameters and dividing the result by two.

Center Distance = (Pinion Pitch Diameter + Output Gear Pitch Diameter) / 2

Center Distance = (0.375 + 1.000) / 2

Center Distance = 1.375 / 2

Center Distance = 0.6875 in

The calculated center distance is 0.6875 inches. This value was used to determine the correct spacing between the input and output shafts in the SOLIDWORKS gearbox assembly.

Maintaining the correct center distance helps the gear teeth mesh properly and reduces the possibility of interference between the gears.

### Part 4: Gearbox Housing Design

**Knowns:**

Gear center distance = 0.6875 in

Input pinion outside diameter = approximately 0.42 in

Output gear outside diameter = approximately 1.04 in

Input shaft diameter = 0.125 in

Output shaft diameter = 0.250 in

Input and output shaft lengths = 1.00 in each

Two separate housing components are required

**Unknowns:**

Overall gearbox housing dimensions

Housing wall thickness

Clearance between the gears and housing

Locations of the bearing holes

Method of connecting the two housing halves


The preliminary sketches show the arrangement of the two spur gears inside the gearbox housing.

The smaller 18-tooth pinion is positioned beside the larger 48-tooth output gear. The distance between their centers is 0.6875 inches, as determined from the gear calculations.

The housing was designed to surround the gears while allowing sufficient space for the gears to rotate.

<img width="1392" height="1276" alt="image" src="https://github.com/user-attachments/assets/c2bae790-c31f-49d1-b99d-c9f3a9a51b0a" />



## Decide


## Communicate

