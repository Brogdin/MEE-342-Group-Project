# Phase 2 Submission
###Test to see change 
## Phase 2 Report

### Overview of Your Final Design
*(Insert Key CAD Images here)*

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

### Discussion of Design for Assembly and Design for 3D Printing
The design was developed with 3D printing in mind for both the manufacturing and assembly phases. While some components are simple enough to be produced in a single small print, others are larger or more complex, requiring the system to be broken down into smaller, more manageable parts that can be printed separately and assembled afterward. One method used to achieve this is through dovetail joints or similar interlocking features, which allow for easier printing while still maintaining structural integrity once fully assembled. [Image of 3D printed dovetail joint]

The strength and reliability of the 3D printed components are intended to be improved through the use of axles, hinges, and other load-bearing features that help support and align layered prints. For example, axles would be used within the ratcheting pulley system to support each pulley wheel, allowing for smoother cable motion and reduced friction during operation. Tolerances within +/- 0.005 of an inch will be considered between mating parts to ensure proper fit without excessive friction, allowing for smooth movement in both the ratcheting and archer trigger mechanisms. Clearance will also be a minimum of 0.005 inches between all moving parts.

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
