# KASBench: A Benchmark for Kubernetes Autoscaling

<img src="../images/globeco-logo.png" alt="Logo" width="100">
KASBench is a new benchmark under development for Kubernetes Autoscaling. GlobeCo is a suite of applications designed to subject autoscalers to a variety of real-world conditions including long call chains, heterogeneous languages, multiple types of stateful data storage, synchronous and asynchronous calling patterns, LLM inferencing, CPU-intensive service, network-intensive services, and disk IO-intensive services.



## Portfolio Management

Potfolio management is one application in the GlobeCo suite.  It is a simulated portfolio management application, including order generation, order management, trading, and execution. 

<img src="../images/GlobeCo Portfolio Management and Trading.png">


### Status

| Microservice              | Language         | Coding | Integration | Instrumentation | Notes                                            |
| ------------------------- | ---------------- | ------ | ----------- | --------------- | ------------------------------------------------ |
| Portfolio Service         | Python/MongoDB   | Done   |             |                 | CPU-light                                        |
| Portfolio Optimizer       | Go or Python     |        |             |                 | CPU-intensive Golang                             |
| Balance Service           | Java/Vitess      |        |             |                 | Database-intensive                               |
| Order Generation Service  | Python           |        |             |                 | CPU-intensive Python                             |
| Order Service             | Java/PostgreSQL  | Done   |             |                 | For microservice chain depth                     |
| Trade Service             | Java/PostgreSQL  | Done   |             |                 | For microservice chain depth                     |
| Execution Service         | Java/PostgreSQL  | Done       |             |                 | Asynchronous (producer)                          |
| FIX Engine               | Go               |  In progress      |             |                 | Stochastic, asynchronous (consumer and producer) |
| Real-Time Pricing Service | Java/PostgreSQL  | Done   |             |                 | Stochastic                                       |
| Security Service          | Python/MongoDB   | Done   |             |                 | For microservice chain depth                     |
| Allocation Service        | Go               |        |             |                 | For microservice chain depth                     |
| Confirmation Service      | Go               |        |             |                 | Asynchronous (consumer)                          |
| Partner Portal            | JavaScript/React |        |             |                 | Not needed initially                             |
| Company Intranet          | JavaScript/React |        |             |                 | UI                                               |
| Benchmark Coordinator     | Go               |        |             |                 | Not needed initially                             |
