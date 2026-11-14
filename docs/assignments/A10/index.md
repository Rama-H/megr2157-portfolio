# A10 – Lead Screw Translating System (Team Project) 

## Team member 1: Rama Hamid (my part) 

## Objective

The objective of this assignment is to design a mechanical lead screw translating system for a bench-top tensile tester capable of applying a maximum tensile force of 2 kN to a test specimen. The system must provide a controlled linear crosshead speed ranging from 1 to 50 mm/min using two identical lead screws, each at least 18 inches long.

The lead screw design involves determining the minimum required diameter based on axial stress, calculating the necessary rotational speed range, and determining the maximum driving torque. A factor of safety of 4 is used to ensure adequate strength under the specified loading conditions. The final lead screws are selected using manufacturer specifications and engineering references.

<img width="1188" height="1396" alt="image" src="https://github.com/user-attachments/assets/aacf7624-3577-4556-a789-9574a6d48a9b" />


## Analyze

### Part 1: Minimum Lead Screw Diameter

**Knowns & Unknowns**

<img width="1250" height="374" alt="image" src="https://github.com/user-attachments/assets/d753fc4e-4a3c-40cf-b01b-1ddf5de01245" />


The minimum required lead screw diameter was determined using the axial stress equation and the specified factor of safety of 4. Since the system uses two identical lead screws, the total tensile force of 2,000 N was assumed to be distributed equally, resulting in an axial load of 1,000 N per screw.

For the preliminary material selection, AISI 1018 steel was considered, with an assumed yield strength of 220 MPa. Using the axial stress relationship, the minimum required diameter was calculated to be 4.81 mm (0.189 in).

**Calculations:**

<img width="744" height="960" alt="image" src="https://github.com/user-attachments/assets/b009db14-d73d-40df-8984-64d0c9f0764e" />

<img width="828" height="654" alt="image" src="https://github.com/user-attachments/assets/d37efb83-464a-46e0-a51d-bd42149466d3" />

The selected Roton #59284 steel Acme lead screw has a manufacturer-listed minor diameter of 0.359 in (9.12 mm). Since the actual minor diameter exceeds the calculated minimum, the selected screw satisfies the preliminary axial stress requirement under the assumed material properties.

<img width="1490" height="1548" alt="image" src="https://github.com/user-attachments/assets/518206e1-6116-4c76-8cb8-9d99f9188015" />


**Note:** The 220 MPa yield strength is a preliminary design assumption for AISI 1018 steel and is not a manufacturer-certified property of Roton #59284.

<img width="1528" height="1346" alt="image" src="https://github.com/user-attachments/assets/db10acf7-e59d-420b-876e-b19402b8afbd" />

<img width="3182" height="1634" alt="image" src="https://github.com/user-attachments/assets/d91d9045-a7cc-47db-8966-c1c1e729623f" />




### Part 2: Rotational Speed Range

**Knowns & Unknowns**

<img width="1250" height="324" alt="image" src="https://github.com/user-attachments/assets/dde0147d-7c9a-4365-a786-4516f68c708e" />


The rotational speed range was calculated using the required linear crosshead speed of 1–50 mm/min and the lead of the selected screw.

According to Roton's engineering data, the 1/2"-10 Acme lead screw has a lead of 0.100 in/revolution, equivalent to 2.54 mm/revolution.

Using the relationship between linear velocity, rotational speed, and screw lead, the required rotational speed range was determined to be:

**Minimum rotational speed: 0.394 rpm**

**Maximum rotational speed: 19.69 rpm**

Therefore, the lead screws must operate between approximately 0.394 and 19.69 rpm to achieve the required linear crosshead speed.

<img width="828" height="935" alt="image" src="https://github.com/user-attachments/assets/71f37969-e8ba-4563-a87d-183b9b143325" />

<img width="1390" height="484" alt="image" src="https://github.com/user-attachments/assets/883b9855-c029-4fa0-bd09-c1a28240d757" />

