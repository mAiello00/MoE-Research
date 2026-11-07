### Link
- https://arxiv.org/html/2512.13525

### Domain
- 

### The Problem
- 

#### The Specific Problem To Be Solved
- Efficient MoE inferencing

#### Why is it Important?
- 

#### Limitations of Existing Approaches that Motivated Their Work
- 

#### The Proposed Solution
- Three key principles:
  - Disaggregates attention and MoE layers onto separate GPU worker pools
  - Introduces an activation scheduler to balance activated experts across layers
  - **SLO-Aware resource scaling**

#### Key Findings and Results
- 

#### Assumptions
- 

#### Limitations
- 

#### Relevance to My Work
- 