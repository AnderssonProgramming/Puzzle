# Tilting Tiles Simulator — ICPC Problem F

<p align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/226/226777.png" width="80" title="Java Logo"/>
  <img src="https://pbs.twimg.com/profile_images/1389542262854635522/XAuQWgWp_400x400.png" width="80" title="BlueJ Logo"/>
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c6/ICPC_Foundation_logo.svg/1200px-ICPC_Foundation_logo.svg.png" width="120" title="ICPC Logo"/>
</p>

**Tilting Tiles Simulator** is developed as part of the POOB (Object-Oriented Programming) course at Escuela Colombiana de Ingeniería Julio Garavito. The simulator is inspired by Problem F: "Tilting Tiles" from the 47th ICPC World Finals (Luxor 2023). It aims to mimic a tilting board puzzle where colored tiles move based on the direction of the tilt, with an added twist: a special adhesive called *gummy glue* that makes a tile stick with its neighbors.

> **Note:** This project solves the original ICPC problem. It is built in iterative cycles, with new features and refinements introduced at each stage.

---

## 🚀 Project Development Cycles

### **Cycle 1: Basic Simulator and Initial Tile Manipulation**

- **Objective:** Build a functional simulator for tilting the puzzle.
- **Key Features:**
  - **Puzzle Creation:**  
    - Create a puzzle board based on provided dimensions or preset configurations.
  - **Tile Management:**  
    - Add, relocate, or delete individual tiles.
  - **Glue Application:**  
    - Introduces the first version of a glue mechanism that can be applied over a tile.
  - **Basic Board Tilting:**  
    - Simulate tilts in the four cardinal directions (left, right, toward, and away).
  - **State Verification:**  
    - Compare the current board state with a target configuration.
  - **User Interaction:**  
    - Enable the simulator to be visible (so messages are shown) or invisible (for background processing).
- **Design Focus:**  
  - Clean separation between simulation logic and presentation.
  - Documentation with UML Class and Sequence Diagrams.
- **Tools Used:**  
  - **Java & Maven** (programmed using **BlueJ** as the IDE).  
  - [BlueJ Documentation](https://www.bluej.org/doc/documentation.html)

---

### **Cycle 2: Enhanced Board Interaction and Additional Commands**

- **Objective:** Extend the simulator with additional commands and refine board interaction.
- **Key New Features:**
  - **Board Exchange:**  
    - Ability to swap the reference board with the current editing board.
  - **Intelligent Tilting:**  
    - Improved tilt functionality that better simulates natural movement.
  - **Hole Creation:**  
    - Command to “make a hole” in an empty cell.
  - **Consultation Enhancements:**  
    - Identify and highlight tiles that cannot be moved when tilting.
    - Display the number of tiles missing to meet a target configuration.
- **Design Focus:**  
  - Extensibility: Preparing the codebase for future functionalities.
  - Visual cues: Clear messages when an action cannot be performed.

---

### **Cycle 3: Simulation of Puzzle Resolution**

- **Objective:** Extend the simulator to both mimic and solve the tilting puzzle.
- **Key New Features:**
  - **Problem Resolution Simulation:**  
    - Implement a routine that simulates a potential solution path from the initial to the desired final state.
    - Step-by-step illustration of tile movements.
  - **User Feedback:**  
    - Detailed messages indicating whether a solution was found or if no solution exists.
- **Design Focus:**  
  - Separation of concerns: The core Puzzle class is used solely for simulation, while the resolution logic is modular.
  - Transparent simulation output (each tilt is shown as a step).

---

### **Cycle 4: Final Refactoring and Extension**

- **Objective:** Polish the simulator and introduce new tile and glue types.
- **Key New Features:**
  - **Extended Tile Types:**  
    - **Normal Tile:** Standard, movable tile.
    - **Fixed Tile:** Cannot be relocated or removed.
    - **Rough Tile:** Resistant to sliding.
    - **Freelance Tile:** Ignores glue adhesion.
    - **Flying Tile:** Does not fall into holes.
  - **Extended Glue Types:**  
    - **Normal Glue:** Basic adhesive effect.
    - **Super Glue:** Causes a tile and its adjacent tiles to stick strongly.
    - **Fragile Glue:** Adhesion lasts only for a single tilt.
- **Additional Enhancements:**
  - Refactored the codebase into two packages: `shapes` (handling tile geometry and behavior) and `puzzle` (for the simulation logic).
  - Improved error handling with custom exceptions and logging.
  - Enhanced visual representation for different tile and glue states.
- **Design Focus:**  
  - Meeting full simulation requirements with a clear package structure.
  - Updated UML documentation, including Package Diagrams, generated via Astah.

---

## 📝 Summary of Simulator Components

### **Tiles:**
- **Normal Tile:** Moves with every tilt.
- **Fixed Tile:** Cannot be relocated or eliminated.
- **Rough Tile:** Resistant to sliding.
- **Freelance Tile:** Does not adhere when glue is applied.
- **Flying Tile:** Avoids falling into holes.

### **Glue Types:**
- **Normal Glue:** Basic adhesion.
- **Super Glue:** Strong adhesive effect with adjacent tiles.
- **Fragile Glue:** Temporary adhesion for a single tilt action.

---
## 📸 Project View

- Design
![image](https://github.com/user-attachments/assets/a1dc1d90-621e-4522-a3ce-ed956a9190bc)

- Empty constructor
![image](https://github.com/user-attachments/assets/dd3ae195-83f6-4afc-8495-451e1c62d8b1)

- Starting and ending constructor with different types of tiles and glues
![image](https://github.com/user-attachments/assets/e7c51e57-0af2-44fd-adb6-d6c0adf3a67b)

- Ending constructor
![image](https://github.com/user-attachments/assets/d1f02066-9bcf-4a41-93f7-378c8fb993e6)

- ICPC Problem
![image](https://github.com/user-attachments/assets/7758ad84-1320-4d36-931b-677bcbaaf7de)
![image](https://github.com/user-attachments/assets/6701dfb0-c1ea-4701-90e2-1bc07b0b7e7e)
![image](https://github.com/user-attachments/assets/687d458b-f543-4dcd-a8ac-262de1541281)





## 📚 Additional Information & Documentation

For further details about the development environment:
- **BlueJ** is used for building this project.  
- You can check out the [BlueJ Documentation](https://www.bluej.org/doc/documentation.html) for more information.

---

## 📧 Questions & Further Information

If you have any questions regarding the project requirements or need additional details about how the simulator was developed, please reach out via email:

**andersson.sanchez-m@mail.escuelaing.edu.co**

---

> This repository is a work in progress, built iteratively across multiple cycles to simulate and eventually solve the tilting tiles puzzle. Each development cycle added new commands and refined the simulation, with a focus on clear design, modularity, and extensibility.

Happy coding and enjoy experimenting with the puzzle simulation!
