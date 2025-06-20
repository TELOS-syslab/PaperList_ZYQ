# Serverless的开端
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :----------- |:---:  |:---:  |
| arxiv | Berkeley View | [Cloud Programming Simplified: A Berkeley View on Serverless Computing](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2019/EECS-2019-3.pdf) | Remote docker fork. |

# Cold start
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :----------- |:---:  |:---:  |
| Eurosys 25'| Alloystack | [AlloyStack: A Library Operating System for Serverless Workflow Applications](https://dl.acm.org/doi/10.1145/3689031.3717490) | The LibOS work |
| OSDI 23' | Mitos | [No Provisioned Concurrency: Fast RDMA-codesigned Remote Fork for Serverless Computing]() | Remote docker fork. |
| SOSP24' | SigmaOS | [Unifying serverless and microservice tasks with SigmaOS](https://dl.acm.org/doi/10.1145/3694715.3695947) |  |
| ASPLOS 20' | Catalyzer | [Catalyzer: Sub-millisecond Startup for Serverless Computing with Initialization-less Booting](https://dl.acm.org/doi/10.1145/3373376.3378512) |  |
| ATC 22' | RunD | [RunD: A Lightweight Secure Container Runtime for High-density Deployment and High-concurrency Startup in Serverless Computing](https://www.usenix.org/conference/atc22/presentation/li-zijun-rund) |  |
| ATC 20' | Faaslets | [Faasm: Lightweight Isolation for Efficient Stateful Serverless Computing](https://www.usenix.org/conference/atc20/presentation/shillaker) | Use WebAssembly as container |
| ATC 18' | SOCK | [SOCK: Rapid Task Provisioning with Serverless-Optimized Containers](https://www.usenix.org/conference/atc18/presentation/oakes) |  |
| Eurosys 20' | SEUSS | [SEUSS: skip redundant paths to make serverless fast](https://dl.acm.org/doi/10.1145/3342195.3392698) | The snapshot mechanism for unikernel serverless runtime. Their key insight is that shapshot reduced the preparation for environment and runtime init which enables optimizations to squash redundancy. |
| ASPLOS 21' | REAP | [Benchmarking, analysis, and optimization of serverless function snapshots](https://dl.acm.org/doi/abs/10.1145/3445814.3446714) | Using snapshot to optimize cold start |
| OSDI 24' | Sabre | [Sabre: Hardware-Accelerated Snapshot Compression for Serverless MicroVMs](https://www.usenix.org/conference/osdi24/presentation/lazarev) | Using Intel to accelerate building and loading snapshot |
| ASPLOS 21' | FaasCache | [FaasCache: keeping serverless computing alive with greedy-dual caching](https://dl.acm.org/doi/10.1145/3445814.3446757) | Adding cache replacment and prefetch mechanism to serverless keep-alive. Avoid some cold starts |
| ASPLOS 23' | AQUATOPE | [AQUATOPE: QoS-and-Uncertainty-Aware Resource Management for Multi-stage Serverless Workflows](https://dl.acm.org/doi/10.1145/3567955.3567960) | Using reinforcement learning to prewarm serverless functions |
| ASPLOS 24' | RainbowCake | [RainbowCake: Mitigating Cold-starts in Serverless with Layer-wise Container Caching and Sharing](https://dl.acm.org/doi/10.1145/3617232.3624871) | Container caching and sharing. |

# Runtime 
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :--------- |:---:  |:---:  |
| ASPLOS 24' | FaaSMem | [FaaSMem: Improving Memory Efficiency of Serverless Computing with Memory Pool Architecture](https://dl.acm.org/doi/10.1145/3620666.3651355) |  |
| SOSP 23' | XFaaS | [XFaaS: Hyperscale and Low Cost Serverless Functions at Meta](https://dl.acm.org/doi/10.1145/3600006.3613155) | Meta's serverless system framework |
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
| SIGCOMM 22' | SPRIGHT | [SPRIGHT: Extracting the Server from Serverless Computing! High-performance eBPF-based Event-driven, Shared-memory Processing](https://dl.acm.org/doi/10.1145/3544216.3544259) | Download Kubernet communication service to eBPF |
| EuroSys 24' | RMMAP | [Serialization/Deserialization-free State Transfer in Serverless Workflows](https://dl.acm.org/doi/10.1145/3627703.3629568) | RDMA |
| ASPLOS 21' | Nightcore | [Nightcore: efficient and scalable serverless computing for latency-sensitive, interactive microservices](https://dl.acm.org/doi/10.1145/3445814.3446701) | A runtime can run multi-serverless-functions in the same VM making communication faster |
| ATC 20' | Faaslets | [Faasm: Lightweight Isolation for Efficient Stateful Serverless Computing](https://www.usenix.org/conference/atc20/presentation/shillaker) | Shared memory |
|  |  |  |  |

# Resorce Scheduling
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :----------- |:---:  |:---:  |
| ATC 24' | Alps | [Alps: An Adaptive Learning, Priority OS Scheduler for Serverless Function](https://www.usenix.org/conference/atc24/presentation/fu) |  |
| Eurosys 23' |  Bayesian | [With Great Freedom Comes Great Opportunity: Rethinking Resource Allocation for Serverless Functions](https://dl.acm.org/doi/abs/10.1145/3552326.3567506) |  |
| SOSP 21' | Harvest | [Faster and Cheaper Serverless Computing on Harvested Resources](https://dl.acm.org/doi/10.1145/3477132.3483580) | Using Harvest VM to run serverless functions |
| HPCA 20'| CLITE | [CLITE: Efficient and QoS-Aware Co-location of Multiple Latency-Critical Jobs for Warehouse Scale Computers](https://ieeexplore.ieee.org/abstract/document/9065583)| |


# End to end
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :----------- |:---:  |:---:  |
|  | FaaSLight | [FaaSLight: General Application-level Cold-start Latency Optimization for Function-as-a-Service in Serverless Computing](https://dl.acm.org/doi/abs/10.1145/3585007?mi=kthjst&af=R&AllField=PubIdSortField%3A%281049-331X%29&content=standard&expand=dl&sortBy=EpubDate_desc&target=advanced) | Automatic detect and remove redundant libraries and code in your application to improve end-to-end latency. |
|  |  |  |  |

# Optimization for Chaining
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :----------- |:---:  |:---:  |
| Eurosys 23' | Palette | [Palette Load Balancing: Locality Hints for Serverless Functions](https://dl.acm.org/doi/abs/10.1145/3552326.3567496) | Using coloring to make serverless start have more locality reuse. |
| Socc 20' | Wukong |  | Wukong modifies the Dask scheduler to find chains of tasks that can be executed on the same node, and sends these sections of the graph to the same function instance. |
| ATC 21' | SONIC | [SONIC: Application-aware data passing for chained serverless applications.](https://www.usenix.org/conference/atc21/presentation/mahgoub) | SONIC selects how to best transfer data among stages of a DAG, and does data-aware function placement, based on its knowledge of the DAG. |
|  |  |  |  |

# Storage
| Cite | Nickname  | Paper |General Idea |
|:---:      |   :----------- |:---:  |:---:  |
| OSDI 18' | Pocket | [Pocket: Elastic Ephemeral Storage for Serverless Analytics](https://www.usenix.org/conference/osdi18/presentation/klimovic) |  |
| PODS 21' | PolarDB | [PolarDB Serverless: A Cloud Native Database for Disaggregated Data Centers](https://dl.acm.org/doi/10.1145/3448016.3457560) |  |
