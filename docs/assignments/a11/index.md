# A11 – Motor Selection (Team Project) 

## Member 1: Pierce Brown

### Motor Selection and Attachments - Part 1
#### Objective
The objective of part 1 was to select a gear-motor for each lead screw using torque and speed requirements from the previous assignment, A10. Document the motor's rated output torque, speed, efficiency, voltage, current, and mounting. Use the motor's torque-speed curve to verify the motors can handle the 2kN total test load across the 1-50mm/min speed range with the required safety factor of 4. 

#### Analyze
<img width="955" height="438" alt="image" src="https://github.com/user-attachments/assets/6ca56df2-92ea-48b4-9b4c-9862d3f5ea56" />

The McMaster-Carr 4855N17 gear motor is listed as base mounted. It has a 1/2 ich diameter by 1 inch long keyed output shaft. The reference drawing also shows four #10-32 face holes on a 2.645 by 2.645 inch pattern.

Using the 2.54mm/rev screw lead from A10, the required cross-head speed of 1-50 mm/min corresponds to 0.394-19.685 rpm per motor. The operating thread torque from A10 is 1.36 N*m per screw. Applying the requires safety factor I got a torque of Td = 5.44 N*m or 48.1 lbf*in. 

<img width="748" height="567" alt="image" src="https://github.com/user-attachments/assets/dd9c7e8f-f04f-4140-8896-dbf6662e0823" />
<img width="751" height="574" alt="image" src="https://github.com/user-attachments/assets/948478c9-c1e8-4681-bbd2-a9b42f47f1f5" />

at the maximum required speed of 19.685 rpm, the 90 V DC torque-speed chart shows around 80-85 lbf*in per moor. This exceeds the required design torque of 48.1 lbf*in per motor, which includes the safety factor of 4. The plotted torque stays above the design requirement throughout the 0.394-19.685 rpm range, supporting the selection of motor 4855N17. https://www.mcmaster.com/4855N17/

### Design Floating Bearing Mount 
#### Objective 

Design a mounting bearing that supports the lower end of the lead screw while allowing it to rotate and move axially. Use a RC3 Fit between the bore and the screw end, and justify the mount dimensions and hole locations. 
    
#### Analyze 


The proposed mount is 80 mm long by 40 mm wide by 15.88 mm thick, with one mount per leadscrew. Viewed from above, the bore center is 40 mm from the left short edge and 20 mm from the bottom long edge. The two M8 clearance-hole centers are 15mm and 65 mm from the same short edge, both 20 mm from the bottom long edge The mounting holes are 2 x 9.00-9.22 mm through for normal M8 clearance. The proposed 15.88 mm (0.625 in) thickness provides 0.500 in of nominal screw engagement and leaves the screw tip 0.125 in short of the bottom face. 


<img width="1000" height="544" alt="image" src="https://github.com/user-attachments/assets/eed8df94-933c-4a15-b032-d0edd5d51908" />

For the selected 0.3750 in basic diameter, the RC3 fit gives an H7 bore of 0.3750-0.3756 in and an f6 screw end of 0.3741-0.3745 in. Using these, the diametrical clearance is calculated as 0.0005-0.0015 inch clearance. 

### Lessons Learned

I learned to check a gearmotor's available torque, the relationship between speed and torque via a speed-torque graph, and that the efficiency estimate depends on using electrical input and mechanical output. I also learned how to use RC3 fit tables to set bore and shaft diameter limits, and how to check clearance at both tolerance extremes. Overall I spent roughly 5 hours on gathering the needed information, calculating, and compiling the work done into the portfolio. 


## Member 2: Rama Hamid

## Objective

The objective of this assignment was to design and analyze the motor mounting bracket, shaft coupler, and frame connections for our dual-leadscrew tensile testing machine. The components were designed to support the required loading, transmit motor torque, and maintain proper alignment while considering the required safety factor of 4

## Analyze

### section 2- Motor Mount Bracket Design

For the motor mounting bracket, we selected 6061-T6 aluminum because it offers good strength, low weight, and ease of machining. We proposed a 6.35 mm (1/4 in) thick mounting plate with four holes corresponding to the motor's mounting pattern. We used bearing stress analysis to determine the minimum required plate thickness under the applied motor torque

