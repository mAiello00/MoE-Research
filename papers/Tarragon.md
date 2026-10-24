### Link
- https://arxiv.org/pdf/2601.01310

### Domain
- Failure Resilience, Fault Tolerance

### The Problem
- Existing solutions have poor failure resilience
  - single worker failure triggerse course grained service-wide restart
- **Can faults in individual MoE workers be isolated and recovered without restarting the entire inference pipeline?**

#### The Specific Problem To Be Solved
- Confines failure's impact to individual workers while making forward progress

#### Why is it Important?
- Single worker failure triggers a course grained recovery, which is expernsive and time consuming

#### Limitations of Existing Approaches that Motivated Their Work
- 

#### The Proposed Solution
- Exploit separation between expert and attention computation
- Treats Attention Workers (AWs) and Expert Workers (EWs) as distinct failure domains
- Reconfiurable datapath to mask failures by rerouting requests to healthy workers

#### Key Findings and Results
- 

#### Assumptions
- 

#### Limitations
- 

#### Relevance to My Work
- Fault tolerance - reroute requests to healthy workers upon failure