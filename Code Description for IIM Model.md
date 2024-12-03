### **Code Description for IIM Graph**

The provided Python code implements the Iterative Independent Model (IIM) for graph generation and analysis. The model simulates a social network structure based on the concepts of *cloning* and *anticloning* vertices across several iterations. Here's a breakdown of the different components:

- **IIM_Graph Class**: This class contains various methods to create graphs using the Iterative Independent Model (IIM). It includes functionality to simulate cloning, anticloning, and probabilistic cloning/anticloning.

#### **Methods in the Code:**

1. **create_graph**:
   - This function generates a graph using one of four different options for the iteration process:
     - **Option 1**: Clone every vertex.
     - **Option 2**: Anticlone every vertex.
     - **Option 3**: Alternate between cloning and anticloning.
     - **Option 4**: Probabilistic cloning or anticloning based on a probability `p`.

2. **clone**:
   - This method clones each vertex in the graph by creating a new node and connecting it to the same neighbors as the original vertex. Additionally, the original vertex is connected to its clone.

3. **anticlone**:
   - This method creates an "anticlone" by adding a new vertex connected to all other vertices that are not neighbors of the original vertex.
   
### Examples of creating graphs by the model
Option 1: Cloning Every Vertex 
![](https://github.com/Ayo1a/Final-research-project/blob/main/images/Examples%20of%20creating%20graphs.png)
**for more examples click on this ![Link](https://github.com/Ayo1a/Final-research-project/blob/main/Graph%20Generation%20Process.md)**

4. **probabilistic_copy**:
   - For each vertex, a probabilistic decision is made: with probability `p`, the vertex is cloned, and with probability `1-p`, it is anticloned. This mimics a more realistic model where the expansion of a node's neighborhood can follow either pattern with some randomness.

5. **draw_graph**:
   - This function visualizes the graph at each iteration using the `matplotlib` library. It labels each vertex and displays the graph after each step.

6. **calculate_diameter**:
   - This method computes the graph diameter (the longest shortest path between any two vertices), provided the graph is connected. If the graph is disconnected, it returns a message indicating the diameter is undefined.

7. **compute_laplacian**:
   - This function computes the normalized Laplacian matrix of the graph. It also visualizes the adjacency matrix, degree matrix, inverse square root of the degree matrix, and the normalized Laplacian matrix using heatmaps.  Let \( D \) denote the diagonal degree matrix of G, we define the normalized Laplacian matrix \( L \) of G as ![](https://github.com/Ayo1a/Final-research-project/blob/main/images/Laplacian.PNG)

**![Here](https://github.com/Ayo1a/Final-research-project/blob/main/Results%20of%20Laplacian%20Matrices.md), you can visually explore the matrices involved in the calculation in the endpoint**
    ![](https://github.com/Ayo1a/Final-research-project/blob/main/images/full%20visual%20laplasian%20calculation.png)
    ![](https://github.com/Ayo1a/Final-research-project/blob/main/images/visual%20laplasian.png)

8. **calculate_spectral_gap**:
   - This function calculates the spectral gap of the graph, which is the difference between the second smallest eigenvalue and the largest eigenvalue of the normalized Laplacian. The spectral gap is important for understanding the graph’s clustering properties.

9. **create_and_draw_steps**:
   - This method generates the graph step by step (across multiple iterations) and visualizes the process, showing the graph at each step.

### Recent Code Enhancements  

**step-by-step graph visualization** and **spectral gap analysis**. These enhancements enable a more detailed exploration of graph evolution and connectivity metrics. Users can now:  
1. Visualize the graph structure at each iteration step.  The create_and_draw_steps method allows you to visualize the evolution of the graph after each iteration, providing an intuitive way to understand the effects of different options.
2. Run simulations multiple times (e.g., 20 times) to calculate the average spectral gap, providing a statistical perspective on graph properties.  


---

### **Example Usage**

The main code at the end of the script demonstrates how to use the `IIM_Graph` class. Here's a brief summary:

- The graph is created using `create_graph` with the specified option (e.g., `option = 4` for probabilistic cloning/anticloning) and initial type (e.g., `'a'` for two connected vertices).
- The graph is visualized after each iteration using the `draw_graph` method.
- The Laplacian matrix of the graph is computed and visualized.
- The spectral gap of the graph is calculated and printed.

---

### **Further Modifications**

- **Option 4**: In `create_graph`, there’s a placeholder for probabilistic cloning/anticloning (commented-out). You can adjust the logic or probability threshold to test different randomization strategies.
  
- **Scalability**: As the graph grows with iterations, the computational complexity (especially for the diameter and Laplacian) can become challenging. The provided methods assume that the graph remains manageable in size for efficient calculation.

---

This code offers a versatile implementation to simulate and analyze social network-like graphs generated by the Iterative Independent Model (IIM) with options for both deterministic and probabilistic graph expansion.
