# AWS 3-Tier Architecture Deployment

## 📌 Project Overview
This project focuses on designing and implementing a **highly available, scalable, and secure 3-tier architecture** on AWS. It ensures **performance, fault tolerance, and security** by leveraging key AWS services.

## 🔥 Architecture Breakdown
The architecture is divided into **three tiers**:

### ⚡️ Presentation Layer (Web Tier)
- Public-facing **Amazon EC2** instances deployed in a **public subnet**.
- Managed by an **Auto Scaling Group (ASG)**.
- Traffic distribution via **Application Load Balancer (ALB)**.

### ⚡️ Application Layer (App Tier)
- Private **Amazon EC2** instances hosting backend services.
- Deployed in a **private subnet** for enhanced security.
- Connected only to the **web tier**.

### ⚡️ Data Layer (Database Tier)
- **Amazon RDS (MySQL)** instance deployed in a **private subnet**.
- Multi-AZ replication for **high availability**.
- Accessible only from the **application layer**.

## 🚀 AWS Services Used
- **Networking:** VPC, Subnets, NAT Gateway, Internet Gateway
- **Compute:** Amazon EC2 with Auto Scaling Groups (ASG)
- **Load Balancing:** Application Load Balancer (ALB)
- **Database:** Amazon RDS (Multi-AZ MySQL)
- **Security:** Security Groups, IAM Roles

## 🏗️ Implementation Steps
### 1️⃣ VPC & Subnet Setup
- Create a **VPC** and define CIDR block.
- Setup **public and private subnets**.
- Attach an **Internet Gateway** for external access.
- Deploy a **NAT Gateway** for private subnet outbound traffic.

### 2️⃣ Security Configuration
- **Web Security Group**: Allows HTTP(S) from ALB only.
- **App Security Group**: Restricts access to only Web Tier.
- **Database Security Group**: Allows traffic only from App Tier.

### 3️⃣ EC2 Instance Setup
- Launch EC2 instances for **Web and App layers**.
- Install necessary software (Nginx, backend services).
- Create **Amazon Machine Images (AMIs)**.

### 4️⃣ Load Balancer & Auto Scaling Setup
- Deploy **ALBs** for both Web & App tiers.
- Create **Target Groups** for traffic distribution.
- Setup **Auto Scaling Groups** to handle traffic spikes.

### 5️⃣ RDS Database Setup
- Deploy **Amazon RDS (MySQL)** inside **private subnet**.
- Enable **Multi-AZ deployment** for failover protection.

## 🏆 Key Features
✅ **Scalability** - Auto Scaling Groups handle traffic fluctuations.  
✅ **High Availability** - Multi-AZ RDS ensures database reliability.  
✅ **Security** - Network segmentation with VPC, Subnets & Security Groups.  
✅ **Performance** - Load balancing optimizes traffic distribution.  

## 📂 Repository
🔗 **GitHub Repository**: [https://github.com/venkatraja1234/3-TIER-ARCHITECTURE]

## 📌 Conclusion
This project follows AWS best practices to deploy a **secure, scalable, and fault-tolerant** web application infrastructure. 🚀

**#AWS #CloudComputing #DevOps #InfrastructureAsCode #Networking #Scalability**
