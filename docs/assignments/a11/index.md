# A11 – Motor Selection Part 2 (Team Project)

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


### Section 4- Frame Twist and T-Slot Connector Design

For the frame connections, we proposed heavy 40 Series aluminum T-slot framing with an 80 × 40 mm top profile and a preliminary support spacing of 400 mm. We analyzed the vertical reactions and twisting moments produced by the two motors to determine the loading that must be resisted at the frame connections. Symmetric loading and equal sharing of the motor reaction torques were assumed for the preliminary analysis


#### Knowns & Unknowns

<img width="1180" height="1116" alt="image" src="https://github.com/user-attachments/assets/791174bf-200c-4a9b-bde5-e34d6a06fa72" />


<img width="1178" height="636" alt="image" src="https://github.com/user-attachments/assets/aecfa39e-8286-48fb-abe2-93e0b0be73f0" />


<img width="828" height="909" alt="image" src="https://github.com/user-attachments/assets/245533e1-fb57-40da-bc72-afedc4ad5f3e" />


<img width="828" height="674" alt="image" src="https://github.com/user-attachments/assets/d6d4a587-6daa-49d3-b161-26afe1154691" />


<img width="3070" height="1620" alt="image" src="https://github.com/user-attachments/assets/72ee13ea-b775-456d-be89-281590ef3c3d" />


<img width="2118" height="1524" alt="image" src="https://github.com/user-attachments/assets/59fcf3ac-ba3d-4536-93d1-99928e7db4ed" />


We selected the 80/20 Gusseted Inside-Corner Bracket, Grainger Item #5JRU3 (manufacturer model 40-4338), as our preliminary frame connector. The bracket is compatible with 40 Series T-slot framing and has eight mounting holes, allowing multiple fastening points. Its gusseted design was chosen to provide additional rigidity at the connection between the top beam and vertical supports. Grainger also lists a compatible M8 bolt and T-slot nut assembly, Item #5JRH6

The preliminary analysis gave vertical reactions of 1000 N and torsional reactions of 5.44 N·m at each support under the assumed loading conditions. The manufacturer's drawing confirmed a 40 mm spacing between mounting-hole columns, which was used as an assumed effective lever arm to calculate a 136 N force couple. The final fastener forces and connector capacity still require verification based on the actual bracket arrangement and loading direction


### Lessons Learned 

Through this assignment, I learned how to apply bearing stress, torsional shear stress, and equilibrium equations to the design of mechanical components. I also learned that theoretical minimum dimensions are not always the most practical choices, since rigidity, alignment, assembly, and manufacturer specifications must also be considered. This assignment helped me understand how the motor mount, coupler, and frame connections work together in the tensile testing machine.


**_Time spent: 5 hours_**
