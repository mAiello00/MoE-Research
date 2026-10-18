### Link
- https://arxiv.org/pdf/2603.06350

### Domain
- Expert Serving

### The Problem
- expert load imbalance is a fundamental challenge in distributed serving (some experts become popular and receive the majority of the load)
- this imbalance leads to the *expert straggler* problem (increases inference latency and serving costs)

#### The Specific Problem To Be Solved
- Mitigate expert load imbalance
- **achieve expert load balance without generation performance loss** (requires fine-grained, elastic, and accurate expert scaling in MoE serving)

#### Why is it Important?
- improvae function locality
- improve GPU utilization
- improve cross-expert load balance

#### Limitations of Existing Approaches that Motivated Their Work
- 

#### The Proposed Solution
- optimized scaling and placement strategies
- estimate incoming expert load distribution and proactively identify stragglers
- serverless solution
- predictors identify straggler experts
- **dynamically scale expert replicas to eliminate stragglers and balance workloads**

#### Key Findings and Results
- 

#### Assumptions
- 

#### Limitations
- 

#### Relevance to My Work
- 