# AWS Route 53 Routing Policies (Simple Memory Notes)

## 1. Simple Routing
**Meaning:** One domain → one server (basic setup)

**Memory Trick:**  
Simple = Single server (no confusion)

---

## 2. Weighted Routing
**Meaning:** Traffic is split using percentages (weights)

Example:  
- 70% → Server A  
- 30% → Server B  

**Memory Trick:**  
Weighted = Weight decides traffic share

---

## 3. Failover Routing
**Meaning:** Primary server + backup server (switch if failure happens)

**Memory Trick:**  
Failover = First fails, backup saves

---

## 4. Latency-Based Routing
**Meaning:** Routes users to the fastest (lowest delay) server

**Memory Trick:**  
Latency = Less delay = faster access

---

## 5. Geolocation Routing
**Meaning:** Routes based on user’s location (country/continent)

**Memory Trick:**  
Geo = Geography decides route

---

## 6. Multi-Value Routing
**Meaning:** Returns multiple healthy IPs for better availability

**Memory Trick:**  
Multi-value = Many answers for one request

---

## 7. Geoproximity Routing
**Meaning:** Routes based on distance + allows bias control (shift traffic)

**Memory Trick:**  
Geoproximity = Nearby + adjustable control

---

## 8. IP-Based Routing
**Meaning:** Routes based on user IP address or IP range

**Memory Trick:**  
IP = Identity of network decides route

---

# Quick Revision Trick

## Order:
S W F L G M G I

- S → Simple  
- W → Weighted  
- F → Failover  
- L → Latency  
- G → Geolocation  
- M → Multi-value  
- G → Geoproximity  
- I → IP-based  

**Mnemonic Sentence:**  
Some Wise Friends Like Good Modern Global Internet