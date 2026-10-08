SLE-3: Architecture Design of a Grid-Based Pathfinding System
Project Title
Architecture Design of a Grid-Based Pathfinding System
1. Project Overview
The Grid-Based Pathfinding System is an AI-based system designed to find
a path between a starting point and a goal point in a grid environment.
The grid may contain obstacles that the pathfinding algorithm must
avoid.
The system uses:
- Breadth-First Search (BFS)
- A* Search
- Manhattan Distance heuristic for A*
This SLE-3 activity represents the system architecture using the C4
Model.
2. Objectives
- Represent the pathfinding system using the C4 architecture model.
- Show how the user interacts with the system.
- Identify the major containers of the system.
- Break down the Search Engine into its internal components.
- Connect the architecture with the actual implementation elements.
- Document the design decisions made for the system.
3. C4 Model
Level 1 -- Context Diagram
The Context Diagram shows the complete Grid-Based Pathfinding System and
the external User / Operator.
User / Operator → Grid-Based Pathfinding System
The user provides:
- Grid
- Start point
- Goal point
- Obstacles
Grid-Based Pathfinding System → User / Operator
The system returns the calculated path as the path output.
Level 2 -- Container Diagram
The major containers identified in the system are:
1. Input Module -- Accepts and validates the grid, start point,
   goal point, and obstacles.
2. Search Engine -- Performs pathfinding using BFS or A*.
3. Heuristic Module -- Calculates the Manhattan Distance used by
   A*.
4. Memory / Visited Set -- Stores visited nodes and search state.
5. Output Module -- Generates and displays the final path or search
   result.
Level 3 -- Component Diagram
The Search Engine is selected as the main container for detailed
component-level design.
Its internal components include:
- Frontier / Open List -- Stores nodes waiting to be explored.
- Goal Test -- Checks whether the current node is the goal.
- Explored / Closed Set -- Tracks visited nodes.
- Path Reconstructor -- Builds the final path using parent-node
  information.
Level 4 -- Code Level Overview
  Main Element                        Responsibility
  Grid / Maze representation          Represents the grid, start, goal,
                                      and obstacles.
  bfs()                             Performs Breadth-First Search.
  astar()                           Performs A* search.
  heuristic() / Manhattan Distance  Estimates the remaining distance to
                                      the goal for A*.
  reconstruct_path()                Reconstructs the final path after
                                  the goal is reached.
4. Repository Structure
SLE-3/
│
├── README.md
├── SLE3_Full_C4_Architecture_Design_FINAL.docx
├── diagrams/
│   ├── context_diagram.png
│   ├── container_diagram.png
│   └── component_diagram.png
└── AI_CONTRIBUTION_LOG.md
Exact filenames may be adjusted when the final files are uploaded.

5. Design Decisions
- The architecture separates input, search, heuristic calculation,
  memory, and output responsibilities.
- BFS and A* are represented inside the Search Engine because both
  solve the same pathfinding problem using different search
  strategies.
- Manhattan Distance is represented separately because it is used as
  the heuristic for A*.
- The architecture is kept simple and readable to avoid unnecessary
  containers and crowded diagrams.
6. Technologies / Tools
- Python -- Pathfinding implementation
- BFS -- Uninformed search algorithm
- A* -- Informed search algorithm
- Manhattan Distance -- A* heuristic
- draw.io / diagrams.net -- Architecture diagrams
- Microsoft Word -- SLE-3 documentation
- GitHub -- Version control and submission
7. AI Contribution
AI assistance was used during the SLE-3 activity for:
- Understanding the C4 Model.
- Planning the architecture levels.
- Organizing the system into Context, Container, Component, and Code
  levels.
- Planning diagram elements and interactions.
- Improving documentation and explanations.
- Preparing the AI Contribution Note.
8. Student Contribution
The student:
- Selected the Grid-Based Pathfinding System from the previous SLE-2
  work.
- Worked with BFS and A* pathfinding.
- Used Manhattan Distance as the A* heuristic.
- Reviewed and selected the major system containers.
- Selected the Search Engine for component-level decomposition.
- Created, arranged, and reviewed the C4 diagrams.
- Prepared and verified the final SLE-3 documentation.
- Verified that the architecture represents the actual pathfinding
  system.
9. Conclusion
The SLE-3 activity represents the Grid-Based Pathfinding System using
all four levels of the C4 Model. The Context level shows the external
user interaction, the Container level shows the major system parts, the
Component level explains the internal structure of the Search Engine,
and the Code level identifies the main implementation elements.
This architecture provides a clear connection between the system design
and the BFS/A* pathfinding work completed in the previous SLE
activities.
