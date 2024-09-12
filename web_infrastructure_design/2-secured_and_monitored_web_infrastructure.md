# Secured and monitored web infrastructure

## Diagram :
![Diagram](https://github.com/AnthonyCointre/holbertonschool-system_engineering-devops/blob/main/web_infrastructure_design/2-secured_and_monitored_web_infrastructure.jpg)


## Specifics about the infrastructure:

- For every additional element, why you are adding it:
    - 3 Firewalls to provide layered security by blocking unauthorized access and preventing potential attacks.
    - 1 SSL Certificate to secures data in transit, protects user privacy, and ensures the authenticity of the website.
    - 3 Monitoring Clients to track system performance, detect anomalies, and ensure the infrastructure is operating correctly.

- What are firewalls for:
    - Firewalls control and monitor network traffic, enforcing security policies to protect against unauthorized access and cyber threats.

- Why is the traffic served over HTTPS:
    - HTTPS encrypts data transmitted between users and the server, protecting sensitive information and ensuring data integrity and privacy.

- What monitoring is used for:
    - Monitoring provides insights into system performance, helps detect issues early, and aids in troubleshooting and optimizing the infrastructure.

- How the monitoring tool is collecting data:
    - Monitoring tools collect data through agents or APIs installed on servers, which gather metrics like CPU usage, memory, and network traffic, and send them to a central monitoring system.

- Explain what to do if you want to monitor your web server QPS:
    - To monitor Queries Per Second (QPS) on your web server, configure the monitoring tool to track and report on the number of requests the server handles within a given time frame.


## Issues with the infrastructure:

- Why terminating SSL at the load balancer level is an issue:
    - If SSL is terminated at the load balancer, traffic between the load balancer and the web server is unencrypted, potentially exposing data to internal network threats.

- Why having only one MySQL server capable of accepting writes is an issue:
    - Having only one MySQL server for write operations creates a single point of failure and limits scalability, as the server can become a bottleneck under high load.

- Why having servers with all the same components (database, web server and application server) might be a problem:
    - Having servers with identical database, web server, and application server can create management complexity, redundancy issues, and reduce fault tolerance, as failure in one server type impacts multiple functions.
