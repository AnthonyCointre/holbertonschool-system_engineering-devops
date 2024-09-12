# Simple web stack

## Diagram :
![Diagram](https://github.com/AnthonyCointre/holbertonschool-system_engineering-devops/blob/main/web_infrastructure_design/0-simple_web_stack.jpg)


## User want to access the website :

- The user enters www.foobar.com in their browser, triggering a DNS request.
- The DNS server resolves www.foobar.com to 8.8.8.8 using the A record.
- The browser sends an HTTP request to 8.8.8.8, which reaches the server.
- The Nginx web server on the server receives the request and forwards it to the application server.
- The application server processes the request using the application files.
- The application server interacts with the MySQL database to retrieve or store data.
- The response is sent back through Nginx to the user's browser, displaying the requested webpage.


## Specifics about the infrastructure:

- What is a server:
    - A server is a computer that provides services or resources to other computers over a network.

- What is the role of the domain name:
    - A domain name translates human-readable addresses into IP addresses for locating servers.

- What type of DNS record www is in www.foobar.com:
    - The www in www.foobar.com is typically a CNAME record that maps to a canonical domain name.

- What is the role of the web server:
    - A web server handles HTTP requests and delivers static content or routes requests to application servers.

- What is the role of the application server:
    - An application server processes server-side logic and interacts with databases to generate dynamic content.

- What is the role of the database:
    - A database stores and manages data used by the application and accessed via the application server.

- What is the server using to communicate with the computer of the user requesting the website:
    - The server communicates with the user's computer using the HTTP or HTTPS protocol.


## Issues with the infrastructure:

- SPOF:
    - SPOF (Single Point of Failure) is a component whose failure can cause the entire system to become unavailable.

- Downtime when maintenance needed (like deploying new code web server needs to be restarted):
    - Downtime during maintenance occurs when restarting a web server is necessary, leading to temporary unavailability.

- Cannot scale if too much incoming traffic:
    - Inability to scale means the system cannot handle increased traffic effectively, causing potential slowdowns or outages.
