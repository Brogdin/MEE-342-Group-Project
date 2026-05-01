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

---

## 3. Test Procedures, Results, and Interpretation
* *[Insert testing protocols used]*
* *[Insert data and interpretation of results]*

---

## 4. Comparison with Phase 2 Predictions
* *[Insert analysis comparing Phase 3 results to initial Phase 2 expectations]*

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

## 2. Phase 3 Video: Prototype Demo & Reflection
    
[![Watch the video](https://img.youtube.com/vi/9t-9DwF2vv4/hqdefault.jpg)](https://www.youtube.com/watch?v=9t-9DwF2vv4)

---

## 3. Final Poster and Poster Session

<img width="7200" height="4800" alt="MEE 342 Poster File Group 12 Forklift-1" src="https://github.com/user-attachments/assets/d2d782da-0aaa-4b46-8fa9-36206abd6ecc" />

---
