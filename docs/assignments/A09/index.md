# A9 – Pulleys

## Objective

The objective of this assignment was to design and analyze a belt-driven pulley system capable of transferring power between two parallel shafts separated by a center distance of 4–6 inches. The design required two 3-inch-diameter pulleys operating between 1000 and 2000 rpm, with an initial static belt tension between 4 and 6 lbf and a minimum safety factor of 3.

The design process involved calculating the tight-side and loose-side belt tensions using friction principles, determining the required polyurethane belt diameter and circumference, sizing a hardened AISI 1060 steel shaft under torsional loading, selecting an appropriate journal bearing using pressure, surface velocity, and PV calculations, and developing a supporting frame.

The final design was evaluated using analytical calculations, manufacturer specifications, material-property references, and hand-drawn engineering sketches. The process and design decisions were documented to explain how each component was selected and how the system meets the specified requirements.


<img width="1200" height="564" alt="image" src="https://github.com/user-attachments/assets/f4d0af6c-4684-4ab4-9065-91c0fbedabfa" />


## Analyze
Select our design parameters

| Parameter | Selected Value |
|-----------|---------------|
| Pulley diameter, \(D\) | 3 in |
| Center distance, \(C\) | 5 in |
| Rotational speed, \(N\) | 1500 rpm |
| Initial static belt tension, \(T_0\) | 5 lbf |
| Pulley material | Aluminum |
| Belt material | Polyurethane rubber |
| Belt yield strength, \(S_y\) | 471 psi |
| Safety factor, \(n\) | 3 |

### Part 1: Belt Design
**Knowns**:  D1 = D2 = 3 in | C = 5 in | N = 1500 rpm | T0 = 5 lbf (static belt tension) | Sy = 471 psi | n = 3 | Belt material: Polyurethane rubber | Pulley material: Aluminum

**Unknowns**:  T1 = Tight-side belt tension | T2 = Loose-side belt tension | Amin = Minimum belt cross-sectional area | dmin = Minimum belt diameter | L = Belt circumference/length | Suitable McMaster-Carr round belt


#### Design Approach

The first step was to determine the belt forces and the minimum belt diameter required to safely transmit torque between two 3-inch-diameter pulleys separated by a 5-inch center distance.

I selected an initial static belt tension of 5 lbf and a rotational speed of 1500 rpm, both within the assignment requirements. The belt material was polyurethane rubber with a specified yield strength of 471 psi. A minimum safety factor of 3 was required.

#### Free-Body Diagram and Symbolic Analysis

I began by drawing a free-body diagram of the two-pulley system, identifying the tight-side tension (T₁) and loose-side tension (T₂).

Using the selected initial belt tension, I established the relationship:

T₁ + T₂ = 2T₀ = 2(5) = 10 lbf

I then used the belt-friction (capstan) equation to relate the two tensions:

T₁ / T₂ = e^(μθ)

For equal-diameter pulleys, the belt wrap angle is 180°, or θ = π radians. I used an assumed friction coefficient of μ = 0.32 for the preliminary analysis.

I rearranged these equations symbolically before substituting numerical values. This allowed me to determine the tight-side and loose-side tensions while maintaining the selected total belt tension.

Belt Force Calculations

<img width="828" height="1051" alt="image" src="https://github.com/user-attachments/assets/6cb2bf13-ff73-4485-a0dd-d72f826f47ec" />


Using the assumed friction coefficient and wrap angle:

K = e^(μθ) = e^(0.32π) = 2.733

T₁ = 2T₀K / (1 + K) = 10(2.733) / (1 + 2.733) = 7.32 lbf

T₂ = 2T₀ / (1 + K) = 10 / (1 + 2.733) = 2.68 lbf

The difference between these tensions produces the torque transmitted by the pulley:

M = (T₁ − T₂)(D / 2)

M = (7.32 − 2.68)(1.5) = 6.96 lbf·in

Next, I calculated the allowable belt stress by dividing the specified polyurethane yield strength by the required safety factor:

σ_allow = Sᵧ / N = 471 / 3 = 157 psi

Using the normal stress equation, I calculated the minimum required cross-sectional area:

A_min = T₁ / σ_allow = 7.32 / 157 = 0.0466 in²

For a circular belt cross section:

d_min = √(4A_min / π) = √(4 × 0.0466 / π)

d_min = 0.244 in

Belt Circumference and Selection

Because both pulleys have equal diameters, I used the open-belt length equation:

L = 2C + πD

With a center distance of 5 inches and pulley diameter of 3 inches:

L = 2(5) + π(3)

L = 19.425 in

This represents the approximate belt pitch-line circumference.

