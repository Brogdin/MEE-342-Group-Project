#  Phase 3 Report:
## 1. Fabrication Details

**Printers Used**
The team utilized an **Elegoo Centauri Carbon**, a **Bambu X2D**, and initially a **Prusa XL**.
* **Elegoo Centauri Carbon:** Required for the PPS-CF parts as it could reach the necessary high nozzle temperatures (320°C).
* **Bambu X2D:** Used for the PETG components (max temperature 300°C).
* **Prusa XL:** Used initially for larger parts before access was lost.

**Filaments & Settings**
* **PETG:** Used for primary structural components to maximize impact resistance. Printed using standard Polymaker profile settings.
* **PPS-CF (Carbon Fiber reinforced):** Used for high-stress rotational and shear components. 
    * **Nozzle Temperature:** 320°C
    * **Bed Temperature:** 85°C
    * **Print Speed:** Slowed from 250mm/s to 100mm/s to ensure proper layer adhesion.

**Infill**
Initial prints were set to 100% infill for maximum density. However, during reprints, the PETG infill was reduced to 50% to conserve limited material while still maximizing structural strength.

**Reprints**
A total of **3 sets of reprints** were required. Notably, the bicep piece was originally printed as two parts on the larger Prusa XL, but after losing access to that printer, it had to be split into three separate parts to fit the smaller build volumes of the remaining printers.

---

## 2. Assembly Procedure and Challenges

* **Slip-Fit Design:** The prototype was designed so that the majority of components connected via a slip fit. This approach allowed for easier alignment and troubleshooting during the initial assembly phase before permanent fixing.
* **Adhesives:** High-strength super glue was utilized to secure slip-fit joints in areas where permanent structural bonds were required or where mechanical tolerances were too loose to hold under vibration.
* **High-Grade Fishing Line Linkages:** For specific dynamic connections—specifically between the gear rack and the pulley wheel—high-grade fishing line as well as the spring and the pin was employed. This provided a high-tensile, low-friction link capable of handling the operational loads of the mechanism.
* **Tolerance Management:** Balancing the "slip fit" dimensions across different printers (Elegoo vs. Bambu) proved difficult, requiring manual sanding in some areas to ensure parts mated correctly.
* **Adhesive Control:** Ensuring super glue did not seep into moving parts or the fishing line tracks during the permanent bonding phase was a significant precision challenge.

Eves updates: please remove this comment/ change wording: 
1. Our group changed the main connections from a slip fit to a very slight press fit dovetail. The orginal slip fit had too large of a gap that super glue was unable to properly connect the two bicep structure parts. 

2. The main bicep structural member was split into three parts. These parts were split along the top, long middle, and the bottom. The splits were slight compression fits made using the bamboo dovetail tool. Our group included these splits to allow the large bicept structure to attach  and hold itself together well in all directions without requiring too much adhesive other than just the transverse direction.

3. The adhesives our group used high-strength super glue. This glue was applied to all joints and areas where permanent structural bonds are required or where mechanical tolerances were too loose.

4. One of the challenges our team faced with press fit is that some of the parts we did not plan to act as press fitted parts acted as if they were press fits. This was mostly seen within the axle for the pawl. Because the axel for the pawl was a a little larger in diameter and acted as a press fit, this axel was sanded down. 

5. For the cables that acted like linkages within the assembly, we used the fishing line that could with stand the tension of 80 pounds. Because the spring could withstand teh tension of 60 pounds, the fishing line would not break under the 60 pounds the spring could hold. This fishing line was thin at 0.8 mm and allowed the string to smoothly sit ontop and not interfere with the other moving parts within our project. The fishing line was used for the dynamic connections between the gear rack and the pulley wheel. It was also used between the spring and the gear rack. Additionally, it was used between the spring and the pin on the forearm section.

6. When first assembling the arm brace, tolerance management was one of the biggest issues. There were a few parts that had the same dimensions on the male and female components. For example, within our ratcheting mechanism, the gear rack struggled to smoothly up and down within the bicep structure's female  component. The male and female components of this section of the assembly were orginally the same size making it impossible for both parts to fit together. To quickly fix this issue, our group chose to sand both the female and male parts so they would work well within our design. Another issue our group faced was teh quality of the adhesive used. The super glue was having trouble attaching to the 3D prints. The super glue would also not dry properly even after waiting a longer time than recommended on the bottle. The super glue was unable to help use fix broken axles because the axels did not have a large amount of surface area to attach to the bicep structure. This still allowed the axel to be broke off the bicep structure easily. 
---

## 3. Test Procedures, Results, and Interpretation
### Testing Objectives
The primary goals of the Phase 3 testing were to verify:
1. **Range of Motion (ROM):** Can the user reach full extension and contraction while the spring is engaged?
2. **Structural Integrity:** Can the connection points (forearm and pin) handle the spring's maximum tension?
3. **Mechanism Logic:** Does the archer release mechanism successfully trigger the tensioning cycle?

### Procedures & Observations
Due to the manufacturing failures noted in section 5, full autonomous mechanism testing was inhibited. To compensate, the team performed a **simulated ratcheting test**:
* **ROM Verification:** By manually holding the pulley to simulate the ratcheting lock, the user was able to move through a full range of motion. The spring successfully extended to the expected length without breaking the housing.
* **FEA Validation:** Components previously analyzed as part of phase 2 in ANSYS—specifically the **forearm component** and the **double-shear pin**—performed exactly as modeled, holding the full force of the spring without deformation.
* **Archer Release Mechanism:** The mechanism was cycled successfully three times. The pin fell into the slot and activated the system as designed. However, on the fourth cycle, the axle for the claw fractured due to fatigue stress.

