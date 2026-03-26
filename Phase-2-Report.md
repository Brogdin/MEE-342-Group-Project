# Phase 2 Submission

## Phase 2 Report

### Overview of Your Final Design
*(Insert Key CAD Images here)*
#### Full 3D Assembly:
Image of Rack: 

Image of Pawl: 

Image of Claw: 

Image of Forearm Structural Member: 

Image of Bicep Structural Member: 


#### Drawings and Views: 
Rack Part Drawing: 

Pawl Part Drawing:

Claw Part Drawing: 

Forearm Structural Member Part Drawing:

Bicep Structural Member Part Drawing:

Exploded View of the Assembly: 

Basic Motion Animation Showing Mechanism in Operation: 

#### Printability: 
Ensure Parts are Sized within the Build Volume of the 3D Printer:
Our group owns a Bambu Lab P1S printer. The build volume of this printer is 256mm by 256mm by 256mm. This is 10 inches by 10 inches by 10 inches. The longest part our group plans to print is 20.5 inches long. 
This length exceeds the build volume of our printer. To address this issue, our group will separate this long part into two parts, add dove tails to where these parts are divided, then print each part. Afterwards, the dove tail pattern will be used to attach the parts together. Dove tails allows the parts to be printed in smaller portions and can be reattached while allowing the structure to stay strong and act as if it was a single member. 



### Description of Major Design Decisions and Changes from Phase 1
The initial Phase 1 design utilized a pneumatic cylinder connected through a ball and socket joint to provide tension for assisting the bicep in lifting loads, with fabric braces positioned along the arm for support. The system was originally intended to support approximately 20 pounds of additional overhead weight. However, recent feedback from Phase 1 and further design evaluation resulted in several major changes implemented in Phase 2 for improved usability, safety, and mechanical efficiency.

The pneumatic cylinder and pin-based adjustment system were removed and replaced with an updated ratcheting system consisting of a linear pawl, pulley, and gear rack to regulate and adjust the tension in the system. [Image of a linear ratchet and pawl mechanism] Additionally, an archer-style mechanism trigger was introduced, including a cable, claw, and trigger interface, which allows the user to engage and disengage tension with minimal effort. This directly addresses feedback indicating that the system should require less input from the user’s opposite arm.

Several structural changes were adjusted to improve stability and comfort:
* **Rigid Bars:** Two rigid bars were added along the outer portion of the arm, secured with fabric straps, replacing the previous brace configuration located between the bicep and forearm.
* **Spring Repositioning:** The spring now runs around the middle length of the user’s arm.
* **Trigger Placement:** The archer mechanism is located near the elbow to better control the release in tension.
* **Secondary Wheel System:** Introduced to guide and temporarily lock in the disengaged cord until it is manually reset.

These modifications reduce user effort, improve the control of tension, and enhance the reliability of the system while maintaining its intended functional purpose.

### Detailed Explanation of Required Analyses
*(Provide detailed explanation of Shaft, Gear, Fatigue, Bearings, Interfaces, etc., with clear assumptions and results)*

Section 1.) Static Stress and Factor of Safety: 
Critical Part: Rack

Analysis Results and Discussion about Rack: 
The rack was analyzed using PPS-CF as the material. The mechanical properties of PPS-CF are as follows:
Material: PPS-CF (Printed & Annealed Filament)
Density = 1260 kg/m^3
Isotropic Elasticity:
Young's Modulus = 8.23E+09 Pa
Poisson's Ratio = 0.39
Shear Modulus   = 2.96E+09 Pa
Bulk Modulus    = 1.247E+10 Pa
Strength:
Tensile Yield Strength      = 8.70E+07 Pa
Compressive Yield Strength  = 9.00E+07 Pa
Tensile Ultimate Strength   = 8.70E+07 Pa
Compressive Ultimate Strength = 1.05E+08 Pa

Loading for the rack was 30lbs (135N) loaded onto one of the teeth to simulate the pawl pushing on the tooth of the rack. 

Results: Max von-misses stress was roughly 40MPa, which is significantly below yield for PPS-CF. Previously, the rack did not have fillets on the edge of the teeth which had initially led to a stress of close to 70MPa but after adding in fillets the results improved and the stress concentration reduced greatly.

Image of Rack Mesh: 

<img width="778" height="437" alt="mesh rack" src="https://github.com/user-attachments/assets/e2738a33-f6fb-41a6-8fcf-6070a5183a7f" />

Image of Boundary Conditions and Loading: 

<img width="778" height="360" alt="rack loading" src="https://github.com/user-attachments/assets/c824e1a8-8fe3-4e7c-b28d-ca7c9d781bbe" />

Image of Bending and Torsional Stresses: 

<img width="775" height="366" alt="rack stress" src="https://github.com/user-attachments/assets/7fbb4dc5-653c-4751-9b51-66974f957968" />

Image of Total Deformation: 

<img width="777" height="365" alt="rack total deformation" src="https://github.com/user-attachments/assets/e512ad89-c685-46fb-8172-6b3d7ea75c4b" />

Image of Stress on Tooth: 

