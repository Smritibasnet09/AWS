# NAT (Network Address Translation) in AWS

## 🔹 NAT Instance

### Definition
A NAT Instance is an Amazon EC2 instance configured to allow instances in private subnets to access the internet while blocking inbound connections initiated from the internet.

### Concept
- Placed in a **public subnet** with a public IP  
- Enables **outbound internet access** for private instances  
- Blocks **inbound internet traffic**  
- Requires **disabling source/destination check**  

### Configuration
- Update **route tables** in private subnets to route traffic via NAT Instance  
- Configure **security groups**:
  - Inbound:
    - Allow HTTP/HTTPS from private subnets  
    - Allow SSH from trusted IPs  
  - Outbound:
    - Allow HTTP/HTTPS to the internet  

### Limitations
- Not highly available by default  
- No automatic scaling  
- Bandwidth depends on EC2 instance type  
- Requires manual maintenance  

### Key Point
Provides more control but requires manual setup and management  

---

## 🔹 NAT Gateway

### Definition
A NAT Gateway is a fully managed AWS service that provides scalable and highly available outbound internet access for instances in private subnets.

### Concept
- Managed by AWS (no maintenance required)  
- Deployed in a specific Availability Zone  
- Assigned an Elastic IP  
- Automatically handles high traffic  

### Behavior
- Traffic flow: Private Subnet → NAT Gateway → Internet Gateway → Internet  
- Cannot be used by instances in the same subnet  

### Features
- High availability (within an AZ)  
- Automatic scaling (5 Gbps to 100 Gbps)  
- No security group management required  

### Fault Tolerance
- Deploy one NAT Gateway per Availability Zone  
- No cross-AZ failover needed  

### Pricing
- Based on usage duration and bandwidth  

### Key Point
Provides high availability and scalability with minimal management  

---

## 🔄 Comparison

| Feature          | NAT Instance          | NAT Gateway          |
|------------------|----------------------|----------------------|
| Management       | Manual               | Fully Managed        |
| Availability     | Low                  | High                 |
| Scaling          | Manual               | Automatic            |
| Bandwidth        | Depends on instance  | Up to 100 Gbps       |
| Security Groups  | Required             | Not Required         |
| Cost             | Instance-based       | Usage-based          |

---

## 🧠 Exam Tip

- NAT Instance → More control, more maintenance  
- NAT Gateway → Less control, more scalable  