# A7 – Bracket FEA

## Objective
For this assignment, I am performing Finite Element Analysis (FEA) on the bracket I designed in previous assignments (A5 and A6) using SolidWorks Simulation The purpose is to evaluate the bracket's stress, displacement, and factor of safety under an applied load of 600 lbf

I will use different mesh sizes to examine convergence and determine how mesh refinement affects the simulation results. Based on the results, I will identify areas that may need improvement and modify the design to improve its structural performance

## Analyze

## Design I – Original Bracket

**Initial FEA Setup**

I began the analysis using the parametric bracket developed in Assignment A6. I saved a separate copy of the original CAD model to preserve the previous design.

The material assigned to the bracket is 6061-T6 aluminum, which will remain unchanged throughout the optimization process.

The first analysis uses a static study in SolidWorks Simulation to evaluate the bracket under the prescribed loading conditions. The results will establish a baseline for subsequent mesh refinement and geometry optimization.

**a) Select Proper Constraints**

I started by creating a static study in SolidWorks Simulation and preparing my bracket for analysis

To represent how the bracket would be supported during loading, I selected the two bottom surfaces of the upper U-shaped features and applied a Fixed Geometry fixture

These surfaces represent the areas where the bracket would be supported by a bar. The fixed constraints prevent movement at these locations while the external load is applied to the lower cylindrical portion of the bracket

The same fixture locations will be maintained throughout the mesh refinement tests to ensure a consistent comparison of the results

<img width="2912" height="1902" alt="image" src="https://github.com/user-attachments/assets/56a4be7b-7dbd-4b5e-81a7-b4cb258d3015" />


**b) Select Appropriate Loading**

I applied a 600-lbf vertically downward force to the cylindrical portion of the bracket. The force was distributed across the selected cylindrical surface to represent the applied load

I used the Selected Direction option to control the force direction and reversed it so the load acted downward

<img width="2048" height="1350" alt="image" src="https://github.com/user-attachments/assets/3a2942b9-a79d-4972-8d96-939ef0d54ac9" />

**c) Select a Mesh**

After defining the fixtures and external load, I proceeded to generate the initial finite element mesh using SolidWorks Simulation.

I started with the default mesh settings to establish a baseline for the first analysis. The mesh will be refined in subsequent simulations to evaluate convergence of the stress, displacement, and safety factor results.

**Initial Meshing Attempt**

During my first attempt to generate the finite element mesh, SolidWorks reported a meshing failure. The initial mesh could not be generated successfully.

To troubleshoot this issue, I investigated the mesh settings and attempted to use a finer, curvature-based mesh to better represent the bracket geometry.

This step helped me understand that mesh generation depends on the complexity of the geometry and the size of the elements.

<img width="2910" height="1914" alt="image" src="https://github.com/user-attachments/assets/3b67e6ca-f397-48ec-8ba9-d594d077b6cf" />

**Mesh Generation**
After defining the fixed supports and applying the 600-lbf downward load to the cylindrical shaft, I attempted to generate a finite element mesh in SOLIDWORKS Simulation. However, the initial simulation encountered several issues because the bracket consisted of two separate solid bodies that were not properly connected.

I first attempted to resolve this issue by defining bonded interactions between the bodies. Despite adjusting the interaction settings and refining the mesh, the simulation continued to identify an underconstrained body, causing the analysis to fail.

To resolve this problem, I used Insert → Features → Combine → Add to merge the two solid bodies into a single continuous structure. SOLIDWORKS confirmed the successful operation by displaying Solid Bodies (1) instead of Solid Bodies (2).

After combining the bodies, I returned to the static simulation study and generated a new curvature-based mesh. The mesh was successfully created, with triangular surface elements covering the entire bracket, including the upper U-shaped section, vertical support, and cylindrical shaft.

This modification eliminated the need for bonded interactions between separate bodies and allowed the model to proceed to the finite element analysis stage for evaluating stress and displacement.


<img width="2918" height="1902" alt="image" src="https://github.com/user-attachments/assets/e72f2380-f003-483c-b7e5-c87c5066a965" />


### Initial Finite Element Analysis — Design I

After successfully generating the finite element mesh, I ran the static simulation in SOLIDWORKS using the applied 600-lbf load and defined fixed supports.

The simulation generated stress, displacement, and strain results. I examined the deformed shape to visualize the bracket's response to the applied load. The deformation was displayed using a scale factor of 5.18099 to make the deflection easier to observe.

