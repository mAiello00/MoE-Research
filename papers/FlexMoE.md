https://arxiv.org/pdf/2304.03946

### Domain
- Training
- Expert Routing Imbalance
- **Distributed Training System**

### The Problem

#### The Specific Problem To Be Solved
- addresses dynamic imbalance of experts during large-scale MoE training
- addresses inefficiency caused by dynami data flow
- aim to overcome routing imbalance and fuctuation by dynamic expert management and device placement

#### Why is it Important?
- during routing, the input tokens show highly uneven preference for experts, and routing results keep varying over training
- **this workload imbalance can lead to significant efficiency slowdown and severe resources under-utilization**

#### Limitations of Existing Approaches that Motivated Their Work
- most existing approaches use an auxiliary load balancing loss at each MoE layer to enforce balanced routing
- penalty weight also typically added to control system efficiency (workload balance) and statistical efficiency (model quality)
- another technique is dropping tokens above a certain expery capacity
- **can only mitigate workload impalance rather than fundamentally guarantee workload balance**

#### The Proposed Solution
- fine-grained replicated expert parallelism
- selects heavy experts, duplicates them over multiple devices, and spreads the input tokens across the replicas
- precisely models the execution procedure of the MoE layer to estimate the costs that determine the concrete expert replication scheme
- design an adaptive expert management mechanism to adaptively adjust the expert-to-device mapping and the assignment of tokens during training

#### Key Findings and Results
- found that MoE model exhibit routing fluctuation during the training process (expert popularity fluxuates throughout training)
- 

#### Assumptions and Limitaitons
- tmp