### Link
- https://arxiv.org/pdf/2510.02613

### Domain
- Elasticity and Autoscaling

### The Problem
- 

#### The Specific Problem To Be Solved
- zero downtime verticla scaling in production
- elastically serve large scale MoE models 

#### Why is it Important?
- classical scaling approaches are highly inefficient
- horizontal scaling provisions requires provisioning fixed quantities of accelerators
- so small traffic increases can result in massive overprovisions of compute

#### Limitations of Existing Approaches that Motivated Their Work
- 

#### The Proposed Solution
- 

#### Key Findings and Results
- 

#### Assumptions
- 

#### Limitations
- the Tensor Parallelism (TP) degree needs to be fixed
- intake of new requests is paused while preparing the new instance

#### Relevance to My Work
- 