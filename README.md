# Cricket Elimination using Ford-Fulkerson Algorithm

This project implements the **Cricket Elimination** problem using the **Ford-Fulkerson Algorithm** (Max-Flow Network) to determine when a team is mathematically eliminated from a tournament. The tool analyzes current standings and remaining matchups to assist in algorithmic decision-making.

---

## 📌 Project Overview

In sports tournaments, a team can be eliminated long before they mathematically lose all chances. Determining this "elimination point" is trivial when considering only basic wins and losses, but it becomes a complex network flow problem when factoring in the remaining head-to-head matches between other competing teams.

This project models the problem as a network flow graph where:
- **Source to Match Nodes:** Represents the remaining games to be played between pairs of teams.
- **Match Nodes to Team Nodes:** Distributes the potential wins from those matches.
- **Team Nodes to Sink:** Constrains how many more wins a team can achieve without knocking out the team in question.

If the maximum flow fills all match capacities from the source, the team is still alive. Otherwise, they are mathematically eliminated.

---

## 📂 Repository Structure

* **`project.cpp`**: The core C++ source code containing the network flow graph construction and the Ford-Fulkerson algorithm implementation.
* **`input4.txt`**: Sample input data configuration file representing tournament standings (teams, current wins, losses, remaining matches, and a matrix of head-to-head remaining games).
* **`description.pdf`**: Detailed documentation explaining the theoretical background, constraints, and algorithmic design of the project.

---

## 🛠️ Getting Started

### Prerequisites
To compile and run this project, you need a C++ compiler (like `g++`) installed on your system.

### Compilation
Compile the source code using the following command in your terminal:
```bash
g++ -O3 project.cpp -o cricket_elimination
