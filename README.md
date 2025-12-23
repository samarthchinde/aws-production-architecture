# aws-production-architecture
Production-style AWS infrastructure showcasing a secure, multi-AZ architecture using VPC, private subnets, Auto Scaling Groups, Application Load Balancer, NAT Gateways, Bastion Host, Jenkins, and a Python web application, with monitored traffic flow and high availability

# AWS Production-Style Infrastructure with Jenkins & Auto Scaling

This repository demonstrates a **production-grade AWS architecture** designed and implemented using real-world cloud and DevOps best practices.  
The project focuses on **security, scalability, high availability, and controlled access**.

---

## 🧠 Project Overview

The infrastructure hosts **Jenkins** and a **Python-based web application** on EC2 instances launched via **Auto Scaling Groups** in **private subnets**.  
Traffic is routed using an **Application Load Balancer**, outbound access is enabled through **NAT Gateways**, and secure administration is handled using a **Bastion Host**.

---

## 🏗 Architecture Highlights

- Multi-AZ AWS architecture
- Public and private subnet separation
- Auto Scaling Groups for fault tolerance
- Application Load Balancer for traffic distribution
- NAT Gateways for outbound internet access
- Bastion Host for secure SSH access
- Least-privilege security group design
- Monitoring via ALB health checks and ASG metrics

---

## 🔁 Workflow Overview

1. User requests hit the **Application Load Balancer**
2. ALB routes traffic to EC2 instances in **private subnets**
3. Instances are managed by **Auto Scaling Groups**
4. Jenkins and Python app run on private EC2 instances
5. Outbound traffic flows via **NAT Gateways**
6. SSH access is performed through **Bastion Host**
7. Health checks and traffic flow are continuously monitored

---

## 🛠 Tech Stack

**AWS (EC2, VPC, Auto Scaling, Application Load Balancer, NAT Gateway), Jenkins, Python, Security Groups, Bastion Host, CloudWatch (basic monitoring)**

---

## 🔐 Security Design

- No public IPs on application instances
- SSH access restricted to Bastion Host
- Application access restricted to ALB security group
- Least-privilege inbound and outbound rules

---

## 📊 Monitoring & Validation

- ALB health checks for instance availability
- Auto Scaling metrics for instance lifecycle
- Verified traffic flow and request distribution
- Service availability tested end to end

---

## 📸 Proof of Implementation

Screenshots of live resources are available in the `screenshots/` directory:
- Application Load Balancer
- Auto Scaling Group
- Jenkins running on EC2
- Bastion Host SSH access
- NAT Gateway configuration

---

## 📌 Key Learnings

- Real-world AWS networking and routing
- Secure access patterns using Bastion Host
- Importance of NAT Gateways for CI/CD tools
- High availability using Multi-AZ + ASG + ALB
- Cost-aware infrastructure decisions

---

## 🚀 Future Enhancements

- Infrastructure as Code (Terraform)
- CI/CD pipeline automation
- Centralized logging and monitoring
- Blue/Green deployment strategy

---

## 📬 Contact

Feel free to connect with me on LinkedIn for discussions around **AWS, Cloud Architecture, and DevOps**.
