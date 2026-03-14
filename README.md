# Resilient and Scalable Web Application Deployment on AWS

## Overview
This project demonstrates the design and deployment of a **highly available, resilient, and scalable web application architecture on AWS**. The infrastructure leverages multiple AWS services to ensure **fault tolerance, automatic scaling, load balancing, and secure access**.

The architecture distributes application resources across **multiple Availability Zones (AZs)** to minimize downtime and maintain application performance during traffic spikes or infrastructure failures.

---

## Architecture Goals

### High Availability
Ensure minimal downtime by deploying resources across **multiple Availability Zones**.

### Scalability
Automatically adjust compute capacity using **Auto Scaling** to handle varying traffic loads.

### Security
Implement secure networking and access control using **security groups and isolated network environments**.

### Resilience
Design the system to **recover automatically from failures** and continue operating without manual intervention.

---

## AWS Services Used

### Virtual Private Cloud (VPC)
A **custom VPC** is created to provide an isolated networking environment.

Key components include:
- Public subnets for load balancers
- Private subnets for application servers
- Multiple Availability Zones for redundancy

---

### Elastic Compute Cloud (EC2)
EC2 instances host the web application.

Features:
- Scalable compute capacity
- Secure instance configuration
- Custom AMI for consistent instance deployment

---

### Elastic File System (EFS)
Provides **shared and scalable file storage** accessible by all EC2 instances.

Benefits:
- Concurrent access from multiple servers
- Automatic scaling of storage
- Persistent shared application data

---

### Auto Scaling
Auto Scaling dynamically adjusts the number of EC2 instances based on demand.

Capabilities:
- Automatic scaling during traffic spikes
- Cost optimization during low traffic
- Health checks and instance replacement

---

### Application Load Balancer (ALB)
The ALB distributes incoming traffic across multiple EC2 instances.

Benefits:
- Improves fault tolerance
- Prevents server overload
- Ensures efficient request routing

---

### Route 53
Route 53 is used for **DNS management and traffic routing**.

Functions:
- Domain name management
- Reliable request routing
- Integration with AWS load balancers

---

## Architecture Flow

User Request → Route 53 → Application Load Balancer → Auto Scaling EC2 Instances → Shared Storage (EFS)

The application runs across **multiple Availability Zones**, ensuring high availability and fault tolerance.

---

## Project Phases

### 1. Design Phase
Architecture planning focused on:

- Security
- Scalability
- High availability
- Fault tolerance

---

### 2. Implementation Phase

Steps performed:

1. Create custom VPC
2. Configure public and private subnets
3. Setup security groups
4. Deploy and configure EFS
5. Create a custom EC2 AMI
6. Configure Auto Scaling groups
7. Deploy Application Load Balancer
8. Configure Route 53 for DNS routing

---

### 3. Testing and Optimization Phase

Testing performed includes:

- Functional testing
- Load testing
- Failover simulation
- Performance tuning

---

### 4. Documentation Phase

Comprehensive documentation was created covering:

- Architecture design
- Infrastructure configuration
- Deployment procedures
- Performance optimization

---

## Project Deliverables

- Architecture diagrams
- Deployment and configuration guide
- Performance and optimization report
- Project presentation explaining:
  - Deployment strategy
  - Challenges faced
  - Solutions implemented

---

## Key Features

- Multi-AZ High Availability
- Automatic Horizontal Scaling
- Load Balanced Infrastructure
- Shared File Storage with EFS
- Secure Networking with VPC
- Domain Routing with Route 53

---

## Future Improvements

- Implement CI/CD pipeline using GitHub Actions or AWS CodePipeline
- Add monitoring using CloudWatch
- Integrate WAF for enhanced security
- Implement containerized deployment using Docker and ECS

---

## Author

**Divesh Bhakari**
