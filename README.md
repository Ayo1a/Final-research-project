![](https://github.com/Ayo1a/Final-research-project/blob/main/images/Cover_forReadMe.jpg)
# Iterative Independent Model (IIM) 

This repository contains the implementation of the **Iterative Independent Model (IIM)** and a proposal extended model, which is based on the **Barabási–Albert model**. 

**The project is a research project and its primary objective is to modeling evaluate the accuracy of the research article "[Iterative Independent Model: arXiv:2209.01093](https://arxiv.org/pdf/2209.01093)" in claiming that the IIM effectively represents real-world networks, such as social networks, internet traffic, and biological systems and thereby promoting their research. To achieve this, we created a Python model of the IIM and analyzed the results.**

IIM graphs are a kind of **complex network**. From the understanding that complex networks effectively represent social networks in the real world, this article and research project were born. A significant part of this project involved developing a deep mathematical understanding of graphs and their attributes, such as the spectral gap, Laplacian matrix, diameter, and more. These concepts were studied to understand their effects on graph structure and behavior to analyze the model results effectively.

Additionally, the project includes a proposal for a ![new hybrid model](https://github.com/Ayo1a/Final-research-project/blob/main/Proposal%20to%20hybrid%20Barabashi%20model.md), the **Barabashi Model**, which combines features of the IIM and the Barabási–Albert model to provide deeper insights into network behaviors.

#### Refer to the ![Files Structure.md](https://github.com/Ayo1a/Final-research-project/blob/main/Files%20Structure.md) file for better navigation throughout the project

---

## Reflection on the Project

Working on this project has been an incredibly rewarding and enjoyable experience. It was fascinating to explore the nuances of graph theory and observe the dynamic behaviors of different graph generation methods. Each step, from implementing the models to visualizing their evolution and analyzing their spectral properties, deepened my mathematical understanding strengthened my appreciation for the graph world, and expanded my knowledge of different Python graph folders, providing a very deep understanding of the subject. This project not only challenged me technically but also inspired me to delve further into the beauty and complexity of mathematical models in graph structures.

**I would like to express my sincere gratitude to my project supervisor, Dr. Zur Luria from Azrieli College of Engineering, for his unwavering belief in me throughout the project and for being an inspiring source of knowledge.**

**Belief is a highly expander graph** 🌟

## Project Overview

### Iterative Independent Model (IIM)
The Iterative Independent Model (IIM) is a deterministic graph generation model designed to simulate the structure and evolution of real-world networks, such as social networks, internet traffic, and biological systems. It generalizes earlier models by incorporating **cloning** and **anticloning** processes to mimic transitive and anti-transitive behaviors observed in social dynamics:
- **Cloning**: Reflects the principle of "the friend of my friend is my friend."
- **Anticloning**: Captures the behavior of "the enemy of my enemy is my friend."
- **To get an initial look at the graphs generated in this study** ![Click here[]()](https://github.com/Ayo1a/Final-research-project/blob/main/Graph%20Generation%20Process.md)

In this model, each node in the graph independently undergoes either cloning or anticloning during each iterative step. Despite its deterministic nature, the model exhibits intrinsic structural properties, making it versatile for applications regardless of randomness.

Key properties of IIM graphs include:
- **Spectral Gap Bounded Away from Zero**: Indicative of clustering and robustness in the network and will be the key feature for common behavior with social networks.
- **Bounded Graph Diameter**: Suggests efficient connectivity, a hallmark of social networks.
- **Dominance and Clique Numbers**: Further characterize the clustering and hierarchical properties of the graph.
- **Universal Induced Subgraphs**: Any fixed graph \(F\) will eventually appear as an induced subgraph after sufficient iterations.

- ### Computational Aspects of the IIM Properties

The Iterative Independent Model (IIM) exhibits several structural properties that provide insights into network behavior. However, analyzing these properties involves a mix of computational challenges, with some being efficiently solvable and others classified as NP-complete.

### **Computational Complexity of IIM Properties**

The Iterative Independent Model (IIM) exhibits several structural properties that provide insights into network behavior. However, analyzing these properties involves a mix of computational challenges. While some properties are computationally tractable, others fall under NP-complete problems, making them computationally infeasible.

It is essential to understand that due to computational limitations, it is not possible to test all parameters comprehensively. Therefore the analysis in the project focuses on key characteristics that can be efficiently calculated.


#### **Spectral Gap**
- **Available to Check**: A key feature in our project through which we will verify the results of the article. The spectral gap, the difference between the eigenvalues ​​at the edges of the graph's Laplacian, can be computed efficiently using numerical linear algebra techniques. Tools like `numpy` or specialized libraries can be used to compute eigenvalues in polynomial time for graphs of practical size.

#### **Graph Diameter**
- **Available to Check**: The graph diameter, the longest shortest path in the network, can be computed using all-pairs shortest paths algorithms such as Floyd-Warshall (O(\|V\|³)) or more efficient algorithms like Dijkstra's (O(\|E\| + \|V\| log \|V\|)) for sparse graphs. While computationally intensive for very large graphs, it is tractable for moderately sized networks.

#### **Dominance Number**
- **NP-Complete**: Determining the dominance number, which is the size of the smallest set of nodes such that every node in the graph is either in the set or adjacent to a node in the set, is NP-complete. Approximations or heuristics (e.g., greedy algorithms) are often used to find solutions for practical applications.

#### **Clique Number**
- **NP-Complete**: The clique number, the size of the largest complete subgraph, is also NP-complete to determine. Exact solutions require exhaustive search methods like the Bron-Kerbosch algorithm. Approximation techniques or heuristics can provide usable insights in reasonable time.

#### **Universal Induced Subgraphs**
- **Not Tractable in General**: Determining whether a graph contains a specific induced subgraph (subgraph isomorphism) is NP-complete. For small subgraphs, this can sometimes be checked efficiently using tailored algorithms or pattern-matching libraries.

### Summary of Computational Properties
| **Property**               | **Complexity**       | **Comments**                                                                 |
|----------------------------|---------------------|-----------------------------------------------------------------------------|
| **Spectral Gap**            | Polynomial Time     | Efficiently computed via numerical linear algebra.                          |
| **Graph Diameter**          | Polynomial Time     | Computed using shortest-path algorithms; feasible for moderately sized graphs. |
| **Dominance Number**        | NP-Complete         | Approximation or heuristic methods are needed for large graphs.             |
| **Clique Number**           | NP-Complete         | Exact methods are infeasible for large graphs; approximations often used.   |
| **Universal Induced Subgraphs** | NP-Complete         | Determining specific induced subgraphs is intractable for large networks.    |


The primary goal of this project is to evaluate whether the IIM accurately represents social networks by analyzing the **spectral gap** and **diameter**, and comparing these properties to real-world network characteristics. To conduct this analysis, we first compute the Laplacian matrix of the graph. This matrix is derived using the rank matrix D, adjacency matrix A, and unit matrix I, following the formula: ![](https://github.com/Ayo1a/Final-research-project/blob/main/images/Laplacian.PNG) when the range of eigenvalues ​​of the matrix is ![](https://github.com/Ayo1a/Final-research-project/blob/main/images/range.PNG )​​and and the spectral gap is calculated using the following approach: ![](https://github.com/Ayo1a/Final-research-project/blob/main/images/spectral%20gap.PNG)

### Hybrid Barabashi Model
![link to page proposal](https://github.com/Ayo1a/Final-research-project/blob/main/Proposal%20to%20hybrid%20Barabashi%20model.md)
As an extension to the IIM, the **Barabashi Model** introduces a hybrid approach by integrating principles of the IIM with the **Barabási–Albert model**. Its main features include:
- **General Barabási's Rank distribution**, which ensures a heavy-tailed degree distribution, characteristic of many real-world networks.
- The **Small World phenomenon**, where common friends increase the likelihood of new connections, enhancing network clustering.


---

## Implementation Details

### Libraries Used
The project uses the following Python libraries:
- `networkx`: For graph creation, manipulation, and analysis.
- `matplotlib.pyplot`: For visualizing graphs and their properties.
- `numpy`: For numerical computations and matrix operations.
- `seaborn`: For data visualization enhancements.
- `random`: For generating stochastic elements in the models.

### Refer to the ![Files Structure.md](https://github.com/Ayo1a/Final-research-project/blob/main/Files%20Structure.md) file for better navigation throughout the project