#### Knowns & Unknowns

<img width="1180" height="568" alt="image" src="https://github.com/user-attachments/assets/97d8d138-e5cf-4ed6-b407-e4d8d111bf23" />

#### FBD & handwritten calculations 
<img width="768" height="960" alt="image" src="https://github.com/user-attachments/assets/703c154e-de98-47a3-8354-aa443f2009ad" />

<img width="1544" height="1542" alt="image" src="https://github.com/user-attachments/assets/b475d392-c851-4c97-b9f4-d4a2414ba65a" />

<img width="828" height="576" alt="image" src="https://github.com/user-attachments/assets/af45dd9e-2e03-4819-81f3-f891f90c0dfb" />

The calculated minimum thickness was approximately 0.086 mm for the simplified bolt bearing-stress model. We selected a thicker 6.35 mm plate to provide a more practical and rigid mounting surface. This thickness satisfies the preliminary bearing-stress check, although bracket bending, frame attachment loads, and deflection still require verification.

source: https://www.mcmaster.com/4855N17/

### Section 3- Coupler Design

The coupler connects the motor output shaft to the leadscrew and transfers the torque required to operate the tensile testing machine. We initially analyzed a hollow cylindrical coupler using 6061-T6 aluminum to estimate the minimum outer diameter and wall thickness. We then selected a commercially available flexible coupling to accommodate small shaft misalignments and simplify assembly

#### Knowns & Unknowns

<img width="1184" height="880" alt="image" src="https://github.com/user-attachments/assets/176ee0d1-b9a0-417c-b733-6e25d33590da" />

<img width="1176" height="590" alt="image" src="https://github.com/user-attachments/assets/2dea67bc-87ce-4b7c-97ac-86ea53b1715b" />

#### FBD & handwritten calculations

<img width="828" height="812" alt="image" src="https://github.com/user-attachments/assets/c5bb2b8a-25fb-4427-8d82-b907ebd106a3" />

<img width="828" height="902" alt="image" src="https://github.com/user-attachments/assets/0eae6f5b-6c03-47e3-86c1-43ce89521211" />

<img width="3172" height="1640" alt="image" src="https://github.com/user-attachments/assets/b5b95761-de36-4bb7-a566-722d4ce8bdae" />

We selected McMaster-Carr Precision Flexible Shaft Coupling #6208K569 as our preliminary coupler. It has two 12.70 mm (1/2 in) bores, a 31.75 mm outer diameter, and a 31.75 mm overall length. Its maximum rated torque of 9.49 N·m exceeds our design torque of 5.44 N·m. We chose this coupling because its flexible design accommodates small misalignments and its clamp-on mounting simplifies assembly. The motor's keyed shaft and the leadscrew coupling end still need to be checked for compatibility


Our preliminary cylindrical analysis gave a minimum wall thickness of approximately 0.133 mm, and we initially proposed a 6.35 mm wall thickness. These calculations helped establish a preliminary design, but they do not directly represent the stress distribution in the purchased spiral-cut coupling. Therefore, the manufacturer's published torque rating was used for the preliminary product selection.

source: https://www.mcmaster.com/6208K569/


### Section 4- Frame Twist and T-Slot Connector Design

For the frame connections, we proposed heavy 40 Series aluminum T-slot framing with an 80 × 40 mm top profile and a preliminary support spacing of 400 mm. We analyzed the vertical reactions and twisting moments produced by the two motors to determine the loading that must be resisted at the frame connections. Symmetric loading and equal sharing of the motor reaction torques were assumed for the preliminary analysis


#### Knowns & Unknowns

<img width="1180" height="1116" alt="image" src="https://github.com/user-attachments/assets/791174bf-200c-4a9b-bde5-e34d6a06fa72" />


<img width="1178" height="636" alt="image" src="https://github.com/user-attachments/assets/aecfa39e-8286-48fb-abe2-93e0b0be73f0" />


#### FBD & handwritten calculations


<img width="828" height="909" alt="image" src="https://github.com/user-attachments/assets/245533e1-fb57-40da-bc72-afedc4ad5f3e" />


<img width="1642" height="1336" alt="image" src="https://github.com/user-attachments/assets/219d6b6a-ebe8-4ea9-abd3-1f0b200381f4" />