The next step was to evaluate the maximum Von Mises stress and resultant displacement to determine whether the original design satisfied the assignment requirements.

**1. Von Mises Stress Results — Design I**

<img width="3196" height="1906" alt="image" src="https://github.com/user-attachments/assets/d9ee73cc-4ca8-41c5-be2f-3211aed5f708" />

The legend shows a maximum stress of (4.538x10^8 N/m^2)

Converting to psi:
sigma_max= (4.538x10^8)/ (6894.76)

sigma_max= 65,819 psi

After running the static simulation, I examined the Von Mises stress distribution throughout the bracket under the applied 600-lbf load.

The maximum Von Mises stress was approximately 65,819 psi (65.82 ksi), with stress concentrations occurring near the inside corners of the upper support structure.

The calculated stress exceeded the allowable stress of 10,000 psi and the material yield strength of approximately 39,885 psi. Therefore, the initial design did not satisfy the stress requirement.

The initial design will require geometric modifications to reduce stress concentrations and improve its structural performance.

**Result: FAIL — Design modification required**



**2. Displacement Analysis — Design I**


<img width="3200" height="1908" alt="image" src="https://github.com/user-attachments/assets/b78728c2-b581-403f-92bc-c3a9b87fd7d7" />


After evaluating the Von Mises stress, I examined the resultant displacement of the bracket under the applied 600-lbf load.

The simulation produced a maximum displacement of 2.684 mm (0.1057 in), occurring near the free end of the cylindrical shaft. The displacement gradually decreased toward the upper fixed supports.

Compared with the displacement limit of 0.005 in established in the previous design assignment, the initial bracket exceeded the allowable deflection.

The displacement plot also showed the expected bending behavior of the bracket under the applied downward load.

**Result: FAIL — Design modification required to improve stiffness.**


**3. Equivalent Strain Analysis — Design I**


<img width="3200" height="1910" alt="image" src="https://github.com/user-attachments/assets/2a2af8e2-3a3f-4918-87f4-7b69cbf0acf1" />


After evaluating the stress and displacement results, I examined the equivalent strain distribution to identify areas experiencing the greatest deformation under the applied 600-lbf load.

The simulation produced a maximum equivalent strain of approximately 0.003899 in/in. The strain distribution showed higher concentrations around the upper support regions, particularly near the inside corners of the U-shaped bracket.

The lower cylindrical shaft exhibited comparatively low equivalent strain, while the upper support regions experienced greater localized deformation.

These results help identify areas that may benefit from geometric modifications during the design optimization process

**4. Factor of Safety Analysis — Design I**

<img width="3200" height="1906" alt="image" src="https://github.com/user-attachments/assets/dcd2b7a0-236e-4ae0-96e3-fd81a2128bf6" />

After examining the stress, displacement, and strain results, I performed a Factor of Safety (FOS) analysis using the maximum Von Mises stress criterion and the yield strength of 6061-T6 aluminum.

SOLIDWORKS calculated a minimum factor of safety of 0.606, indicating that the maximum stress exceeds the material's yield strength.

The Factor of Safety plot showed that the original bracket did not meet the minimum safety requirement under the applied 600-lbf load. This indicates that geometric modifications are necessary to improve the structural performance of the bracket.

**Result: FAIL — Design modification required**

### Table 1. Initial FEA Results — Design I, Mesh 1

| Parameter | Result |
|------------|---------|
| Material | 6061-T6 Aluminum |
| Applied Load | 600 lbf |
| Maximum Von Mises Stress | 65,819 psi |
| Material Yield Strength | 39,885 psi |
| Maximum Displacement | 2.684 mm |
| Maximum Displacement | 0.1057 in |
| Maximum Equivalent Strain | 0.003899 |
| Number of Elements | 24,404 |
| Number of Nodes | 37,899 |
| Minimum Factor of Safety | 0.606 (FAIL) |


### Mesh Convergence Study — Design I

The initial mesh was used as the baseline for the convergence study. Additional simulations will be performed using progressively smaller element sizes while maintaining the same geometry, material, boundary conditions, and applied load

The maximum Von Mises stress and resultant displacement will be compared between successive meshes to evaluate convergence within the specified 7% tolerance

