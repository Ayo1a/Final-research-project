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


### Spectral Gap Analysis

We ran the simulation 20 times and calculated the spectral gap for each run. The average spectral gap is calculated as follows:

- **Average Spectral Gap**: Average spectral gap over 15 runs: 0.7926149898118253

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


