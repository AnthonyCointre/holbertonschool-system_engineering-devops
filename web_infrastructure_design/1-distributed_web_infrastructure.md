# Distributed web infrastructure

## Diagram :
![Diagram](https://github.com/AnthonyCointre/holbertonschool-system_engineering-devops/blob/main/web_infrastructure_design/1-distributed_web_infrastructure.jpg)


## Specifics about the infrastructure:

- For every additional element, why you are adding it:
    - 2 Servers to provides redundancy and failover capability.
    - 1 Web Serverto manages web traffic and serves static content efficiently.
    - 1 Application Server to handles dynamic content and business logic.
    - 1 Load-Balancer to distributes traffic to prevent any single server from becoming a bottleneck.
    - 1 Application Files to needed for the application to function.
    - 1 Database to stores data required by the application.

- What distribution algorithm your load balancer is configured with and how it works:
    - Common algorithms include round-robin, least connections, and IP hash.

- Is your load-balancer enabling an Active-Active or Active-Passive setup, explain the difference between both:
    - Active-Active: All servers handle traffic simultaneously, balancing the load and providing redundancy.
    - Active-Passive: Only one server handles traffic while the other remains idle, taking over only if the active server fails.

- How a database Primary-Replica (Master-Slave) cluster works:
    - The Primary (Master) node handles write operations and data changes.
    - The Replica (Slave) nodes handle read operations and synchronize data from the Primary, providing load distribution and redundancy.

- What is the difference between the Primary node and the Replica node in regard to the application:
    - The Primary node accepts writes and updates data.
    - The Replica node only handles read queries and replicates data from the Primary node.


## Issues with the infrastructure:

- Where are SPOF:
    - The database or the load balancer could be a SPOF if they fail and are not redundant.

- Security issues (no firewall, no HTTPS):
    - No Firewall: Lacks protection against unauthorized access and attacks.
    - No HTTPS: Data transmitted over the network is not encrypted, risking exposure of sensitive information.

- No monitoring:
    - Absence of monitoring means potential issues may go unnoticed, leading to undetected performance problems or outages.