The initial curvature-based mesh consisted of **24,404 elements and 37,899 nodes**, with a maximum element size of **0.120538 in** and a minimum element size of **0.0602693 in**. This baseline simulation produced a maximum Von Mises stress of **65,819 psi**, a maximum resultant displacement of **2.684 mm**, and a minimum factor of safety of **0.606**

<img width="2900" height="1854" alt="image" src="https://github.com/user-attachments/assets/f77b232f-c0b2-4f29-821f-70871b181c94" />

### Mesh Refinement — Mesh 2

To evaluate mesh convergence, I refined the initial curvature-based mesh by reducing the maximum and minimum element sizes by approximately 25%.

The initial mesh used a maximum element size of 0.120538 in and a minimum element size of 0.0602693 in. For the second simulation, I reduced these values to 0.090 in and 0.045 in, respectively.

The purpose of this refinement was to increase the number of finite elements and examine whether the maximum Von Mises stress and resultant displacement would approach stable values.

I maintained the same material (6061-T6 aluminum), 600-lbf downward load, fixed support locations, and bracket geometry to ensure a consistent comparison.

The minimum number of elements in a circle was kept at 8, and the element growth ratio remained at 1.4. These settings were unchanged to isolate the effect of reducing the element sizes

### Table 2. Mesh Refinement Parameters
 
| Parameter | Mesh 1 (Initial) | Mesh 2 (Refined) |
|------------|------------------|------------------|
| Mesh Type | Curvature-based | Curvature-based |
| Maximum Element Size (in) | 0.120538 | 0.090 |
| Minimum Element Size (in) | 0.0602693 | 0.045 |
| Minimum Elements in a Circle | 8 | 8 |
| Element Growth Ratio | 1.4 | 1.4 |


**Mesh 2 — Von Mises Stress Results**

After reducing the maximum and minimum element sizes to 0.090 in and 0.045 in, respectively, I generated the refined mesh and reran the static simulation while maintaining the same material, loading conditions, fixtures, and bracket geometry.

The second simulation produced a maximum Von Mises stress of approximately 5.450 × 10⁸ Pa (79,045 psi), compared with 65,818 psi from the initial mesh.

The percentage change in maximum stress was calculated as:

<img width="1300" height="554" alt="image" src="https://github.com/user-attachments/assets/c64b2383-98b7-4115-ad56-013bf9fbd404" />


The stress increased with mesh refinement, indicating that the maximum stress result has not yet converged within the specified 7% tolerance.

The highest stress regions remained concentrated near the upper support corners. Additional mesh refinement is needed to determine whether the maximum stress approaches a stable value.

<img width="3200" height="1906" alt="image" src="https://github.com/user-attachments/assets/9c92576f-485a-4057-9fb6-6224bafc1925" />

Result: Stress convergence not achieved between Mesh 1 and Mesh 2.


**Mesh 2 — Displacement Results**

After refining the mesh, I examined the resultant displacement under the same 600-lbf downward load.

The maximum displacement increased slightly from 2.684 mm in Mesh 1 to 2.700 mm in Mesh 2. The highest displacement occurred near the free end of the cylindrical shaft, while displacement decreased toward the fixed upper supports.

The percentage change between the two meshes was calculated as:

<img width="1060" height="323" alt="image" src="https://github.com/user-attachments/assets/35b12c95-fc59-4ad9-8a58-e8f8c6e73bda" />


Since the percentage change was below the required 7% tolerance, the displacement results demonstrated convergence between the two mesh sizes.

However, the maximum displacement of approximately 0.1063 in still exceeded the allowable displacement of 0.005 in.

Result: Displacement convergence PASS — Structural stiffness requirement FAIL.

<img width="3200" height="1910" alt="image" src="https://github.com/user-attachments/assets/4f95c12d-3f63-4dc5-a185-1dc2c91126f4" />


**Mesh 2 — Mesh Refinement and Convergence**

For the second simulation, I refined the curvature-based mesh by reducing the maximum element size from 0.120538 in to 0.090 in and the minimum element size from 0.0602693 in to 0.045 in

The refined mesh contained 50,007 elements and 75,726 nodes, compared with 24,404 elements and 37,899 nodes in the initial mesh. The mesh maintained high quality with no distorted elements

The maximum Von Mises stress increased from 65,818 psi to approximately 79,045 psi, representing a 20.1% change. Meanwhile, the maximum displacement increased from 2.684 mm to 2.700 mm, representing a 0.60% change

The displacement results satisfied the 7% convergence criterion, but the maximum stress results did not.

