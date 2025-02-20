# Cold start
|Nickname  |Paper |Cite   |General Idea   |
|:---:      |   :----------- |:---:  |:---:  |
| Catalyzer | [Catalyzer: Sub-millisecond Startup for Serverless Computing with Initialization-less Booting](https://dl.acm.org/doi/10.1145/3373376.3378512) | ASPLOS 20' |  |
|  |  |  |  |

# Runtime 
|Nickname  |Paper |Cite   |General Idea   |
|:---:      |   :--------- |:---:  |:---:  |
| FaaSMem | [FaaSMem: Improving Memory Efficiency of Serverless Computing with Memory Pool Architecture](https://dl.acm.org/doi/10.1145/3620666.3651355) | ASPLOS 24' |  |
|  |  |  |  |

# Fault tolerance
|Nickname  |Paper |Cite   |General Idea   |
|:---:      |   :----- |:---:  |:---:  |
| Code review | [Automated Verification of Idempotence for Stateful Serverless Applications](https://www.usenix.org/conference/osdi23/presentation/ding)  | OSDI 23' | Only Idempotent code can safely retry. Thay build an automatic tool to review serverless function codes to find whether meet Idempotent. |
| Halfmoon | [Halfmoon: Log-Optimal Fault-Tolerant Stateful Serverless Computing](https://dl.acm.org/doi/10.1145/3600006.3613154)  | SOSP 23' | Halfmoon provides two logging protocols that enforce exactly-once semantics while providing log-free reads and writes, respectively. |
| Boki | [Boki: Stateful Serverless Computing with Shared Logs](https://dl.acm.org/doi/10.1145/3477132.3483541)  | SOSP 21' | Use shared log to enable stateful serverless applications to manage their state with durability, consistency, and fault tolerance. |
| Beldi | [Fault-tolerant and transactional stateful serverless workflows](https://www.usenix.org/conference/osdi20/presentation/zhang-haoran)  | OSDI 20' | Extending the log-based fault-tolerant approach in Olive (OSDI 2016). |
| AFT | [A fault-tolerance shim for serverless computing](https://dl.acm.org/doi/10.1145/3342195.3387535)  | EuroSys 20' | AFT offers transactional key-value store API. |
| Olive | [Realizing the Fault-Tolerance Promise of Cloud Storage Using Locks with Intent](https://www.usenix.org/conference/osdi16/technical-sessions/presentation/setty) | OSDI 16' |  |

# Communication
|Nickname  |Paper |Cite   |General Idea   |
|:---:      |  :--- |:---:  |:---:  |
| SPRIGHT | [SPRIGHT: Extracting the Server from Serverless Computing! High-performance eBPF-based Event-driven, Shared-memory Processing](https://dl.acm.org/doi/10.1145/3544216.3544259) | SIGCOMM 22' |  |
|  |  |  |  |

# Scheduling
|Nickname  |Paper |Cite   |General Idea   |
|:---:      |   :----------- |:---:  |:---:  |
| Alps | [Alps: An Adaptive Learning, Priority OS Scheduler for Serverless Function](https://www.usenix.org/conference/atc24/presentation/fu) | ATC 24' |  |
|  |  |  |  |