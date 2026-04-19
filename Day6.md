# Day 6 — AWS VPC (Amazon Virtual Private Cloud)

Today I am learning about **Amazon VPC**, which is one of the most important networking services in AWS. It basically helps you create your own isolated network inside AWS, where you can launch and manage resources like EC2 instances securely.

---

## 1. IP Addresses 

Before understanding VPC, it’s important to know what an IP address is.

- An **IP address** is a unique number assigned to each device in a network.
- It helps devices identify and communicate with each other.

There are two main types:

- **IPv4**: 32-bit address format (example: `192.168.1.1`)
- **IPv6**: 128-bit address format (newer version with a much larger address space)

IP addresses are like “home addresses” for devices on a network.

---

## 2. CIDR (Classless Inter-Domain Routing)

CIDR is a method used to efficiently manage IP addresses.

Instead of fixed classes (like old systems), CIDR allows flexible allocation.

### Example:

- `192.168.1.0` → network address  
- `/24` → shows how many bits are used for the network part  

### Why CIDR is important:
- Helps in better IP allocation
- Reduces wastage of IP addresses
- Commonly used in AWS VPC networking

CIDR defines “how big or small your network is.”

---

## 3. What is AWS VPC?

**Amazon VPC (Virtual Private Cloud)** is a service that lets you create your own private network inside AWS.

You can think of it like:
> A private section of AWS where you control networking completely.

Inside a VPC, you can:
- Launch EC2 instances
- Control IP ranges
- Set up subnets
- Manage routing and security

---

## 4. Default VPC in AWS

Every AWS account automatically comes with a **default VPC**.

### Key points:

- When you launch an EC2 instance **without selecting a subnet**, it goes into the default VPC.
- The default VPC already has internet connectivity configured.
- EC2 instances in default VPC automatically get:
  - Public IPv4 address
  - Private IPv4 address
  - Public DNS name

---

## 5. Why Default VPC is Useful

The default VPC is mainly for beginners and quick setups.

It helps because:
- You don’t need to configure networking from scratch
- Instances can connect to the internet immediately
- Useful for testing and learning AWS

But in real-world projects:
> Engineers usually create **custom VPCs** for better security and control.

---

## 6. Simple Mental Model

Think of VPC like this:

- **AWS = big city**
- **VPC = your private house compound**
- **Subnets = rooms inside the house**
- **EC2 instances = devices inside rooms**
- **Internet Gateway = door to outside world**

So you fully control who enters, who leaves, and how communication happens.

---

## 7. Summary

Today’s learning:

- IP addresses identify devices on a network
- IPv4 is 32-bit, IPv6 is 128-bit
- CIDR helps efficiently allocate IP ranges
- VPC is your private network inside AWS
- Default VPC is automatically created in every AWS account
- EC2 instances in default VPC get internet access by default

---

## Final Thought

VPC is basically the foundation of AWS networking. Once you understand this properly, things like subnets, route tables, NAT gateways, and security groups will start making much more sense.