Therefore, an additional mesh refinement will be performed to investigate whether the stress results approach convergence

Conclusion: Displacement convergence was achieved between Mesh 1 and Mesh 2, while further refinement is required to evaluate stress convergence

<img width="3198" height="1906" alt="image" src="https://github.com/user-attachments/assets/f8c1ee2d-d17a-4cde-875d-169e42b883fd" />

**Mesh 3 — Von Mises Stress Results**

For the third simulation, I further refined the curvature-based mesh while maintaining the original geometry, 6061-T6 aluminum material, fixed supports, and 600-lbf downward load.

The maximum Von Mises stress increased to approximately 105,514 psi (105.51 ksi), compared with 79,045 psi for Mesh 2.

The percentage change was calculated as:

<img width="1126" height="200" alt="image" src="https://github.com/user-attachments/assets/f2b936e0-7ddf-4798-a0f4-ad5969a5628e" />


The stress change exceeded the specified 7% convergence tolerance. The highest stresses remained concentrated near the upper support regions.

The increasing maximum stress with mesh refinement suggests that localized stress concentrations near the constrained edges may be influencing the results. Therefore, the peak stress has not demonstrated convergence.

Result: Stress convergence FAIL — Further investigation of localized stress concentrations is required.

<img width="3200" height="1908" alt="image" src="https://github.com/user-attachments/assets/c4241c58-6d52-4ef4-97ae-f41b0bada625" />


### Mesh 3 — Final Mesh Refinement

Mesh Convergence Comparison

### Table 3. Mesh Convergence Study Results
 
| Parameter | Mesh 1 | Mesh 2 | Mesh 3 |
|------------|---------|---------|---------|
| Total Elements | 24,404 | 50,007 | 115,359 |
| Total Nodes | 37,899 | 75,726 | 169,808 |
| Maximum Stress (psi) | 65,818 | 79,045 | 105,514 |
| Maximum Displacement (mm) | 2.684 | 2.700 | 2.713 |
| Stress Change (%) | — | 20.1 | 33.5 |
| Displacement Change (%) | — | 0.60 | 0.48 | 
Convergence Evaluation


<img width="2912" height="1862" alt="image" src="https://github.com/user-attachments/assets/5c5d2200-3e8e-426e-a4f8-7d3ae382ef03" />

**Investigation of Maximum Stress Location — Design I**


After completing the mesh convergence study, I used the Probe tool in SOLIDWORKS Simulation to investigate the location of the maximum Von Mises stress.

The maximum stress was approximately 105,514 psi (727.5 MPa), located at the upper-left inside corner of the bracket near the fixed support.

Additional probe measurements showed elevated stresses around the upper support regions, indicating localized stress concentrations.

Since the maximum stress increased with mesh refinement, I considered the possibility of a numerical stress singularity near the fixed boundary conditions. Therefore, the maximum stress result requires further investigation before being used to evaluate convergence or guide design modifications.

The displacement results demonstrated convergence within the specified 7% tolerance, while the maximum stress results did not.

These observations will help guide the next stage of the analysis and the development of Design II.

<img width="3200" height="1906" alt="image" src="https://github.com/user-attachments/assets/65215f5a-f68a-471e-881f-32a8bf9e4fc4" />


**Comparison of Nodal and Elemental Stress Results**

To further investigate the maximum stress concentration, I compared the nodal and elemental Von Mises stress results for Mesh 3.

The nodal stress plot reported a maximum stress of 105,514 psi, while the elemental stress plot reported approximately 78,538 psi.

The difference between these results was approximately 25.6%, indicating that the reported peak stress was sensitive to the stress display method.

The highest stresses remained concentrated near the upper fixed-support regions. Combined with the increasing maximum stress observed during mesh refinement, this suggested a possible stress singularity associated with the boundary conditions or sharp geometric features.

Although displacement convergence was achieved, the maximum stress had not converged. Therefore, the stress results require further investigation before a reliable maximum-stress assessment can be made

<img width="2048" height="1223" alt="image" src="https://github.com/user-attachments/assets/9757a23c-cc2a-4836-a8ed-8f56162eb3ad" />

<img width="2048" height="1214" alt="image" src="https://github.com/user-attachments/assets/96aabff6-641b-4010-b1a9-cc2f91a506cd" />



