# Scale up

## Diagram :
![Diagram](https://github.com/AnthonyCointre/holbertonschool-system_engineering-devops/blob/main/web_infrastructure_design/3-scale_up.jpg)


## Specifics about the infrastructure:

- For every additional element, why you are adding it:
    - 1 Server to provides additional resources or redundancy to support the expanded infrastructure.
    - 1 Load-Balancer Cluster to increases reliability and distribution efficiency by having multiple load-balancers share the load and provide failover capability.
    - 1 Split Components to separates different server roles to optimize performance and scalability, allowing each server to focus on a specific task and reducing the risk of a single component affecting the entire system.