<img width="1440" height="1322" alt="image" src="https://github.com/user-attachments/assets/11b65262-c904-4785-940a-94a2327c3632" />

_Reference_: _Roton, Acme Lead Screws & Nuts — Engineering Data, Table 4._

### Part 3: Maximum Driving Torque

**Knowns & Unknowns**

<img width="1254" height="434" alt="image" src="https://github.com/user-attachments/assets/c8cef9b4-907e-4ce7-84ff-80cfd2b54195" />


The maximum driving torque was determined to ensure that the lead screw system can generate the required tensile force of 2 kN.

Because the system consists of two identical lead screws, each screw was assumed to carry an axial load of 1,000 N.

The selected screw uses an Acme thread profile with an included thread angle of 29°, corresponding to a half-angle of 14.5°. The Acme thread geometry was referenced from Machinery's Handbook, 31st Edition, pages 2057–2060.

<img width="1368" height="914" alt="image" src="https://github.com/user-attachments/assets/b9a6527d-ac98-4a3b-9f38-3a4a4cd55118" />


For the friction analysis, a coefficient of static friction of μ = 0.16 was selected for lubricated steel-on-bronze contact. This value was extracted from Machinery's Handbook, 31st Edition, page 173, Table 1.

<img width="824" height="1350" alt="image" src="https://github.com/user-attachments/assets/74308205-4b38-40b6-b13e-587d61d6ef6c" />


The effective friction coefficient was calculated by accounting for the Acme thread angle. Using the lead screw torque equation and the selected screw geometry, the required driving torque was determined to be approximately:

**Torque per lead screw: 1.36 N·m**

**Combined torque for two lead screws: 2.72 N·m**

**Calculations:** 


<img width="705" height="960" alt="image" src="https://github.com/user-attachments/assets/ddb72952-9d07-47ca-a745-fccf23887eaf" />

<img width="828" height="594" alt="image" src="https://github.com/user-attachments/assets/906a4b74-bb8a-4e26-954b-650c0713d706" />

<img width="828" height="752" alt="image" src="https://github.com/user-attachments/assets/81127b10-9319-4851-bcfb-9b94bc54e4f2" />


These values represent the calculated screw-thread driving torque under the stated friction and loading assumptions. Additional losses from bearings and the mechanical transmission would need to be considered when selecting the final driving mechanism.



### Part 4: Lead Screw Selection

Based on the calculated minimum diameter, rotational speed range, and driving torque, two identical **Roton #59284, 1/2"-10 RH Steel Acme lead screws** were selected for the tensile tester.

_Reference: Roton, Acme Lead Screws, Table 5, and Roton #59284 product specifications._

https://www.roton.com/products/acme-lead-screws-nuts/screws/ 

<img width="1518" height="1638" alt="image" src="https://github.com/user-attachments/assets/bd59570b-290e-4acd-87ae-cfb7514dacb8" />

<img width="1478" height="892" alt="image" src="https://github.com/user-attachments/assets/f513767e-608a-4794-acef-c79e696354d9" />


<img width="2428" height="1626" alt="image" src="https://github.com/user-attachments/assets/24fa8423-30d2-4404-b073-880d395b3bef" />

<img width="802" height="646" alt="image" src="https://github.com/user-attachments/assets/278dcdfd-c45f-43c8-81cf-967f53366563" />


The selected screw has a minor diameter greater than the preliminary calculated minimum diameter of 4.81 mm. Its lead also provides the required rotational speed range of 0.394–19.69 rpm.

The use of two identical lead screws allows the tensile load to be distributed between the screws while maintaining synchronized crosshead movement.



## Decide
_Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Communicate




## Team member 2: Pierce Brown


## Objective


## Analyze


## Decide
_Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Communicate













## Team member 3: Bridget Fagan


## Objective


## Analyze


## Decide
_Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Communicate