**Factor of Safety Analysis — Design I (Mesh 3)**
After completing the mesh convergence study, I evaluated the factor of safety using Mesh 3, the finest mesh in the analysis.

In SolidWorks Simulation, I generated a Factor of Safety plot using the maximum Von Mises stress criterion and the yield strength of 6061-T6 aluminum.

The factor of safety was calculated using:


FOS= (sigma_y) / (sigma_max)

Using the yield strength of 39,885 psi and the maximum nodal stress of approximately 105,514 psi:

=(39,885)/(105,514)
=0.378

The preliminary calculated factor of safety is approximately 0.378, which is below 1.0.

Minimum FOS reported by SolidWorks: 0.378027

**Factor of Safety Plot:**

<img width="2926" height="1872" alt="image" src="https://github.com/user-attachments/assets/26a874fe-f413-4b1e-9a4d-a009ab02134a" />


The factor of safety is below 1.0, indicating that the maximum calculated stress exceeds the material's yield strength under the applied loading conditions.

However, because the maximum stress did not converge within the required 7% tolerance, this factor of safety remains mesh-dependent.

These results indicate that the original bracket requires geometric modifications to improve its strength.

**Result: FAIL — Design modification required**


<img width="2634" height="1818" alt="image" src="https://github.com/user-attachments/assets/fa14d4a3-487b-45c3-8def-761db0ec8ae3" />



**Mesh 3 — Displacement Results**

The third simulation produced a maximum resultant displacement of 2.713 mm (0.1068 in), compared with 2.700 mm for Mesh 2.

The maximum displacement changed by only 0.48% between Meshes 2 and 3, satisfying the specified 7% mesh convergence tolerance. However, the maximum Von Mises stress continued increasing with refinement and did not satisfy the convergence criterion.

Although displacement convergence was achieved, the maximum displacement remained greater than the allowable limit of 0.005 in.

**Result: Displacement convergence PASS — Stiffness requirement FAIL**


The percentage change in displacement between Meshes 2 and 3 was:


<img width="1190" height="330" alt="image" src="https://github.com/user-attachments/assets/9f2e1c53-393c-4b2b-9c05-cf9f8a5292e6" />


<img width="3200" height="1894" alt="image" src="https://github.com/user-attachments/assets/5e03e79b-8786-4701-8c97-60508f6e7b8d" />


### Mass Properties — Design I

After completing the FEA simulations, I used the SolidWorks Mass Properties tool to determine the mass of the original bracket.

The following properties were obtained:

Table 4. Physical Properties of Design I

| Property | Value |
|----------|--------|
| Material | 6061-T6 Aluminum |
| Mass | 0.45 lb |
| Volume | 4.59 in³ |
| Density | 0.10 lb/in³ |
| Surface Area | 30.80 in² |

The original bracket has a mass of approximately 0.45 lb (0.204 kg).

This mass will serve as the baseline for comparing the subsequent design iterations. The objective is to improve the bracket's strength and stiffness while minimizing unnecessary material.

<img width="2924" height="1906" alt="image" src="https://github.com/user-attachments/assets/65972d02-7657-4818-8cde-8080e92ce1de" />



### Mesh Convergence Conclusion — Design I

Three mesh simulations were performed to evaluate the numerical convergence of the original bracket under the applied 600-lbf load.

The displacement results converged within the required 7% tolerance, with a final percentage change of 0.48% between Mesh 2 and Mesh 3.

However, the maximum Von Mises stress continued increasing with mesh refinement and did not achieve convergence. This behavior may be associated with localized stress concentrations near the fixed upper support corners.

Since stress convergence was not achieved after three attempts, Mesh 3 was selected for the final evaluation, following the assignment instructions.

The final simulation produced a maximum stress of 105,514 psi, a maximum displacement of 2.713 mm, and a minimum factor of safety of 0.378.

Although the displacement results converged, the bracket exceeded the allowable stress and displacement limits. Therefore, geometric modifications were necessary to improve its structural performance.

**Final Result: Design I failed the strength and stiffness requirements**


## Design II

### Fillet Modification — Design II

For Design II, I modified my original bracket geometry by adding **0.10-inch fillets** to seven selected edges. These included the interior corners of the upper bracket, the transitions between the horizontal and vertical sections, and the connection between the vertical support and the lower cylindrical section.

The purpose of adding these fillets was to reduce sharp corners and stress concentrations while improving load distribution throughout the bracket.