I then accounted for the round belt's cross-sectional diameter to estimate its outside circumference:

L_outside ≈ L + πd

L_outside ≈ 19.425 + π(0.250)

L_outside ≈ 20.21 in

For the preliminary component selection, I identified a 1/4-inch-diameter polyurethane round belt from McMaster-Carr, catalog reference 3044K606. The selected diameter is slightly larger than the calculated minimum.

Design Verification

Using a nominal belt diameter of 0.250 inches, I calculated the actual cross-sectional area:

A = πd² / 4 = π(0.250)² / 4 = 0.04909 in²

The resulting normal stress was:

σ = T₁ / A = 7.32 / 0.04909 = 149.1 psi

The calculated safety factor was:

N = Sᵧ / σ = 471 / 149.1 = 3.16

Since the calculated safety factor of 3.16 exceeds the required minimum of 3, the selected 1/4-inch belt diameter satisfies the preliminary tensile-stress requirement.

**Engineering Considerations**

The friction coefficient of μ = 0.32 was an assumed design parameter rather than a verified manufacturer value for this specific belt–pulley combination. Therefore, the calculated belt tensions and transmitted torque depend on that assumption.

The calculated outside circumference is approximately 20.21 inches. The exact stocked belt circumference should be verified against the McMaster-Carr catalog before physical manufacture.


### Part 2 — Shaft Diameter Design

#### Design Approach

The second part of this assignment involved determining the minimum shaft diameter required to transmit torque between the pulleys without exceeding the allowable shear stress. The shaft material specified for this design was AISI 1060 hardened steel, and the required minimum safety factor was 3.

I used the belt tensions calculated in Part 1 to determine the transmitted torque, then applied the torsion equation for a solid circular shaft to calculate the minimum required shaft diameter.

**Knowns and Unknowns**

The known parameters were:

Pulley diameter (D) = 3 in

Pulley radius (r) = 1.5 in

Tight-side belt tension (T₁) = 7.32 lbf

Loose-side belt tension (T₂) = 2.68 lbf

Shaft material = AISI 1060 hardened steel

Required safety factor (N) = 3

The unknowns were the transmitted torque (T), material yield strength (Sᵧ), allowable shear stress (τ_allow), and minimum shaft diameter (d_min).

#### Free-Body Diagram and Torque Calculation

<img width="828" height="1131" alt="image" src="https://github.com/user-attachments/assets/44c05f90-fe36-4765-9572-13c099d858a7" />

I began by drawing a free-body diagram showing the two belt tensions acting tangentially on the pulley and the resulting torque transmitted through the shaft.

Because the tight-side and loose-side belt tensions produce opposing moments about the pulley center, the transmitted torque is calculated using the difference between the two forces multiplied by the pulley radius.

T = (T₁ − T₂)r

T = (7.32 − 2.68)(1.5)

T = 6.96 lbf·in

This torque was used to determine the minimum shaft diameter.

#### Material Selection and Allowable Shear Stress

For the shaft, I used AISI 1060 hardened steel. I referenced Machinery's Handbook, 31st Edition, page 423, Table 11b, to obtain the material properties.

<img width="933" height="1331" alt="image" src="https://github.com/user-attachments/assets/dab34937-6ea1-4a42-b137-b02fb074dfe3" />


For AISI 1060 steel tempered at 400°F, the handbook lists:

Ultimate tensile strength = 160,000 psi

Yield strength (Sᵧ) = 113,000 psi

Brinell hardness = 321 BHN

For the preliminary torsional design, I estimated the allowable shear stress using the maximum-shear-stress (Tresca) criterion with the required safety factor:

τ_allow = Sᵧ / (2N)

τ_allow = 113,000 / (2 × 3)

τ_allow = 18,833.3 psi

This allowable shear stress was then used to calculate the minimum shaft diameter.

Symbolic Shaft Diameter Derivation

For a solid circular shaft subjected to torque, the maximum torsional shear stress is:

τ_max = Tc / J

Where:

T = transmitted torque

c = outer radius of the shaft = d / 2

J = polar moment of inertia = πd⁴ / 32

Substituting these expressions:

τ_max = 16T / (πd³)

Setting the maximum torsional shear stress equal to the allowable shear stress:

16T / (πd³) = Sᵧ / (2N)

Rearranging to solve for the minimum shaft diameter:

d_min = ∛(32NT / (πSᵧ))

Numerical Solution

Substituting the known values:

d_min = ∛[(32 × 3 × 6.96) / (π × 113,000)]

d_min = 0.1235 in

This represents the minimum shaft diameter required to resist the calculated transmitted torque under the preliminary torsion-only loading condition.