<img width="776" height="366" alt="tooth stress" src="https://github.com/user-attachments/assets/d430dccd-ff8a-415d-af6f-f007770b1dd5" />

Factor of Safety: 2.29


Critical Part: Pawl
Analysis Results and Discussion about Pawl: 
The pawl was analyzed using PPS-CF as the material. Properties can be seen above.
The loading for the pawl was 30lbs (135N) loaded on the face of the pawl that contacts the tooth of the rack. 
Results: relatively low Von-Misses Stress of 8.5MPa on the underside of the pawl where the pawl experienced significant bending.

Image of Pawl Mesh: 

<img width="778" height="423" alt="pawl mesh " src="https://github.com/user-attachments/assets/6099d872-d4cf-4fb5-a80b-530b6216952e" />

Image of Boundary Conditions and Loading: 

<img width="780" height="361" alt="pawl loading " src="https://github.com/user-attachments/assets/8c44c5fe-266b-4e67-9940-dd30b157fb15" />

Image of Bending and Torsional Stresses: 

<img width="777" height="359" alt="Pawl stress" src="https://github.com/user-attachments/assets/ecb08eae-0b15-498c-8911-262a82bd9911" />

Image of Total Deformation: 

<img width="779" height="363" alt="pawl deformation" src="https://github.com/user-attachments/assets/e7c36291-2212-4aa2-8172-a3c4fb9b45a0" />

Factor of Safety: 28.19


Critical Part: Forearm Structural Member
Analysis Results and Discussion about Forearm Structural Member: 
The forearm structural member was analyzed using PETG. Initially, PPS-CF was used for analysis, but after seeing the results, and considering the repeated impact to the part, the material was changed to PETG due to its improved impact resistance and because it is more cost effective compared to PPS-CF as well as easier to print with. Material properties are listed below:
Material: PETG (Printed Filament)
Density = 1270 kg/m^3
Isotropic Elasticity:
Young's Modulus = 2.10E+09 Pa
Poisson's Ratio = 0.38
Shear Modulus   = 7.61E+08 Pa
Bulk Modulus    = 2.29E+09 Pa
Strength:
Tensile Yield Strength        = 5.00E+07 Pa
Compressive Yield Strength    = 5.50E+07 Pa
Tensile Ultimate Strength     = 5.00E+07 Pa
Compressive Ultimate Strength = 6.50E+07 Pa

Loading for the structural member was 60lbs (270N) applied in 3 different load cases. These 3 loadcases were at 0deg from the vertical axis, +60 deg from the vertical axis and -60 deg from the vertical axis. The 3 loadcases were ran to analyze different arm angles and how the force applied by the pin impacts the arm.

Results: low von misses stress around 3-5MPa depending on the angle, PETG is a suitable material for this part.

All Results with Force Pointing to the Right: 
Image of Forearm Structural Member Mesh: 

<img width="775" height="427" alt="for mesh " src="https://github.com/user-attachments/assets/ace11faa-30ac-481a-9400-6c963b44420a" />

Image of Boundary Conditions and Loading: 

<img width="780" height="361" alt="for load" src="https://github.com/user-attachments/assets/f6ad5d5d-91d3-456f-90c6-998477db4904" />

Image of Bending and Torsional Stresses: 

<img width="781" height="363" alt="for def" src="https://github.com/user-attachments/assets/9905f8a5-caab-49e5-95a2-af5e9c24b59d" />

Image of Total Deformation: 

<img width="775" height="361" alt="stress" src="https://github.com/user-attachments/assets/1e0c9139-2208-47e9-8eaa-f22db28417a5" />

All Results with Force Pointing to the Away from Viewer: 
Image of Boundary Conditions and Loading: 

<img width="781" height="364" alt="21" src="https://github.com/user-attachments/assets/22de5e05-b1a1-4131-b045-ac6d4e57b0cf" />

Image of Bending and Torsional Stresses: 

<img width="778" height="358" alt="22" src="https://github.com/user-attachments/assets/ad48719e-9018-49e8-9d92-8d4091d26e92" />

Image of Total Deformation: 

<img width="776" height="365" alt="23" src="https://github.com/user-attachments/assets/5833ace9-80f4-4b61-9deb-02d43c37d427" />

All Results with Force Pointing to the Left: 
Image of Boundary Conditions and Loading: 

<img width="777" height="361" alt="24" src="https://github.com/user-attachments/assets/6f2dee26-33f3-4661-8bf9-32fe26d87e1c" />

Image of Bending and Torsional Stresses: 

<img width="777" height="363" alt="26" src="https://github.com/user-attachments/assets/8d947b6e-0d78-4a79-878f-7d84ceb3f641" />

Image of Total Deformation: 

<img width="778" height="363" alt="27" src="https://github.com/user-attachments/assets/fd299c7f-503b-47c6-8a7e-414debbb584a" />

Factor of Safety: 12.73 (For all directions of force)