<img width="3070" height="1620" alt="image" src="https://github.com/user-attachments/assets/72ee13ea-b775-456d-be89-281590ef3c3d" />


<img width="2118" height="1524" alt="image" src="https://github.com/user-attachments/assets/59fcf3ac-ba3d-4536-93d1-99928e7db4ed" />


We selected the 80/20 Gusseted Inside-Corner Bracket, Grainger Item #5JRU3 (manufacturer model 40-4338), as our preliminary frame connector. The bracket is compatible with 40 Series T-slot framing and has eight mounting holes, allowing multiple fastening points. Its gusseted design was chosen to provide additional rigidity at the connection between the top beam and vertical supports. Grainger also lists a compatible M8 bolt and T-slot nut assembly, Item #5JRH6

The preliminary analysis gave vertical reactions of 1000 N and torsional reactions of 5.44 N·m at each support under the assumed loading conditions. The manufacturer's drawing confirmed a 40 mm spacing between mounting-hole columns, which was used as an assumed effective lever arm to calculate a 136 N force couple. The final fastener forces and connector capacity still require verification based on the actual bracket arrangement and loading direction

sources: 

Grainger product page: https://www.grainger.com/product/80-20-Inside-Corner-Bracket-Gusseted-5JRU3

Grainger dimension drawing:  https://www.grainger.com/ec/pdf/grainger-5jru3.pdf

### Cost Tables

Bill of Materials:

<img width="863" height="218" alt="Screenshot 2026-11-23 222122" src="https://github.com/user-attachments/assets/39b65a6e-0df4-44f5-b08e-bfa61bff8ab1" />

<img width="361" height="225" alt="Screenshot 2026-11-23 220615" src="https://github.com/user-attachments/assets/cef529fb-f6f0-4943-8fee-bd3f5014f0ea" />

Design Production Cost:

<img width="234" height="99" alt="Screenshot 2026-11-23 222033" src="https://github.com/user-attachments/assets/0d93c411-c0e0-47d3-a524-2057e711e502" />


### Lessons Learned 

Through this assignment, I learned how to apply bearing stress, torsional shear stress, and equilibrium equations to the design of mechanical components. I also learned that theoretical minimum dimensions are not always the most practical choices, since rigidity, alignment, assembly, and manufacturer specifications must also be considered. This assignment helped me understand how the motor mount, coupler, and frame connections work together in the tensile testing machine.


**_Time spent: 5 hours_**




## Member 3: Bridget Fagan

### Click [here](https://github.com/user-attachments/files/35306960/A11.FEA.zip) to download the CAD files.

## Objective

The objective of this part of the assignment was to conduct simulations on the tensile tester assembly to verify that the assembly would survive its application. To do this, we had to apply meshes of three different sizes to the model and run the same study for convergence. The entire frame is made from aluminum with the exception of the steel lead screws. There are two parts to this section. The first part involves testing the top rail to ensure it can withstand the torque and axial loads of the lead screws. The second part involves testing the side rails for the same criteria.

## Analyze

### Section 5


#### Model Setup

Part 5 required the testing of the top of the frame against the applied torque from the motor as well as the axial force through the lead screws. To set up the model, I removed the crosshead assembly including the nut and flange and the lead screws. The crosshead assembly does not affect the results of the study, and the lead screws do not mesh correctly in coarser sizes. To get around this, I removed the lead screws and instead applied the axial force around the rim of the hole the lead screw was in. The hole has a sharp corner, and from the results of my first study with a coarse mesh, the maximum stress occurred at those corners. This would be concerning if not for the fact that the lead screw is not directly mounted to the top of the frame in the way that is described. 

The feet of the frame and the faces of the frame top were fixed as shown which emulates the standard loading conditions of a simply supported beam. I conducted the study this way to understand the worst possible case of loading, and I found that the maximum stress was within the elastic region for aluminum, at 4.86 x 10^7 N/m^2.

<img width="614" height="266" alt="Screenshot 2026-11-23 151244" src="https://github.com/user-attachments/assets/d7496c0e-a6f6-49d3-9284-773b77886e4d" />