Final Shaft Diameter Selection

Rather than selecting a shaft diameter equal to the calculated minimum, I selected a nominal shaft diameter of:

d_selected = 0.250 in (1/4 inch)

This diameter is larger than the minimum calculated value and is compatible with the 1/4-inch journal bearings selected later in Part 3.

Selecting a standard 1/4-inch diameter also provides additional margin against torsional yielding and simplifies the selection of commercially available bearings.

**Engineering Considerations**

The shaft diameter calculation was based on pure torsion. In an actual pulley system, the shaft also experiences transverse forces from the belt tensions, which can produce bending stresses.

Therefore, the calculated minimum diameter is a preliminary torsional requirement rather than a complete combined bending-and-torsion verification. The final shaft arrangement should also account for bearing locations, bending loads, and any geometric features such as shoulders or keyways.


### Part 3 — Journal Bearing Design
#### Design Approach and Calculations

The third part of this assignment involved designing journal bearings to support the rotating shafts while reducing friction and handling the forces generated by the belt-driven pulley system.

I began by identifying the known and unknown parameters, including the selected shaft diameter of 0.250 inches, operating speed of 1500 rpm, bearing pressure, surface velocity, and PV rating. I then used the appropriate bearing equations to determine the operating conditions.

<img width="828" height="1083" alt="image" src="https://github.com/user-attachments/assets/b2e795d2-2454-47ae-b736-3d9172b669b3" />

To determine the load acting on each bearing, I drew a free-body diagram showing the pulley positioned between two journal bearings. I assumed that the pulley was centered between the supports, allowing the total belt load of 10 lbf to be distributed equally.

Based on this arrangement, each bearing carries a radial load of 5 lbf. Using a preliminary bearing length of 0.500 inches, I calculated a bearing pressure of 40 psi, a shaft surface velocity of 98.17 ft/min, and a PV rating of 3,927 psi·ft/min.

<img width="828" height="926" alt="image" src="https://github.com/user-attachments/assets/4f362f6b-7ced-438e-915f-e6e570691c28" />


#### Material and Bearing Selection

I referred to Machinery's Handbook, 31st Edition, page 2440, Table 4, to evaluate suitable journal-bearing materials.

<img width="876" height="1334" alt="image" src="https://github.com/user-attachments/assets/5aebb320-be5e-44ea-9132-b11196f50a2d" />


I selected SAE 841 oil-embedded bronze because its porous structure retains lubricant, helping reduce friction and maintenance requirements. This material is suitable for consideration in a rotating steel-shaft application.

I then searched McMaster-Carr for a commercially available bearing compatible with my selected shaft diameter and bearing length.

The selected component was McMaster-Carr Part #6391K132, an oil-embedded bronze sleeve bearing with a 0.250-inch nominal shaft diameter, 0.375-inch nominal housing diameter, and 0.500-inch length.

<img width="3128" height="1598" alt="image" src="https://github.com/user-attachments/assets/423523ad-436a-49f5-af7d-f02370d85b97" />

<img width="3104" height="1532" alt="image" src="https://github.com/user-attachments/assets/21c15b3f-2927-47a4-9770-9adc052b857e" />


#### Design Verification

To evaluate the selected bearing, I compared my calculated pressure, velocity, and PV values against the operating limits listed in the McMaster-Carr product specifications.

The calculated operating margins were 50 for pressure, 12.22 for velocity, and 12.73 for PV. All three exceeded the required minimum value of 3 under the preliminary loading assumptions.

These results supported my bearing selection. However, the analysis assumes equal loading between two bearings and does not independently establish bearing life or all operating conditions.

**Engineering Considerations**

The selected bearing dimensions are compatible with the preliminary shaft design. For the final system, two bearings would support each shaft, with the pulley positioned between them. The supporting frame must accommodate this arrangement to maintain the assumed load distribution.

This analysis helped me understand how bearing material, dimensions, rotational speed, and applied load influence journal-bearing selection.

### Part 4 — Frame Design
#### Design Approach

The final design stage involved developing a supporting frame for the pulley system. My goal was to create a simple structure that could accommodate the two rotating shafts, maintain the required 5-inch center distance, and provide sufficient clearance around the pulleys.

I used a rectangular plate-style frame concept because it was straightforward to dimension and allowed the bearing locations to be positioned accurately.

#### Frame Geometry and Sketches

I selected the following preliminary frame dimensions:

Length: 10 inches

Height: 5 inches

Thickness: 0.50 inches

Distance between shaft centers: 5 inches

Nominal bearing housing diameter: 0.375 inches

I drew top, front, side, and isometric views to communicate the proposed geometry. The two shaft locations were spaced 5 inches apart, matching the center distance used throughout the belt calculations.