I maintained the original material, **Aluminum 6061-T6**, to ensure that the comparison between Design I and Design II was based solely on geometric modifications rather than changes in material properties.


<img width="2920" height="1902" alt="image" src="https://github.com/user-attachments/assets/f08ceda0-5d93-4191-8d6d-f51b0baf887d" />


### 2. Material Properties
 
The material assigned to Design II was **Aluminum 6061-T6**, the same material used in Design I.
 
The material properties used in the simulation were:
 
| Property | Value |
|-----------|-----------|
| Material | Aluminum 6061-T6 |
| Elastic Modulus | 69,000 MPa |
| Poisson's Ratio | 0.33 |
| Yield Strength | 275 MPa |
| Tensile Strength | 310 MPa |
| Density | 2,700 kg/m³ |
 
Keeping the material constant allowed me to evaluate how adding fillets affected the structural response.
 

---
 
### 3. Static Simulation Setup: Fixtures and Loading
 
I created a static simulation in SOLIDWORKS Simulation to evaluate the structural behavior of the modified bracket.
 
Fixed constraints were applied to the upper mounting surfaces of the bracket, representing the regions where the component is held in place.
 
A downward force of **600 lbf** was applied to the lower cylindrical section of the bracket.
 
I used the **Selected Direction** option to define the force direction rather than applying a radial force normal to the cylindrical surface. This allowed me to represent the intended downward loading condition.
 
The loading and boundary conditions were intentionally kept consistent with Design I for comparison.
 
#### Figure 4: Design II – Fixtures and Applied Load
 
<img width="2048" height="1327" alt="image" src="https://github.com/user-attachments/assets/64e37604-68b7-4347-a720-60ecedc54bfb" />
 
---
 
### 4. Mesh 1: Initial Mesh Generation
 
I generated the first mesh using the **blended curvature-based meshing method** with high-quality solid elements.
 
The initial mesh settings were:
 
| Mesh Parameter | Value |
|---------------|-------|
| Mesh Type | Blended curvature-based |
| Maximum Element Size | 0.1664 in |
| Minimum Element Size | 0.0555 in |
| Minimum Elements in a Circle | 8 |
| Element Growth Ratio | 1.4 |
| Mesh Quality | High |
| Total Elements | 12,272 |
| Total Nodes | 19,693 |
| Distorted Elements | 0 |
 
The initial mesh contained **12,272 elements** and **19,693 nodes**. The mesh quality report indicated **zero distorted elements**.
 
This mesh served as the baseline for evaluating stress and displacement before performing additional mesh refinement.

 
 
---
 
### 5. Mesh 1: Von Mises Stress Analysis
 
After running the static simulation, I examined the Von Mises stress distribution throughout the bracket.
 
The simulation produced a maximum Von Mises stress of approximately:
 
sigma_max = 3.872  10^8 Pa

sigma_max = 387.2 MPa

 
The highest stress concentrations appeared near the upper interior corners of the bracket, particularly around the left mounting region
 
The material yield strength was **275 MPa**
 
Since the maximum stress exceeded the yield strength, the simulation indicated that the bracket did not satisfy the material yield criterion under the applied loading condition
 
Although fillets were introduced to reduce stress concentrations, additional analysis and geometric optimization are necessary
 
#### Figure 7: Design II – Mesh 1 Von Mises Stress Distribution
 
<img width="2048" height="1333" alt="image" src="https://github.com/user-attachments/assets/548175ae-5b0e-4319-8583-ca0acbcd11b7" />
 
---
 
### 6. Mesh 1: Displacement Analysis
 
I examined the resultant displacement distribution to evaluate the stiffness of the modified bracket.
 
The maximum resultant displacement was:
 
delta_max = 2.917 mm
 
Converting to inches:
 
delta_max= (2.917)/(25.4)
 

delta_max= 0.1148 in

 
The maximum displacement occurred near the free end of the lower cylindrical section where the external load was applied.
 
The displacement was approximately zero near the fixed mounting surfaces and increased toward the loaded region.
 
The deformation scale displayed by SOLIDWORKS was **4.70405**, which was used only to visually exaggerate the deformed shape


 
#### Figure 8: Design II – Mesh 1 Resultant Displacement
 
<img width="2048" height="1343" alt="image" src="https://github.com/user-attachments/assets/6e5f1a38-c1af-46db-89e6-c51ca1da57fa" />
 
---
 
