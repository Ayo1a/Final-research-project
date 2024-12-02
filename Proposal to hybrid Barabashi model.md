## Proposal to a hybrid model that mixes the Barabási–Albert model 

The idea of proposing another model is to exploit the capabilities of IIM graphs to be more similar to social networks and to gain additional characteristics. 
After researching the properties of social networks, we decided to propose a model that takes inspiration from the Barabási–Albert model.

Based on the Barabási model, a vertex added to the graph will be prioritized for connection to a vertex with a high degree. 
As a result, a distinct feature of social networks called a **heavy tail** is obtained. That is, we will have a lot of vertices with a low degree and a few vertices with 
an extremely high degree. 
- This is socially reasonable since this can be likened to psychological behavior.
For example, suppose a person arrives at a new place. The likelihood that they will connect with a popular person is high, just like a child arriving at a new class.

**Example of a graph with heavy tail** 
 - We can see a lot of vertices with a low degree and a few vertices with 
an extremely high degree. 

![](https://github.com/Ayo1a/Final-research-project/blob/main/images/heavy_tail.png)

Alongside this, the IIM model also provides an example of social behavior of **small-world** feature with the **clone operation** and reflects the principle of "the friend of my friend is my friend". 
The proposed model generates a graph through clone operations, but the added vertices choose a vertex with a high degree as a priority.

### Expected Outcomes
The proposed model claims to contain the **heavy-tail** feature of the Barabási model, which represents a resemblance to a social network. 
Additionally, it is expected to exhibit the **small-world** feature from the IIM model (i.e., if we have many friends in common, we are highly likely to know each other), 
which the Barabási model does not have. This small-world feature is derived from the IIM model’s graph structure.

By hybridizing both models and leveraging their features, we expect the following results:

1. **Large clustering coefficient**
2. **Spectral gap bounded away from zero** 
3. **Small diameter** — Even though the spectral gap is not very small, in the worst case, where a vertex is at the end of the heavy tail and another vertex is at the head, the vertex at the tail is connected to another vertex within the network. From there, a short path exists to reach the vertex at the head.

This model aims to combine the best aspects of both the Barabási and IIM models, reflecting key properties found in real-world social networks.
