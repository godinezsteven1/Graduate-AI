# PathFinding-AI

This project implements an AI agent to solve a variant of the **graph coloring problem** on a dynamically generated grid using a limited set of brush shapes and colors. Built for the **"Shapeshifting Coloring Problems"** assignment, 
this project simulates an environment where an agent colors cells under strict adjacency constraints using local search techniques.

> **Goal:** Fill a grid using the fewest possible brush placements and colors such that **no adjacent cells share the same color**.

---

## Project Overview

Given PyGame-based grid environment and tasked with building an AI agent:

- Moves a virtual brush across the grid
- Chooses from 9 distinct brush shapes
- Chooses from 4 color options
- Places shapes without overlapping or violating adjacency constraints

The agent completes the coloring using **local search** technique Simulated Annealing


---

## Features Implemented

-  **Grid Coloring Agent**
  - Navigates grid 
  - Switches between brush shapes and colors
  - Places shapes only where valid
  - Avoids adjacent same-colored cells

-  **Local Search Strategy**
  - Color selection avoids immediate conflicts
  - Agent retries/re-evaluates when placement fails

-  **Visualization**
  - Uses PyGame to show live grid state
  - Current brush shape and color rendered on hover
  - Final coloring viewable with color-coded grid

---

## Sample Output

-  Valid colored grid with no adjacency violations
-  17 placed shapes 
- Runtime: ~3.07 seconds 

---

## Technologies & Concepts

- **NumPy** (used indirectly in env)
- **Local Search (Simulated Annealing / Hill Climbing)**
- **Constraint Satisfaction**
- **Brush Placement & Shape Rotation**
- **Graph Coloring Applications**

---

## Other Restraints

- All code interactions with the environment occur **only through `execute()`**
- No direct grid manipulation allowed
- AI model built and trained from scratch
- Collaborations & AI tool usage are clearly cited per assignment rules

---

## Access & Usage

This repository is part of a **university assignment**. To comply with academic policies, only the high level logic and output are shared publicly. For full code access, please refer to the main README or contact me directly.

---
