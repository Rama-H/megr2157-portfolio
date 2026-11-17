# A10 – Lead Screw Translating System (Team Project)

## Team member 1: Rama Hamid

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

#### Lessons Learned 

Throughout this assignment, I learned how to select a lead screw based on the mechanical requirements of a tensile testing system. I learned how to determine the minimum screw diameter using axial stress and a factor of safety, calculate the rotational speed needed to achieve a specific linear speed, and determine the torque required to apply the desired tensile force.

One of the biggest challenges was finding the correct information in Machinery's Handbook and the manufacturer's catalogs. This helped me understand the importance of using reliable references and checking dimensions, material properties, and friction when selecting mechanical components.


**Time Spent: 2 days**


## Team member 2: Pierce Brown

### Nut and Flange 
#### Objective
  The objective of the nut and flange section is to verify the nuts internal threads support the applied load with a minimum safety factor of 4, then find the compatible flange. 

#### Analyze
The selected components are McMaster bronze nut 95072A109 and steel flange 95082A642. These were found on Rotons website originally as nut 90222 and flange 89838, then their best fitting equivalent were found on McMaster since Roton did not have download links. The nut has a 1/2"-10 Acme internal thread for the lead screw and a 15/16"-16 external mounting thread for the flange. Using the symbolical solutions, an excel table was filled out to automatically solve for the numerical answers. This way, if the previous parts values get changed, they are automatically re-evaluated for my section. The chosen material was bronze, and a yield strength value was googled, returning 125 MPa. 

<img width="485" height="345" alt="Screenshot 2026-11-16 180817" src="https://github.com/user-attachments/assets/00a02475-e000-4d9e-b5fe-a01f53a9a729" />
<img width="497" height="358" alt="Screenshot 2026-11-16 173739" src="https://github.com/user-attachments/assets/8097f0a2-5606-4576-acf4-9b12670751e7" />

The FBD above shows how one isolated nut receives half of Fmax. The screw's threads transfers the load to the nut, and the nuts external threads transfer the load to the flange. 

Using the stated material strength and engagement assumptions, the calculated thread bending stress was 10.99  MPa, below the allowable 31.25 MPa. the resulting safety factor of 11.37 greatly exceeds the required value of 4. The accuracy of that actual safety factor is conditional on the assumed effective engagement. The strength of the mounting bolts and external threads are assumed sufficient. 

### Crosshead
#### Objective
 The crosshead sections main objective is to select a suitable crosshead material and dimensions, then verify and change the selected material and dimensions to minimize deflection to less than 0.1mm while supporting the maximum load with a safety factor of 4. 

#### Analyze 
  The crosshead was modeled as a simply supported beam carrying a 2,000 N center load. The selected material was 6061-T6 aluminum, with a rectangular cross section 80 mm wide by 30 mm vertical by 400 mm long. The screw-hole centers were placed 50 mm from each end, giving a 300mm support span. 
  
<img width="508" height="397" alt="Screenshot 2026-11-16 173755" src="https://github.com/user-attachments/assets/6fb2cc1b-12b5-4923-bc5e-1dcee2a365a0" />
<img width="490" height="392" alt="Screenshot 2026-11-16 180829" src="https://github.com/user-attachments/assets/9832e561-3b30-4bd4-8f02-09443e39a4b0" />
<img width="510" height="198" alt="Screenshot 2026-11-16 173804" src="https://github.com/user-attachments/assets/7d2c33fa-51c6-429f-a342-3acdca8525a1" />

The maximum bending stress of 12.5 MPa is below the allowable 69 Mpa. the calculated safety factor of 22.08 exceeds the required value of 4. Bending strength requires a minimum thickness of 12.77 mm, while deflection requires 29.04 mm. Deflection therefor controls the design, and a thickness of 30 mm was selected. This gives a bending stress of 12.5 MPa, a safety factor of 22.08, and a maximum deflection of 0.09071 mm

### Lessons Learned
From this assignment I learned how to check the bending strength of a nut's internal threads from the lectures model. I also learned that a crosshead can meet the strength requirement while exceeding the deflection limit. Initially I set the thickness to 25 mm which passed the bending-strength check, but failed at the deflection check. Increasing the thickness to 30 mm reduced the deflection to a passable amount. Deflection therefor controlled the selected thickness in this assignment. Building the calculations in Excel allowed me to update the dimensions and automatically recalculate the results. 

I spent a total of 2 days working on my section.

## Team member 3: Bridget Fagan

### Multiview Sketches

Below are the multiview sketches for the crosshead assembly. The flange and nut are aligned along the lead screw and are situated underneath the crosshead. As the motor eventually turns the lead screw, the nut and flange will force the crosshead up along the lead screw, applying force to the sample.

<img width="1512" height="2016" alt="image0 (4)" src="https://github.com/user-attachments/assets/8308d183-34a9-4280-8ab2-bd3fbca6531b" />

## Objective

The main CAD objectives were to create an assembly of the theoretical tensile tester using direct part downloads and relevant assembly constraints. Most of the parts in the assembly were downloaded from McMaster-Carr using the Solidworks 2025 add-in. Below is the list of parts used in the assembly.

<img width="987" height="592" alt="Screenshot 2026-11-16 155539" src="https://github.com/user-attachments/assets/2c469700-0dd6-4ed1-814f-b6e337f38606" />


