# Cold start
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :----------- |:---:  |:---:  |
| OSDI 23' | Mitos | [No Provisioned Concurrency: Fast RDMA-codesigned Remote Fork for Serverless Computing]() | Remote docker fork. |
| SOSP24' | SigmaOS | [Unifying serverless and microservice tasks with SigmaOS](https://dl.acm.org/doi/10.1145/3694715.3695947) |  |
| ASPLOS 20' | Catalyzer | [Catalyzer: Sub-millisecond Startup for Serverless Computing with Initialization-less Booting](https://dl.acm.org/doi/10.1145/3373376.3378512) |  |
| ATC 22' | RunD | [RunD: A Lightweight Secure Container Runtime for High-density Deployment and High-concurrency Startup in Serverless Computing](https://www.usenix.org/conference/atc22/presentation/li-zijun-rund) |  |
| ATC 18' | SOCK | [SOCK: Rapid Task Provisioning with Serverless-Optimized Containers](https://www.usenix.org/conference/atc18/presentation/oakes) |  |

# Runtime 
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :--------- |:---:  |:---:  |
| ASPLOS 24' | FaaSMem | [FaaSMem: Improving Memory Efficiency of Serverless Computing with Memory Pool Architecture](https://dl.acm.org/doi/10.1145/3620666.3651355) |  |
| ISCA 22' | Jukebox | [Lukewarm serverless functions: characterization and optimization](https://dl.acm.org/doi/10.1145/3470496.3527390) | L2 cache prefetch |

# Fault tolerance
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :----- |:---:  |:---:  |
| OSDI 23' | Code review | [Automated Verification of Idempotence for Stateful Serverless Applications](https://www.usenix.org/conference/osdi23/presentation/ding)  | Only Idempotent code can safely retry. Thay build an automatic tool to review serverless function codes to find whether meet Idempotent. |
| SOSP 23' | Halfmoon | [Halfmoon: Log-Optimal Fault-Tolerant Stateful Serverless Computing](https://dl.acm.org/doi/10.1145/3600006.3613154)  | Halfmoon provides two logging protocols that enforce exactly-once semantics while providing log-free reads and writes, respectively. |
| SOSP 21' | Boki | [Boki: Stateful Serverless Computing with Shared Logs](https://dl.acm.org/doi/10.1145/3477132.3483541)  | Use shared log to enable stateful serverless applications to manage their state with durability, consistency, and fault tolerance. |
| OSDI 20' | Beldi | [Fault-tolerant and transactional stateful serverless workflows](https://www.usenix.org/conference/osdi20/presentation/zhang-haoran)  | Extending the log-based fault-tolerant approach in Olive (OSDI 2016). |
| EuroSys 20' | AFT | [A fault-tolerance shim for serverless computing](https://dl.acm.org/doi/10.1145/3342195.3387535) | AFT offers transactional key-value store API. |
| OSDI 16' | Olive | [Realizing the Fault-Tolerance Promise of Cloud Storage Using Locks with Intent](https://www.usenix.org/conference/osdi16/technical-sessions/presentation/setty) |  |

# Communication
| Cite | Nickname  | Paper |General Idea |
|:---:      |  :--- |:---:  |:---:  |
| SIGCOMM 22' | SPRIGHT | [SPRIGHT: Extracting the Server from Serverless Computing! High-performance eBPF-based Event-driven, Shared-memory Processing](https://dl.acm.org/doi/10.1145/3544216.3544259) |  |
| EuroSys 24' | RMMAP | [Serialization/Deserialization-free State Transfer in Serverless Workflows](https://dl.acm.org/doi/10.1145/3627703.3629568) | RDMA |
|  |  |  |  |
|  |  |  |  |

# Scheduling
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :----------- |:---:  |:---:  |
| ATC 24' | Alps | [Alps: An Adaptive Learning, Priority OS Scheduler for Serverless Function](https://www.usenix.org/conference/atc24/presentation/fu) |  |
|  |  |  |  |