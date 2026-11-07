### Link
- https://arxiv.org/pdf/2509.17863

### Domain
- Elasticity, Independent Services

### The Problem
- **Can expert-level service disaggregation provide fine-grained scaling and fault resilience without substantially sacrificing normal serving performance?**

#### The Specific Problem To Be Solved
- 

#### Why is it Important?
- 

#### Limitations of Existing Approaches that Motivated Their Work
- Course scaling granularities (poor elasticity)
- Collective communication (All-to-All Communication)
  - brittle, meaning that a failure often results in the entire group restarting
- Worload imbalance

#### The Proposed Solution
- **Disaggregates MoE experts into independently scalable services and explicitly addresses fault tolerance**
  - Disaggregate experts into independent services
- Decouple MoE layer from the rest of the model
- **Treat the pool of experts as dynamically accessible and independent services** 

#### Key Findings and Results
- 

#### Assumptions
- 

#### Limitations
- 

#### Relevance to My Work
- 