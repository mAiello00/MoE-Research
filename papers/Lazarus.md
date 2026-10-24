### Link
- https://arxiv.org/pdf/2407.04656

### Domain
- Elasticity
- Expert Placement
- Fault Tolerance

### The Problem
- cost of failures while training large models is significant
- likeliood and frequency of failures increases when training large models

#### The Specific Problem To Be Solved
- existing solutions for fault tolerant training either lack elasticity or rely on building resiliency into pipeline parallelism, which can't be applied to MoE

#### Why is it Important?
- high cost of failure during training
- all GPUs idle during a failure until nodes replaced

#### Limitations of Existing Approaches that Motivated Their Work
- 

#### The Proposed Solution
- adaptively allocate expert recplicas to address imbalance in expert workloads
- optimal expert placement algorithm to maximuze probability of recovery after failure 
- **adaptive expert placement and flexible token dispatch**
- upon failure, quickly reconfigure the training job and utilize all remaining GPUs
- **allocate expert replicas based on the dynamic expert load distribution**
- fault-tolerant expert placement strategy helps recvoery probability
- assigns more replicas and more GPUs to heavily loaded experts
  **upon node failure, the controller will recalculate the expert placement plan using the remaining nodes and minimizes the number of replicas migrated**
- token dispatcher balances the number of tokens sent to each GPU

#### Key Findings and Results
- 

#### Assumptions
- 

#### Limitations
- 

#### Relevance to My Work
- 