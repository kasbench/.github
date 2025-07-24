# KASBench: A Benchmark for Kubernetes Autoscaling
<img src="../images/globeco-logo.png" alt="Logo" width="100"> KASBench is a new benchmark under development for Kubernetes Autoscaling. GlobeCo is a suite of applications designed to subject autoscalers to a variety of real-world conditions including long call chains, heterogeneous languages, multiple types of stateful data storage, synchronous and asynchronous calling patterns, LLM inferencing, CPU-intensive service, network-intensive services, and disk IO-intensive services.



## Portfolio Management

Potfolio management is one application in the GlobeCo suite.  It is a simulated portfolio management application, including order generation, order management, trading, and execution. 

<img src="../images/GlobeCo Portfolio Management and Trading.png">


### Status

| Microservice              | Language         | Coding | Integration | Instrumentation | Notes                                            |
| ------------------------- | ---------------- | ------ | ----------- | --------------- | ------------------------------------------------ |
| [Portfolio Service](https://github.com/kasbench/globeco-portfolio-service)         | Python/MongoDB   | Done   |    Done         |  Done               | CPU-light                                        |
| [Portfolio Optimizer](https://github.com/kasbench/globeco-portfolio-optimizer)       | Go     |        |             |                 | CPU-intensive Golang. gRPC                            |
| [Portfolio Accounting Service](https://github.com/kasbench/globeco-portfolio-accounting-service) | Go/Postgres or YugabyteDB | Done | Done| Done |CPU and Database-intensive, batch CLI                           |
| [Order Generation Service](https://github.com/kasbench/globeco-order-generation-service)  | Python/MongoDB           | Done       | Done            |      Done          | CPU-intensive Python                             |
| [Order Service](https://github.com/kasbench/globeco-order-service)             | Java/PostgreSQL  | Done   |   Done          |    Done             | For microservice chain depth                     |
| [Trade Service](https://github.com/kasbench/globeco-trade-service)             | Java/PostgreSQL  | Done   |     Done        |         Done        | For microservice chain depth                     |
| [Execution Service](https://github.com/kasbench/globeco-execution-service)         | Java/PostgreSQL  | Done       |   Done          |   Done              | Asynchronous (producer)                          |
| [FIX Engine](https://github.com/kasbench/globeco-fix-engine)               | Go               |  Done      |   Done          |     Done            | Stochastic, asynchronous (consumer and producer) |
| [Real-Time Pricing Service](https://github.com/kasbench/globeco-pricing-service) | Java/PostgreSQL  | Done   |      Done       |      Done           | Stochastic                                       |
| [Security Service](https://github.com/kasbench/globeco-security-service)          | Python/MongoDB   | Done   |   Done          |   Done              | For microservice chain depth                     |
| [Allocation Service](https://github.com/kasbench/globeco-allocation-service)        | Go               |  Done      | Done           |      Done           | For microservice chain depth                     |
| [Confirmation Service](https://github.com/kasbench/globeco-confirmation-service)      | Go               | Done      |  Done            |          Done       | Asynchronous (consumer)                          |                          |
| [Company Portal](https://github.com/kasbench/globeco-portfolio-management-portal)          | TypeScript/React |  Done      |  Done           |     Done            | UI                                               |
| [Benchmark Coordinator](https://github.com/kasbench/globeco-benchmark-coordinator)     | Python               | In Progress       |             |                 |   Includes load runner                           |
| [Debug Tools](https://github.com/kasbench/globeco-debug-tools) | Docker | Done| Done | N/A | Bastion pod for debugging
| [Development Resources](https://github.com/kasbench/globeco-development-resources) | N/A | N/A | N/A | N/A | Guides, rules, and prompts |
| [Observability Configuration](https://github.com/kasbench/globeco-observability) |N/A| Done | N/A | N/A | Configuration for Prometheus, Jaeger, Grafana and the Open\-Telemetry Collector|
---
