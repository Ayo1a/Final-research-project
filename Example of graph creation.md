# Example of Graph Evolution Using Option 4 (Probabilistic Cloning and Anticloning)

## Overview
In this experiment, we explore the behavior of the Iterative Independent Model (IIM) using **Option 4**, where the graph evolves through **Probabilistic Cloning and Anticloning**. At each iteration, with a specified probability `p`, a vertex may either clone (forming new edges with its neighbors) or anti clone (forming edges with all non-neighboring vertices). We started with initial_type: 'a' for two connected vertices. 

The parameter `p` determines the likelihood of a node choosing cloning over anticloning. For this experiment, we used a probability value of **0.6**, meaning there is a 60% chance for cloning and a 40% chance for anticloning.

## Graph Evolution

The following steps show the evolution of the graph as it goes through multiple iterations. Each step illustrates how the structure of the graph changes based on the probabilistic cloning and anticloning process.

### Step 0: Initial Graph
The initial graph consists of two connected vertices, forming a simple starting structure.

[![Step 0 - Initial Graph](images/step_0_option 4.png)](https://github.com/Ayo1a/Final-research-project/blob/main/images/step%200%20-%20option%204.png)

### Step 1: First Iteration
In the first iteration, probabilistic cloning and anticloning are applied to the existing nodes. The graph expands as new vertices are added.

![Step 1 - First Iteration](images/step_1_first_iteration.png)

### Step 2: Second Iteration
In this step, the graph further evolves with additional nodes and edges based on the probabilistic cloning/anticloning process. The structure continues to develop with more complexity.

![Step 2 - Second Iteration](images/step_2_second_iteration.png)

### Step 3: Third Iteration
By the third iteration, the graph demonstrates more connectivity, showing the impact of both cloning and anticloning decisions on the graph's topology.

![Step 3 - Third Iteration](images/step_3_third_iteration.png)

## Analysis and Observations
- **Clustering Behavior**: As the graph evolves, we observe the clustering effect resulting from cloning (nodes connecting to neighbors) and anticloning (nodes connecting to non-neighbors).
- **Graph Expansion**: Over time, the number of vertices increases, and the graph exhibits more complex relationships between the nodes.
- **Spectral Gap**: We calculated the spectral gap at each iteration, which helps analyze the connectivity and overall structure of the graph.

## Conclusion
This example demonstrates how **Option 4** (Probabilistic Cloning and Anticloning) can generate graphs that evolve based on probabilistic rules. By adjusting the probability parameter `p`, different behaviors and topologies can be observed, offering insights into the underlying dynamics of social networks and complex systems.

In future experiments, we can explore the impact of varying the probability `p` and how it influences the clustering and connectivity of the network over multiple iterations.

