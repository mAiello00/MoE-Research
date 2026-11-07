### Link
- 

### Domain
- 

### The Problem
- LUMEN targets three goals:
  - Fast recovery
  - low steady-state overhead 
  - scalability

#### The Specific Problem To Be Solved
- looking for a more efficient mechanism for failure recovery in MoE systems
- Stop-and-Restart and Fixed-Checkpointing are not efficient
- failures still lead to massive computational waste/inefficiencies

#### Why is it Important?
- 

#### Limitations of Existing Approaches that Motivated Their Work
- built upon SGLang LLM serving system

#### The Proposed Solution
- Three coordinated mechanisms
  - load-aware KV cache checkpointing
  - locaity-aware recovery scheduling
  - speculation-assisted progressive recovery
- **LUMEN augments the token gateway to retain the *token history* of every in-flight request**
- Introduces a centralized controller which maintains a *load table* of per-worker queuing and capacity signals and a *placement table* that maps each request to its checkpoint holder
  - both tables drive checkpoint placement in steady state and a request dispatch when failure occurs
- upon failure detection by the gateway, the controller initially routes interrupted requests to their checkpoint holders to maximize KV usgage

#### Key Findings and Results
- 

#### Assumptions
- **Assumes both the gateway and controller remain operational during recovery**

#### Limitations
- 

#### Relevance to My Work
- **Can potentially look into MULTIPLE CHECKPOINT REPLICATION**
  - currently if both the worker and checkpoint holder fail we have a heavy recompute process
- Can potentially look into fault tolerance when the gateway and controller fail as well