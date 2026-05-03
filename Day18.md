# Learning of Today

# **Simple Routing**  
Simple routing is the most basic type of routing. In this, a domain name is connected to only one server or IP address. Whenever a user requests that domain, they are always sent to the same server. It does not consider anything like location, traffic, or server health.  
Example: example.com → 192.168.1.1 (all users go to this one server)

**Weighted Routing**  
Weighted routing is used when you want to distribute traffic between multiple servers based on assigned percentages. Each server is given a weight, and traffic is divided according to those weights.  
Example: Server A (weight 70) gets about 70% traffic, Server B (weight 30) gets about 30% traffic

**Failover Routing**  
Failover routing is used for reliability. In this, there is a primary server and a backup server. Normally, all traffic goes to the primary server. If the primary server fails, traffic is automatically redirected to the backup server.  
Example: Primary → Server A, Backup → Server B; if Server A goes down, all traffic shifts to Server B

**Latency-Based Routing**  
Latency-based routing focuses on performance. It sends users to the server that provides the fastest response time based on their location and network conditions.  
Example: A user in Nepal is routed to an Asia server, while a user in Europe is routed to a Europe server

**Geolocation Routing**  
Geolocation routing is based on the user’s physical location. Traffic is routed depending on the country or region from which the request is coming.  
Example: Users from Nepal → Server A, Users from India → Server B

**Multi-Value Routing**  
Multi-value routing returns multiple healthy servers instead of just one. The system checks which servers are available and provides a list of them. The client then chooses one.  
Example: DNS returns three IPs (192.168.1.1, 192.168.1.2, 192.168.1.3), and the user connects to one of them

**Geoproximity Routing**  
Geoproximity routing routes traffic based on how close a user is to a server, but also allows manual control to shift traffic between regions.  
Example: Even if users are closer to Server A, you can shift more traffic toward Server B to balance load

**IP-Based Routing**  
IP-based routing uses the user’s IP address to decide where to send the request. Different IP ranges can be mapped to different servers.  
Example: Company IP range → Internal server, Public users → Public server