Critical Part: Pin
Analysis Results and Discussion about Pin: 
The pin was analyzed with PPS-CF as the material. This was done because the pin is placed in double shear with the forea50rm support piece as well as the fishing line. The improved strength of PPS-CF was chosen as suitable for this double shear loading.
Loading: the pin was loaded in double shear, the forearm support covers the center 0.5” of the pin, and the fishing line applies a 60lb force in the opposing direction of the fixed face.
Results: Von Mises stress of 23MPa in double shear. SF of 3.3 for max shear. The pin will be able to handle the loads we expect to apply to it.

Image of Pin Mesh: 

<img width="775" height="426" alt="Screenshot 2026-03-25 221201" src="https://github.com/user-attachments/assets/a73e77da-96eb-48ee-b53d-537357b22027" />

Image of Boundary Conditions and Loading: 

<img width="776" height="360" alt="Screenshot 2026-03-25 221220" src="https://github.com/user-attachments/assets/1e20a1ac-a3a6-4991-9280-bb4d812ee320" />

Image of Bending and Torsional Stresses: 

<img width="777" height="358" alt="Screenshot 2026-03-25 221239" src="https://github.com/user-attachments/assets/9a24b2e9-009c-4cba-981c-0cff8ad1bd76" />

Image of Total Deformation: 

<img width="778" height="355" alt="Screenshot 2026-03-25 221258" src="https://github.com/user-attachments/assets/7a64c1b3-e55a-49eb-ba79-b814a1069a3c" />

Factor of Safety: 3.3

<img width="780" height="364" alt="Screenshot 2026-03-25 221318" src="https://github.com/user-attachments/assets/bfd2f099-c8f1-4765-be69-7c43e3ed2c35" />


Section 2.) Fatigue Assessment 

Estimating Alternating and Mean Stresses Under Expected Repeated Loading: 

<img width="802" height="385" alt="Screenshot 2026-03-25 221704" src="https://github.com/user-attachments/assets/e9d8545b-fe94-46a1-8cde-918d50f9e800" />

<img width="1010" height="336" alt="Screenshot 2026-03-25 221758" src="https://github.com/user-attachments/assets/380078f1-c51d-4436-bd1f-0a1bb4060518" />

<img width="779" height="364" alt="Screenshot 2026-03-25 221817" src="https://github.com/user-attachments/assets/4f9aa185-0f22-4a4d-b4a5-50c4133aea34" />

Estimating Factor of Safety against Fatigue: 12.73 (Found within Section 1 of Forearm Structure Member)

### Discussion of Design for Assembly and Design for 3D Printing
The design was developed with 3D printing in mind for both the manufacturing and assembly phases. While some components are simple enough to be produced in a single small print, others are larger or more complex, requiring the system to be broken down into smaller, more manageable parts that can be printed separately and assembled afterward. One method used to achieve this is through dovetail joints or similar interlocking features, which allow for easier printing while still maintaining structural integrity once fully assembled. [Image of 3D printed dovetail joint]

The strength and reliability of the 3D printed components are intended to be improved through the use of axles, hinges, and other load-bearing features that help support and align layered prints. For example, axles would be used within the ratcheting pulley system to support each pulley wheel, allowing for smoother cable motion and reduced friction during operation. Tolerances within +/- 0.0625 of an inch will be considered between mating parts to ensure proper fit without excessive friction, allowing for smooth movement in both the ratcheting and archer trigger mechanisms. Clearance will also be a minimum of 0.0625 inches between all moving parts.

The design minimizes the number of unique fasteners where possible to reduce complexity and potential errors during assembly. Additionally, components are designed to be modular so that individual parts can be easily replaced if failure occurs. Overall, the system is intended to balance performance, manufacturability, and ease of assembly, making it well-suited for implementation using standard 3D printing methods.

### Anticipated Risks or Weaknesses to be Addressed in Prototyping
With the addition of the new ratchet pulley system and archer trigger system, the increase in moving parts introduces new risks related to failure and misalignment:
* **Wear and Fatigue:** Both systems are prone to wear and fatigue from repetitive motion (e.g., pawl and gear tooth contact degradation), which could lead to slippage within the cord and gear rack, ultimately resulting in system failure.
* **Trigger Mechanisms:** The archer trigger mechanism may be susceptible to accidental release or delayed disengagement, potentially causing a sudden downward motion of the arm that could result in discomfort or minor injury.
* **Interface Wear:** The claw interface within the trigger mechanism may experience wear over time due to stress concentration at the contact points, causing rounding of the tips and increased cable slippage.
* **Structural Slippage:** Slippage around the arm bars due to uneven loading or user movement may occur, reducing effective force transfer and creating instability during operation.
* **Cable Issues:** The pulley system introduces the risk of cable tangling or jamming, which could prevent the user from properly releasing spring tension.
* **Energy Release:** Any failure within these interconnected systems could lead to the uncontrolled release of stored energy in the spring, posing further safety risks to the user.

---

## Phase 2 Video: Detailed Design & CAD Walkthrough

### Guided Tour of the CAD Assembly and Key Parts
*(Insert video link or details here)*

### Short Motion Study Demonstration
*(Insert video link or details here)*

### Explanation of how Analysis Informed Changes to Geometry and Material Choices
*(Insert details here)*
