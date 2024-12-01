# Results and Conclusions 

In this document, we summarize the results of the Iterative Independent Model (IIM) graph simulation and present conclusions drawn from the analysis. The simulations were conducted with various options for graph generation, and key metrics such as spectral gap, graph diameter, and connectivity were evaluated.

## Graph Generation Process

We explored four different options for graph generation:

1. **Cloning every vertex** 
2. **Anticloning every vertex** 
3. **Alternating between cloning and anticloning** 
4. **Probabilistic cloning and anticloning (with probability `p`)**

## Results

### Example Graphs

Below are the example graphs generated during the simulation. Each graph represents the result after a specified number of iterations.

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

### Spectral Gap Analysis

We ran the simulation 20 times and calculated the spectral gap for each run. The average spectral gap is calculated as follows:

- **Average Spectral Gap**: `XX.XX`

#### Spectral Gap Distribution
![Spectral Gap Distribution](images/spectral_gap_distribution.png)

**Description**: The plot shows the distribution of spectral gaps over 20 runs. This helps to understand how the spectral properties of the graph vary across different simulations.

## Conclusions

The results from the simulation show the following:

- The graph's spectral gap is closely related to the graph structure, and a higher spectral gap indicates better connectivity.
- Alternating cloning and anticloning introduce a unique balance between density and sparsity in the graph structure.
- The probabilistic approach introduces variability, which can lead to graphs with more varied spectral gaps.
- The IIM model's ability to model social networks and clustering behavior was evident from the graph structure and spectral properties.

### Next Steps

Further experiments can be conducted by varying the parameters, such as the probability `p`, to investigate its impact on the overall graph structure and spectral gap.

---

### Notes:
1. Replace `XX.XX` with the actual average spectral gap you calculated.
2. Ensure all images mentioned are saved in the `images/` folder.
3. Verify the file renders correctly on GitHub.