### 7. Mesh 1: Factor of Safety
 
The factor of safety was estimated using the material yield strength and maximum Von Mises stress.
 
SF=(sigma_y)/(sigma_max)

 
Substituting the simulation results:
 
SF=(275)/(387.2)

SF=0.710

 
The estimated minimum factor of safety was below 1.0, indicating that the maximum simulated stress exceeded the material's yield strength.
 
This suggests that further geometric modifications are necessary to improve the strength of the bracket.
 
The calculated value will be checked against the SOLIDWORKS Factor of Safety plot.
 
#### Figure 9: Design II – Mesh 1 Factor of Safety
 
<img width="3160" height="1904" alt="image" src="https://github.com/user-attachments/assets/27834d2d-7c63-404a-8e61-2bb3d5d48573" />
 
---
 
### 8. Mesh 1: Summary of Results
 
| Parameter | Design II – Mesh 1 |
|------------|-------------------|
| Maximum Von Mises Stress | 387.2 MPa |
| Maximum Stress Location | Upper Interior Mounting Region |
| Maximum Displacement | 2.917 mm (0.1148 in) |
| Maximum Displacement Location | Lower Cylindrical Section |
| Estimated Minimum Safety Factor | 0.710 |
| Number of Elements | 12,272 |
| Number of Nodes | 19,693 |
| Mesh Quality | High |
| Distorted Elements | 0 |
 
#### Initial Observations and Engineering Insights

The first simulation demonstrated how modifying geometric features can influence stress distribution and structural behavior.

Adding fillets removed sharp transitions at several locations where stress concentrations could develop. However, the initial results showed that the maximum stress still exceeded the yield strength of Aluminum 6061-T6.

I also observed that the largest displacement occurred at the loaded cylindrical section, while the fixed mounting regions experienced minimal displacement.

An important consideration is that the results from a single mesh cannot establish numerical convergence. Even though the mesh contained no distorted elements, additional refinement is necessary to determine whether the predicted stress, displacement, and factor of safety are sufficiently independent of mesh size.

For the next step, I will refine the mesh while maintaining the same geometry, material, loading, and boundary conditions.

I will compare the results using:

% Difference = |(R_fine - R_coarse) / R_fine| × 100 

The target is a difference of 7% or less between successive mesh results. If convergence is not achieved after three attempts, I will use the finest mesh results as instructed

### 9. Mesh 2: Stress and Displacement Analysis

For the second mesh iteration, I refined the mesh while maintaining the same geometry, material, loading, and boundary conditions as Design II – Mesh 1.

#### Simulation Results

| Parameter | Result |
|-----------|----------|
| Maximum Von Mises Stress | 385.5 MPa |
| Maximum Displacement | 2.923 mm (0.1151 in) |
| Maximum Equivalent Strain | 0.004366 |
| Estimated Minimum Safety Factor | 0.713 |

The maximum stress occurred near the inner corners of the upper bracket, where stress concentrations were observed. The maximum displacement occurred near the lower cylindrical shaft.

The maximum stress exceeded the yield strength of Aluminum 6061-T6 (275 MPa), indicating that additional geometric improvements may be necessary to prevent yielding under the applied loading condition.

#### Figure 10: Design II – Mesh 2 Von Mises Stress Distribution

<img width="2048" height="1223" alt="image" src="https://github.com/user-attachments/assets/662b367f-15d5-404f-bd5f-e5669ea45824" />


#### Figure 11: Design II – Mesh 2 Displacement Distribution

<img width="2048" height="1218" alt="image" src="https://github.com/user-attachments/assets/4391c5c8-1f98-427c-b533-31034097c297" />

#### Figure 12: Design II – Mesh 2 Equivalent Strain Distribution

<img width="2048" height="1217" alt="image" src="https://github.com/user-attachments/assets/48ac37b1-5b92-47be-8b35-565ee2cd0faa" />


---

### 10. Mesh Convergence Evaluation

To evaluate mesh convergence, the Mesh 1 and Mesh 2 results were compared using the percent difference formula:

% Difference = |(R_fine - R_coarse) / R_fine| × 100

#### Stress Convergence

Using the maximum Von Mises stress values:

- Mesh 1 Stress = 387.2 MPa
- Mesh 2 Stress = 385.5 MPa

% Difference = |(385.5-387.2) / 385.5| × 100

=0.441

#### Displacement Convergence

Using the maximum displacement values:

