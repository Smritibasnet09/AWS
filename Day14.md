# AWS Core Services Notes

## 1. Amazon SQS (Simple Queue Service)

### Overview
Amazon SQS is a fully managed **message queuing service** that enables decoupling of application components and supports asynchronous communication.

### Key Features
- Fully managed (no server management)
- Highly scalable and reliable
- Messages stored redundantly across multiple Availability Zones
- Supports asynchronous processing

### Types of Queues
- **Standard Queue**
  - At-least-once delivery
  - Best-effort ordering

- **FIFO Queue**
  - Exactly-once processing
  - Strict message ordering

### Use Cases
- Decoupling microservices
- Background job processing
- Handling traffic spikes using buffering

---

## 2. Amazon DynamoDB

### Overview
Amazon DynamoDB is a fully managed **NoSQL database service** designed for high performance and scalability.

### Key Features
- Serverless (automatic scaling)
- Low latency (single-digit milliseconds)
- Key-value and document data model
- Built-in security, backup, and restore

### Core Concepts
- **Table** → Collection of items
- **Item** → Individual record
- **Attribute** → Data field
- **Primary Key**
  - Partition Key
  - Optional Sort Key

### Use Cases
- Real-time applications
- IoT data storage
- Gaming applications
- E-commerce platforms

---

## 3. Amazon FSx

### Overview
Amazon FSx provides **fully managed file storage services** using popular file systems.

### Types
- **FSx for Windows File Server**
  - Supports SMB protocol
  - Integrated with Windows environments

- **FSx for Lustre**
  - High-performance file system
  - Suitable for HPC and ML workloads

### Key Features
- Fully managed file systems
- High throughput and low latency
- Scalable storage
- Integration with AWS services

### Use Cases
- Shared file storage
- Machine learning workloads
- Media processing and rendering

---

## 4. Amazon RDS MySQL (Multi-AZ DB Instance)

### Overview
Amazon RDS is a managed relational database service. A **Multi-AZ deployment** improves availability and fault tolerance.

### Key Features
- Managed MySQL database
- Automated backups and patching
- High availability with Multi-AZ deployment

### Multi-AZ Architecture
- Primary DB instance in one Availability Zone
- Standby replica in another Availability Zone
- Automatic failover during outages

### Benefits
- Increased availability
- Data redundancy
- Minimal downtime

### Use Cases
- Production-grade applications
- Financial systems
- Web applications requiring high availability

---

## Quick Comparison

| Service   | Type           | Purpose                          |
|----------|----------------|----------------------------------|
| SQS      | Messaging      | Decouple application components  |
| DynamoDB | NoSQL Database | Scalable key-value storage       |
| FSx      | File Storage   | Managed file systems             |
| RDS      | Relational DB  | Structured data and transactions |
