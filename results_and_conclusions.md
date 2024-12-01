# Results and Conclusions

In this document, we summarize the results of the Iterative Independent Model (IIM) graph simulation and present conclusions drawn from the analysis. The simulations were conducted with various options for graph generation, and key metrics such as spectral gap, graph diameter, and connectivity were evaluated.

## Graph Generation Process

We explored four different options for graph generation:

1. **Cloning every vertex** 
2. **Anticloning every vertex** 
3. **Alternating between clone and anticloning** 
4. **Probabilistic cloning and anticloning (with probability `p`)**

## Results

### Example Graphs

Below are the example graphs generated during the simulation. Each graph represents the result after a specified number of iterations.

#### Option 1: Cloning Every Vertex
![Graph Cloning](images/cloning_step_1.png)

**Description**: The graph starts with two connected vertices. Each new vertex added is a clone of an existing vertex, leading to a dense, connected structure.

#### Option 2: Anticloning Every Vertex
![Graph Anticlone](images/anticlone_step_1.png)

**Description**: In this option, new vertices are connected to all vertices that are not neighbors of the original vertex. This results in a more sparsely connected graph.

#### Option 4: Probabilistic Cloning and Anticloning
![Graph Probabilistic](images/probabilistic_step_1.png)

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
- The probabilistic approach introduces variability, which can lead to graphs with more varied spectral gaps.
- The IIM model's ability to model social networks and clustering behavior was evident from the graph structure and spectral properties.

### Next Steps

Further experiments can be conducted by varying the parameters, such as the probability `p`, to investigate its impact on the overall graph structure and spectral gap.

---

### Notes:
- Replace `XX.XX` with the actual average spectral gap you calculated.
- Make sure the images you want to include are placed inside the `images/` folder.

### Step 4: Verify the Images on GitHub
After pushing the images and the markdown file, verify on GitHub that:

1. The `images/` folder is correctly uploaded with all the images.
2. The markdown file renders the images correctly when viewed on GitHub.

By following these steps, you should be able to successfully upload and reference images from your `images/` folder in the markdown file.