- Mesh 1 Displacement = 2.917 mm
- Mesh 2 Displacement = 2.923 mm

% Difference = |(2.923-2.917) / 2.923| × 100
=
0.205%

Because both percent differences are less than 1%, the results indicate that the solution is approaching mesh convergence. Further mesh refinement is expected to produce only minor changes in the stress and displacement results.

Both the maximum Von Mises stress and displacement changed by less than the required 7% tolerance between Mesh 1 and Mesh 2. This indicates that the results satisfy the convergence criterion for these two mesh levels. A third mesh refinement will be performed to verify the stability of the results and complete the convergence study.




#### Mesh 2 – Mesh Refinement

For the second mesh analysis, I refined the mesh to evaluate the stability of the finite element results. A high-quality, blended curvature-based solid mesh was used with a maximum element size of 0.12 in and a minimum element size of 0.04 in.

The refined mesh contained 25,930 elements and 40,072 nodes, with no distorted elements reported.

The simulation produced a maximum Von Mises stress of approximately 385.5 MPa and a maximum resultant displacement of 2.923 mm. These results were compared with Mesh 1 to evaluate mesh convergence

<img width="2918" height="1886" alt="image" src="https://github.com/user-attachments/assets/a816d8ce-384a-403a-8595-2f5688174a81" />

---

### 11. Mesh 3 – Final Mesh Refinement

A third mesh refinement was performed to evaluate the convergence of Design II. The same Aluminum 6061-T6 material, fixed supports, and 600 lbf downward load were maintained throughout the analysis.

A high-quality blended curvature-based mesh was generated with a maximum element size of **0.09 in** and a minimum element size of **0.03 in**. The final mesh contained **51,797 elements** and **78,081 nodes**, with no distorted elements.

#### Mesh 3 Results

| Parameter | Mesh 3 Result |
|------------|------------|
| Maximum Von Mises Stress | 389.1 MPa |
| Maximum Displacement | 2.927 mm (0.1152 in) |
| Maximum Equivalent Strain | 0.004418 |
| Minimum Factor of Safety | 0.7068 |
| Number of Elements | 51,797 |
| Number of Nodes | 78,081 |
| Distorted Elements | 0 |

The maximum stress occurred near the inner corners of the upper bracket, where stress concentrations developed. The greatest displacement occurred near the loaded cylindrical shaft.

Figure 13: Design II – Mesh 3 Von Mises Stress Distribution

<img width="2048" height="1331" alt="image" src="https://github.com/user-attachments/assets/977eb1ee-1f4f-421c-ae45-28ae2583f95c" />

Figure 14: Design II – Mesh 3 Displacement Distribution

<img width="2048" height="1338" alt="image" src="https://github.com/user-attachments/assets/ac52d6c4-450a-45b1-8603-08a4b6537498" />

Figure 15: Design II – Mesh 3 Equivalent Strain Distribution

<img width="2048" height="1338" alt="image" src="https://github.com/user-attachments/assets/e05a7e36-cc11-4264-8830-f9cd66c1a164" />

---
**Mesh Convergence**

Comparing Mesh 2 and Mesh 3, the maximum Von Mises stress changed by approximately 0.93%, while the maximum displacement changed by approximately 0.14%.

Both changes were below the 7% convergence tolerance, indicating that the numerical results were sufficiently stable under mesh refinement.

**Design Evaluation**

Although mesh convergence was achieved, the maximum Von Mises stress of 389.1 MPa exceeded the material yield strength of 275 MPa. The minimum factor of safety was 0.7068, below the required value of 1.0.

The maximum displacement of 2.927 mm (0.1152 in) also exceeded the allowable displacement of 0.005 in.

Therefore, **Design II did not satisfy the strength or stiffness requirements**, despite achieving mesh convergence.

---

### 12. Final Summary of Design II

| Parameter | Mesh 1 | Mesh 2 | Mesh 3 |
|------------|------------|------------|------------|
| Maximum Stress (MPa) | 387.2 | 385.5 | 389.1 |
| Maximum Displacement (mm) | 2.917 | 2.923 | 2.927 |
| Factor of Safety | 0.710 | 0.713 | 0.7068 |
| Equivalent Strain | — | 0.004366 | 0.004418 |
| Elements | 12,272 | 25,930 | 51,797 |
| Nodes | 19,693 | 40,072 | 78,081 |



## Decide


## Communicate

