# A7 – Bracket FEA

## Objective
For this assignment, I am performing Finite Element Analysis (FEA) on the bracket I designed in previous assignments (A5 and A6) using SolidWorks Simulation The purpose is to evaluate the bracket's stress, displacement, and factor of safety under an applied load of 600 lbf

I will use different mesh sizes to examine convergence and determine how mesh refinement affects the simulation results. Based on the results, I will identify areas that may need improvement and modify the design to improve its structural performance

## Analyze

### Design I – Original Bracket

Initial FEA Setup

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




## Decide


## Communicate

