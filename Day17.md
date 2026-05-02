# AWS Core Services – Notes (Learning Outcomes)



# AWS Global Accelerator

## What it is
AWS Global Accelerator is a networking service that improves:
- Application availability
- Performance
- User experience

## How it works
- Routes traffic through AWS global network backbone
- Uses Anycast IP addresses
- Directs users to the nearest healthy AWS endpoint

## Key Benefits
- Lower latency (faster access globally)
- Automatic failover
- Improves performance for global users
- Works with EC2, ALB, and NLB

---

# AWS Snow Family (Storage & Edge Computing)

## Overview
AWS Snow Family consists of physical devices used for:
- Data transfer
- Edge computing
- Offline data migration

---

## Snowcone

### Description
- Smallest device in Snow Family
- Portable and lightweight
- Used for edge computing and small data transfer

### Capabilities
- Runs EC2 instances on-device
- Supports AWS Lambda functions

### Use Cases
- Remote locations
- IoT data collection
- Field operations

---

## Snowball Edge

### Description
- Medium-sized device
- More powerful than Snowcone
- Used for large-scale data transfer and edge computing

### Capabilities
- Runs EC2 instances locally
- Supports AWS Lambda functions
- Transfers data to AWS S3

### Use Cases
- Industrial environments
- Large offline data migration

---

## Snowmobile

### Description
- Massive data transfer solution using a truck
- Designed for extremely large-scale data migration

### Capacity
- Up to 100 petabytes of data

### Use Cases
- Data center migration
- Enterprise-level bulk data transfer

---

# Edge Computing (AWS Snow Family)

## Definition
Edge computing is the process of processing data closer to where it is generated instead of sending everything to the cloud.

## Devices Used
- Snowcone
- Snowball Edge

## Capabilities
- Run EC2 instances locally
- Run AWS Lambda functions
- Store and process data at the edge

## Benefits
- Low latency
- Works without internet connectivity
- Reduces cloud bandwidth usage

---

# AWS Storage Mapping (Snow Family)

## Storage Flow
Snow devices transfer data into AWS storage services.

Snow Devices → Amazon S3 → Amazon Glacier

---

## Amazon S3
- Object storage service
- Used for active data storage

## Amazon Glacier
- Long-term archival storage
- Low cost
- Slower access time

---

# Comparison Table

| Service         | Type              | Capacity / Role     | Main Use Case |
|----------------|-------------------|---------------------|--------------|
| Snowcone       | Edge device       | Small               | Remote computing and IoT |
| Snowball Edge  | Edge + transfer    | Medium to large     | Data migration and edge computing |
| Snowmobile     | Data transfer      | 100 petabytes       | Massive data center migration |
| Global Accelerator | Networking service | Global routing     | Improve latency and performance |

---

# Summary
- AWS Global Accelerator improves global application performance using AWS backbone routing
- Snow Family provides physical devices for data transfer and edge computing
- Snowcone and Snowball support local compute and edge processing
- Snowmobile is used for extremely large-scale data migration (100 PB)
- Data eventually integrates into Amazon S3 and Amazon Glacier for storage and archival