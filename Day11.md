# AWS Route 53 Routing Policies (My Notes)

## 1. Simple Routing
I use Simple Routing when I have one domain pointing to one server. It is the most basic routing type.

**My memory trick:**  
Simple = Single server (no confusion)

---

## 2. Weighted Routing
I use Weighted Routing when I want to split traffic between multiple servers using percentages.

Example:  
- 70% traffic → Server A  
- 30% traffic → Server B  

**My memory trick:**  
Weighted = Weight decides traffic share

---

## 3. Failover Routing
I use Failover Routing when I need a backup system. Traffic goes to the primary server, and if it fails, it switches to the secondary server.

**My memory trick:**  
Failover = First fails, backup saves

---

## 4. Latency-Based Routing
I use Latency-Based Routing to send users to the server with the lowest response time (fastest performance).

**My memory trick:**  
Latency = Less delay = faster access

---

## 5. Geolocation Routing
I use Geolocation Routing when I want to route traffic based on the user’s country or region.

**My memory trick:**  
Geo = Geography decides route

---

## 6. Multi-Value Routing
I use Multi-Value Routing to return multiple healthy IP addresses so that availability is improved.

**My memory trick:**  
Multi-value = Many answers for one request

---

## 7. Geoproximity Routing
I use Geoproximity Routing when I want to route traffic based on distance, and I can also adjust bias to shift traffic.

**My memory trick:**  
Geoproximity = Nearby + adjustable control

---

## 8. IP-Based Routing
I use IP-Based Routing when I want to route traffic based on the user’s IP address or IP range.

**My memory trick:**  
IP = Identity of network decides route

---

# Quick Revision Trick

## Order I remember:
S W F L G M G I

- S → Simple  
- W → Weighted  
- F → Failover  
- L → Latency  
- G → Geolocation  
- M → Multi-value  
- G → Geoproximity  
- I → IP-based  

**My mnemonic sentence:**  
Some Wise Friends Like Good Modern Global Internet