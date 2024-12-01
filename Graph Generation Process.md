## Graph Generation Process

We explored four different options for graph generation:

1. **Cloning every vertex** 
2. **Anticloning every vertex** 
3. **Alternating between cloning and anticloning** 
4. **Probabilistic cloning and anticloning (with probability `p`)**
   
### Example Graphs

Below are the example graphs generated during the simulation. Each graph represents the result after a specified number of iterations. 
I used with a specified probability `p`=0.6, and initial_type: 'a' for two connected vertices. 

#### Option 1: Cloning Every Vertex
- **3 Iterations**:
  
  ![Option 1 - 3 Iterations](https://github.com/Ayo1a/Final-research-project/blob/main/example%20of%20different%20graphs/option%201%203%20iterations.png)
- **5 Iterations**:
  
  ![Option 1 - 5 Iterations](https://github.com/Ayo1a/Final-research-project/blob/main/example%20of%20different%20graphs/option%201%205%20iterations.png)

**Description**: The graph starts with two connected vertices. Each new vertex added is a clone of an existing vertex, leading to a dense, connected structure.

#### Option 2: Anticloning Every Vertex
- **3 Iterations**:
  
  ![Option 2 - 3 Iterations](https://github.com/Ayo1a/Final-research-project/blob/main/example%20of%20different%20graphs/option%202%203%20%20iterations.png)
- **5 Iterations**:
  
  ![Option 2 - 5 Iterations](https://github.com/Ayo1a/Final-research-project/blob/main/example%20of%20different%20graphs/option%202%205%20iterations.png)

**Description**: In this option, new vertices are connected to all vertices that are not neighbors of the original vertex. This results in a more sparsely connected graph.

#### Option 3: Alternating Between Cloning and Anticloning
- **3 Iterations**:
  
  ![Option 3 - 3 Iterations](https://github.com/Ayo1a/Final-research-project/blob/main/example%20of%20different%20graphs/option%203%203%20%20iterations.png)
- **5 Iterations**:
  
  ![Option 3 - 5 Iterations](https://github.com/Ayo1a/Final-research-project/blob/main/example%20of%20different%20graphs/option%203%205%20iterations.png)

**Description**: This option alternates between cloning and anticloning in each iteration. This results in a graph that exhibits characteristics of both dense and sparse structures, depending on the iteration.

#### Option 4: Probabilistic Cloning and Anticloning
- **3 Iterations**:
  
  ![Option 4 - 3 Iterations](https://github.com/Ayo1a/Final-research-project/blob/main/example%20of%20different%20graphs/option%204%203%20iterations.png)
- **5 Iterations**:
  
  ![Option 4 - 5 Iterations](https://github.com/Ayo1a/Final-research-project/blob/main/example%20of%20different%20graphs/option%204%205%20iterations.png)

**Description**: The graph is built using a probabilistic approach where cloning and anticloning are alternated based on a probability `p`. This introduces variation in the graph structure.

# Example of Graph Evolution Using Option 4 (Probabilistic Cloning and Anticloning)

## Overview
In this experiment, we are visualizing each step of the graph's creation by the IIM model using **Option 4**, where the graph evolves through **Probabilistic Cloning and Anticloning**. At each iteration, with a specified probability `p`, a vertex may either clone (forming new edges with its neighbors) or anti clone (forming edges with all non-neighboring vertices). We started with initial_type: 'a' for two connected vertices. 

The parameter `p` determines the likelihood of a node choosing cloning over anticloning. For this experiment, we used a probability value of **0.6**, meaning there is a 60% chance for cloning and a 40% chance for anticloning.

## Graph Evolution

The following steps show the evolution of the graph as it goes through multiple iterations. Each step illustrates how the structure of the graph changes based on the probabilistic cloning and anticloning process.

### Step 0: Initial Graph
The initial graph consists of two connected vertices, forming a simple starting structure.

![Step 0 - Initial Graph](https://github.com/Ayo1a/Final-research-project/blob/main/images/step%200%20-%20option%204.png)

### Step 1: First Iteration
In the first iteration, probabilistic cloning and anticloning are applied to the existing nodes. The graph expands as new vertices are added.

![Step 1 - First Iteration](https://github.com/Ayo1a/Final-research-project/blob/main/images/step%201.png)

### Step 2: Second Iteration
In this step, the graph further evolves with additional nodes and edges based on the probabilistic cloning/anticloning process. The structure continues to develop with more complexity.

![Step 2 - Second Iteration](https://github.com/Ayo1a/Final-research-project/blob/main/images/step%202.png)

### Step 3: Third Iteration
By the third iteration, the graph demonstrates more connectivity, showing the impact of both cloning and anticloning decisions on the graph's topology.

![Step 3 - Third Iteration](https://github.com/Ayo1a/Final-research-project/blob/main/images/step%203.png)

### Step 4: Foutrh Iteration
In the fourth iteration, the graph continues to evolve, demonstrating even greater complexity and connectivity. The probabilistic nature of the cloning and anticloning processes leads to further expansion, with new vertices and edges forming according to the probabilistic rules.

![Step 4 - Fourth Iteration](https://github.com/Ayo1a/Final-research-project/blob/main/images/step%204.png)

## Analysis and Observations
- **Clustering Behavior**: As the graph evolves, we observe the clustering effect resulting from cloning (nodes connecting to neighbors) and anticloning (nodes connecting to non-neighbors).
- **Graph Expansion**: Over time, the number of vertices increases, and the graph exhibits more complex relationships between the nodes.
- **Spectral Gap**: We calculated the spectral gap at each iteration, which helps analyze the connectivity and overall structure of the graph.

## Conclusion
This example demonstrates how **Option 4** (Probabilistic Cloning and Anticloning) can generate graphs that evolve based on probabilistic rules. By adjusting the probability parameter `p`, different behaviors and topologies can be observed, offering insights into the underlying dynamics of social networks and complex systems.

In future experiments, we can explore the impact of varying the probability `p` and how it influences the clustering and connectivity of the network over multiple iterations.