### Interpretation of Results
The testing proved that the core mechanical logic and the ANSYS-validated components are structurally sound. The system successfully outputted the required torque to meet project goals. The failures encountered were isolated to components that had not undergone FEA (the claw axle) and manufacturing-specific constraints rather than a flaw in the underlying mechanical concept.
---

## 4. Comparison with Phase 2 Predictions

In Phase 2, FEA static stress analysis predicted high Factors of Safety across the board (FoS of 3.3 for the Pin and 2.29 for the Gear Rack). During physical testing, our Phase 2 predictions for these specific parts proved accurate. When we manually simulated the ratcheting mechanism and moved the arm through its full range of motion, the forearm component, the double-shear pin, and the ratchet mechanism loop successfully held the full force of the spring at maximum extension without yielding. The primary discrepancy between our expected Phase 2 operation and our physical prototype was the failure of the archer release mechanism. While the mechanism worked flawlessly for the first three cycles, the claw's axle sheared due to fatigue stress after the third attempt. This failure resulted from a critical analytical oversight during Phase 2 where we missed doing an ANSYS simulation on this specific part. Actual testing yielded further discrepancies regarding the rod mounts and the gear rack. The fracture of the rod mounts directly contradicted our idealized FEA models. This discrepancy occurred because the FEA assumed a perfectly isotropic material and didn't account for the stress concentrations caused by the lack of geometric fillets, nor the inherent weaknesses along the Z-axis layer adhesion lines in 3D-printed PPS-CF. Additionally, Phase 2 assumed smooth geometric engagement between the pawl and the rack. In reality, printer resolution limits resulted in rounded, shallow teeth, changing the angle of engagement and causing slippage well below the expected operational loads. Ultimately, the discrepancies we faced highlight the inherent challenges of iterative engineering. Our team explicitly chose to design a completely novel, custom ratcheting and trigger system from scratch rather than relying on pre-existing, proven designs found online. While this ambitious approach introduced unpredictable variables—such as the un-analyzed axle and print-resolution limits on the gear teeth—it also successfully validated our core mechanics. The design requires minor iteration, but the underlying physics we predicted in Phase 2 hold true.


---

## 5. Detailed Discussion of Failures, Mistakes, and Surprises

Throughout Phase 3, several issues arose during fabrication, assembly, and testing. While the mechanism functioned in concept, many failures originated from manufacturing and material limitations:

* **Pulley Mechanism:** Lacked a retention mechanism, causing it to slide loosely on its intended axle. This created a risk of pulley detachment mid-operation.
* **Gear Rack:** * The lip was too small relative to the printer resolution, resulting in poor quality.
    * Teeth were too shallow to properly engage and lock the mechanism, causing slippage and unreliable tension control.
    * The gear rack lip obstructed desired spring placement.
* **Clearance & Interference:** The pawl was positioned too close to the gear rack mechanism, making it difficult to install the spring in the desired position.
* **Archer Release Mechanism (Critical Failure):** The axle experienced high stress under loading and began to fracture. This was a direct result of material limitations, leading to misalignment and potential premature release of the locking mechanism.
* **Release Block:** The small block required awkward access or a second hand to disengage, which is less than ideal when the system is under load.

**Conclusion:** The observed failures were primarily due to limitations in material strength, print resolution, improper tolerances, and user accessibility rather than flaws in the core concept.

---

## 6. Concrete Design Changes for Second Iteration

Based on the issues identified, the following design improvements will be implemented in the next iteration:

1.  **Pulley System Redesign:** Add shaft collars, clips, or a shouldered axle to prevent lateral movement and reinforce the stationary design.
2.  **Gear Rack Modification:** Increase tooth size and depth to enhance structural integrity, mechanical engagement, and printability. This will minimize slippage and allow for more reliable tension adjustments.
3.  **Tolerance Refinement:** Emphasize additional space for spring incorporation. The gear rack lip will be repositioned to ensure the mechanism fits properly without excessive post-processing.
4.  **Structural Reinforcement:** The archer release mechanism axle will be replaced with a metal component and/or the diameter will be increased to handle higher stress loads.
5.  **Ergonomic Improvements:** The locking and release interface will be reworked into a trigger, lever, or cable-actuated system located on the hand or wrist. This allows the user to safely release the mechanism under load without awkward positioning.

## 7. Summary of Goal of Our Project: 
Our group's goal  was to use this course's time and resources to make a new product instead of repeating a design we could easily find online. Although our group faced many failures during the design and assembly of our arm brace, we are still proud that we had the opportunity to experiment with creating an orignal concept we designed. Additionally, we feel that having this tough experience made us better engineers. We have gained the experience and knowledge of how to design a practical object that can help the community while understanding how to use programs like ANSYS to check that our design will work within real world situations. 

## 2. Phase 3 Video: Prototype Demo & Reflection
    
[![Watch the video](https://img.youtube.com/vi/9t-9DwF2vv4/hqdefault.jpg)](https://www.youtube.com/watch?v=9t-9DwF2vv4)

---

## 3. Final Poster and Poster Session

<img width="7200" height="4800" alt="MEE 342 Poster File Group 12 Forklift-1" src="https://github.com/user-attachments/assets/d2d782da-0aaa-4b46-8fa9-36206abd6ecc" />

---
