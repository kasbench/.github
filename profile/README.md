# KASBench: A Benchmark for Kubernetes Autoscaling

<img src="../images/globeco-logo.png" alt="Logo" width="100">
KASBench is a new benchmark under development for Kubernetes Autoscaling. GlobeCo is a suite of applications designed to subject autoscalers to a variety of real-world conditions including long call chains, heterogeneous languages, multiple types of stateful data storage, synchronous and asynchronous calling patterns, LLM inferencing, CPU-intensive service, network-intensive services, and disk IO-intensive services.



## Portfolio Management

Potfolio management is one application in the GlobeCo suite.  It is a simulated portfolio management application, including order generation, order management, trading, and execution. 

<img src="../images/GlobeCo Portfolio Management and Trading.png">


### Status

| Microservice              | Language         | Coding | Integration | Instrumentation | Notes                                            |
| ------------------------- | ---------------- | ------ | ----------- | --------------- | ------------------------------------------------ |
| [Portfolio Service](https://github.com/kasbench/globeco-portfolio-service)         | Python/MongoDB   | Done   |             |                 | CPU-light                                        |
| Portfolio Optimizer       | Go or Python     |        |             |                 | CPU-intensive Golang                             |
| Balance Service           | Java/Vitess      |        |             |                 | Database-intensive                               |
| Order Generation Service  | Python           |        |             |                 | CPU-intensive Python                             |
| [Order Service](https://github.com/kasbench/globeco-order-service)             | Java/PostgreSQL  | Done   |   Done          |                 | For microservice chain depth                     |
| [Trade Service](https://github.com/kasbench/globeco-trade-service)             | Java/PostgreSQL  | Done   |     Done        |                 | For microservice chain depth                     |
| [Execution Service](https://github.com/kasbench/globeco-execution-service)         | Java/PostgreSQL  | Done       |   Done          |                 | Asynchronous (producer)                          |
| [FIX Engine](https://github.com/kasbench/globeco-fix-engine)               | Go               |  Done      |   Done          |                 | Stochastic, asynchronous (consumer and producer) |
| [Real-Time Pricing Service](https://github.com/kasbench/globeco-pricing-service) | Java/PostgreSQL  | Done   |      Done       |                 | Stochastic                                       |
| [Security Service](https://github.com/kasbench/globeco-security-service)          | Python/MongoDB   | Done   |   Done          |                 | For microservice chain depth                     |
| Allocation Service        | Go               |        |             |                 | For microservice chain depth                     |
| [Confirmation Service](https://github.com/kasbench/globeco-confirmation-service)      | Go               | Done      |  Done            |                 | Asynchronous (consumer)                          |
| Partner Portal            | JavaScript/React |        |             |                 | Not needed initially                             |
| Company Intranet          | JavaScript/React |        |             |                 | UI                                               |
| Benchmark Coordinator     | Go               |        |             |                 | Not needed initially                             |