## Analyze

### Part 3: CAD Assembly

Click ([A10 (2).zip](https://github.com/user-attachments/files/34944473/A10.2.zip)) to download the assembly .zip file.

The crosshead was designed as a separate part using dimensions from Part 2. The final dimensions of the crosshead were 400 x 80 x 30 mm. I added round fillets on the edges to improve strength and minimize damage. The holes for the lead screws are 300 mm apart, symmetrically from the crosshead center line.

<img width="510" height="763" alt="Screenshot 2026-11-16 155251" src="https://github.com/user-attachments/assets/478b9fd2-b2e1-4e73-9000-171e155587af" />

The frame was designed using the T-slot framing parts manufactured by McMaster-Carr. These rails have standard sizing and fit together with no interference. The set of parts is designed together to create the frame as one whole piece. The edge connectors are enclosed gussets which fit into each rail using a thumb screw that turns to secure itself by 90 degrees.

<img width="622" height="747" alt="Screenshot 2026-11-16 155046" src="https://github.com/user-attachments/assets/b87e49af-cd50-427c-af82-bcd8a4b72fe4" />

The final CAD assembly is shown below. All components are able to be edited individually if a parameter changes. The crosshead sits within the frame with a clearance of 5 mm on either side which compensates for small angles as well as removes the variable of friction against the inside of the frame. The base plate is able to be adjusted vertically, depending on the size of the sample being used. The heads of the lead screws, while not shown in the model, will be held in contact with the base plate using a threaded flange that is mounted via screws to the base plate.

<img width="273" height="331" alt="Screenshot 2026-11-16 163810" src="https://github.com/user-attachments/assets/7d5dcd21-28c7-47f9-9e38-89cd9d5ab748" />

### Lessons Learned

Throughout this assignment I was able to practice assemblies in Solidworks. I learned how to edit downloaded parts and modify them to fit the design, and I learned a lot about screw standards as well. Understanding how the nut, flange, and screw were mated was very important in creating the assembly. 

In total I spent over 7 hours on this part of the assignment. I was responsible for all CAD modeling and multiview sketches which took a very long time as well as tabulating the costs.

### Tabulating Costs

The following table details each part used in the assembly and its associated cost. All parts are sourced from McMaster-Carr, and all part numbers are unique.

<table>
  <tr>
    <th>Item Number</th>
    <th>Quantity</th>
    <th>Name</th>
    <th>Price Per Unit</th>
    <th>Cost</th>
    <th>Purchase Link</th>
  </tr>
  <tr>
    <td>95072A109</td>
    <td>2</td>
    <td>Acme Externally Threaded Nut</td>
    <td>$37.61</td>
    <td>$75.22</td>
    <td>[Link](https://www.mcmaster.com/95072A109/)</td>
  </tr>
  <tr>
    <td>95082A642</td>
    <td>2</td>
    <td>Precision Acme Flange 1215 Carbon Steel, 15/16"-16 Thread Size</td>
    <td>$53.18</td>
    <td>$106.36</td>
    <td>[Link](https://www.mcmaster.com/95082A642)</td>
  </tr>
  <tr>
    <td>5537T195</td>
    <td>2</td>
    <td>T-Slotted Framing Closed Gusset Corner Bracket, 3" Long</td>
    <td>$22.04</td>
    <td>$44.08</td>
    <td>[Link](https://www.mcmaster.com/5537T195/)</td>
  </tr>
  <tr>
    <td>5537T112</td>
    <td>1</td>
    <td>T-Slotted Framing Double Six Slot Rail, Silver, 80 mm High x 40 mm Wide, Solid</td>
    <td>$51.82</td>
    <td>$51.82</td>
    <td>[Link](https://www.mcmaster.com/5537T112/)</td>
  </tr>
  <tr>
    <td>5537T108</td>
    <td>2</td>
    <td>T-Slotted Framing Double 6-Slot Rail, Silver, 80mm High, 40mm Wide, Solid 2' Long</td>
    <td>$51.82</td>
    <td>$51.82</td>
    <td>[Link](https://www.mcmaster.com/5537T112-5537T108/)</td>
  </tr>
  <tr>
    <td>5537T914</td>
    <td>2</td>
    <td>T-Slotted Framing Double 6-Slot Rail, Silver, 80 mm High x 40 mm Wide, Solid</td>
    <td>$2.52</td>
    <td>$5.04</td>
    <td>[Link](https://www.mcmaster.com/5537T914/)</td>
  </tr>
  <tr>
    <td>5537T108</td>
    <td>1</td>
    <td>T-Slotted Framing Double 6-Slot Rail, Silver, 80mm High, 40mm Wide, Solid 2' Long</td>
    <td>$51.82</td>
    <td>$51.82</td>
    <td>[Link](https://www.mcmaster.com/5537T112-5537T108/)</td>
  </tr>
  <tr>
    <td>93410A112</td>
    <td>2</td>
    <td>Alloy Steel Acme Lead Screw Right Hand, 1/2"-10 Thread Size, 2 Feet Long</td>
    <td>$39.17</td>
    <td>$78.34</td>
    <td>[Link](https://www.mcmaster.com/93410A112/)</td>
  </tr>
</table>