The deflection results showed that the maximum deflection occurred in the center of the rail. If the lead screws were in the assembly, they would provide minimal support to the rail in the center to reduce the deflection. There was no unusual bending or warping in the study, the beam behaved as expected. The end faces were what kept the rail behaving normally. The deflection effects of the load peaked in the center of the beam.


## Communicate

#### Meshing and Results

I used three different mesh sizes in this part (coarse, medium, fine) with the aim to achieve a result that converges. I tested each size of mesh for convergence and on the three required criteria (stress, displacement, safety factor) using the following table:

<img width="348" height="62" alt="Screenshot 2026-11-23 193940" src="https://github.com/user-attachments/assets/76fe59cd-2c21-4937-99a6-ca3b802254d1" />

I found that increasing the mesh size led to divergence within the results, which was not unexpected. 

#### Optimization Suggestions

To optimize the model of the frame top, I would suggest adding fillets or chamfers around the holes in the rail. This will reduce stress around the hole and prevent edge degradation through use. To reduce the large deflection in the center, I would install the gusseted brackets discussed in Part 4 between the top rail and side rails to increase the support from the ends.

Using a fine mesh may create more accurate results, however it takes more computing power and time. I would suggest using a medium mesh as a midpoint between computation time and accuracy.


### Section 6

## Analyze

#### Model Setup

***_Note: Due to constraints on computing power and Random Access Memory, the results of this study were not convergent and produced results that were massively variant. As such, the results can not be interpreted the same way as Section 5. Additionally, the study is missing features, which could not be avoided_

Constraining this assembly involved removing all members besides the side rails and the top rail. I fixed the end faces of the top rail and applied compression loads down the side rails equivalent to the 1kN loads through the lead screws and a transverse load applied from the center of the assembly towards the outside. 

## Communicate

#### Meshing and Results

I ran into issues running the simulation with finer meshes as my computer did not have enough memory to run the simulation. I had to adjust by removing the top rail and motor brackets, and applying the loads directly to the side rails, illustrated below.


Iteration 1 (Coarse Mesh):

<img width="484" height="299" alt="Screenshot 2026-11-23 162123" src="https://github.com/user-attachments/assets/567b95cd-9c51-4075-b4a4-40a002fc9f7c" />


Iteration 3 (Fine Mesh):

<img width="460" height="302" alt="Screenshot 2026-11-23 175607" src="https://github.com/user-attachments/assets/d1fccb27-3bda-4251-aa8a-77facaedd597" />


The filled out results table is below:

<img width="347" height="62" alt="Screenshot 2026-11-23 193945" src="https://github.com/user-attachments/assets/ed3ef683-cfd8-434f-a1c3-de8f2b8e70f8" />

The results of this study proved that the rails would not fail under the loads from the lead screws and motors. The most dangerous parameter is deflection, which peaked at 0.19 m. The Von Mises stress peaked at 1.782 x 10^7 N/m^2 which is well within the limit of aluminum. The load path acted along the length of the rail as anticipated, however the transverse loading caused the rails to deflect outwards from the center.

The omission of certain parts of the assembly dramatically affected the results of the study. The motor brackets were not present in any of the simulations, and the top rail was absent for the fine mesh run. This caused the side rails to deflect higher up than expected, as there was no top rail to fix them. Additionally, the motor brackets would have allowed the torque and stresses to be transmitted via the interface between the bracket and top rail, instead of in the generalized location that the simulation was conducted with. I understand that the study is therefore incorrect, however, there was no way around this outcome.


#### Optimization Suggestions

There weren't many issues that were encountered with the side rails, however with the inclusion of the bracket mentioned above in Section 5, the rails would remain more stable when load is applied. Beyond the gusset brackets on the bottom rail and the brackets on the top rail, there isn't much to optimize the side rails. If the load increases in the lead screws, we might consider a rod through the center of the rails to decrease transverse deflection.


### Lessons Learned

A major holdup of this part of the project was the software itself. I had to keep troubleshooting issues with Solidworks for days before I could even run the FEA studies. Even during the FEA, the software would suddenly freeze the analysis for over an hour and refuse to continue. I still don't know what caused this issue, I have never experienced it before, however I did learn a lot about troubleshooting meshes and simulation errors.

_Time Spent: 6 hours_