<img width="828" height="1134" alt="image" src="https://github.com/user-attachments/assets/88d83f76-38bd-4eb5-b101-92de8e41c25a" />


#### Material Selection and Engineering Analysis

I selected 6061-T6 aluminum as the proposed frame material because it offers a useful combination of strength, low weight, corrosion resistance, and machinability.

Using an assumed yield strength of 35,000 psi and the required safety factor of 3, I calculated an allowable normal stress of approximately 11,667 psi.

For a preliminary local load check, I used the estimated 5-lbf bearing reaction and the projected contact dimensions of the bearing and frame. This produced an estimated local bearing-support pressure of 26.6 psi, substantially below the allowable material stress.

<img width="828" height="863" alt="image" src="https://github.com/user-attachments/assets/a847536f-661d-4288-9917-2e855438c3f7" />

#### Design Evaluation

The preliminary calculation indicates that the selected aluminum plate has considerable margin against local compressive yielding under the assumed bearing load.

The sketch represents the front support plate. A matching rear support plate would be needed to provide two bearing supports per shaft, consistent with the bearing free-body diagram developed in Part 3.

Although the local bearing-pressure estimate is favorable, it does not establish the bending stress or overall safety factor of the assembled frame. A complete structural verification would require specifying the mounting arrangement, spacing between support plates, and load paths.

This design exercise helped me understand how frame dimensions, bearing placement, material selection, and load distribution must work together to support a rotating mechanical system.



## Decide

After completing the engineering calculations and evaluating the design requirements, I selected the components and dimensions for my pulley system based on their strength, compatibility, availability, and ability to satisfy the preliminary design constraints.

#### Belt Selection

I selected a 1/4-inch-diameter polyurethane round belt from McMaster-Carr (catalog reference 3044K606). The calculated minimum belt diameter was approximately 0.244 inches, so the nominal 0.250-inch belt provided a calculated tensile safety factor of 3.16, slightly exceeding the required minimum of 3.

#### Shaft Selection

I selected a 0.250-inch-diameter AISI 1060 hardened steel shaft. This diameter was larger than the calculated torsion-only minimum of 0.1235 inches and was compatible with commercially available journal bearings. The material's yield strength was obtained from Machinery's Handbook, 31st Edition, page 423, Table 11b.

#### Journal Bearing Selection

For the journal bearings, I selected McMaster-Carr part #6391K132, an SAE 841 oil-embedded bronze sleeve bearing with a 0.250-inch nominal shaft diameter and 0.500-inch length.

I chose this bearing because its dimensions matched my selected shaft and its oil-embedded construction provides lubrication during rotation. The preliminary pressure, velocity, and PV operating margins exceeded 3 under the assumed loading arrangement.

#### Frame Selection

For the supporting frame, I selected a rectangular plate-style design using 6061-T6 aluminum. The proposed plate dimensions were 10 × 5 × 0.50 inches, with the shaft centers positioned 5 inches apart.

I selected aluminum because it provides adequate preliminary local load capacity while remaining lightweight and relatively easy to machine. The frame concept uses two support plates to accommodate two journal bearings per shaft.

#### Final Design Considerations

The selected components form a preliminary pulley-system design that satisfies the calculated belt tensile-stress requirement and the evaluated journal-bearing operating limits under the stated assumptions.

Before manufacturing the system, I would confirm the exact stocked belt circumference, bearing housing fits, frame mounting arrangement, and shaft strength under combined bending and torsion.


## Communicate
#### Engineering Lessons Learned

This assignment helped me understand how different mechanical components must be analyzed together rather than designed independently.

One important concept I learned was how the capstan equation relates friction and the angle of contact to the difference between the tight-side and loose-side belt tensions. I learned that these forces are not equal during power transmission and that their difference determines the torque delivered to the shaft.

I also learned how to use torsional shear stress to determine a minimum shaft diameter and how selecting a standard diameter larger than the calculated minimum can simplify compatibility with other components.

Another important lesson was understanding the relationship between bearing pressure, shaft surface velocity, and PV rating. Before this assignment, I had not fully considered how rotational speed and applied load influence bearing material selection. Comparing my calculations with manufacturer specifications showed me why a bearing cannot be selected based only on its dimensions.

Finally, designing the frame demonstrated the importance of maintaining consistent assumptions between the free-body diagrams and the physical support arrangement. The bearing reaction forces depend on the locations of the supports, so the frame geometry must reflect the conditions used in the calculations.

Overall, this assignment strengthened my understanding of how analytical calculations, material properties, and commercially available components work together during the mechanical design process.












