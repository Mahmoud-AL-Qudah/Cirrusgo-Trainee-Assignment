# Cirrusgo-Trainee-Assignment
🏗️ AWS 3-Tier WordPress Architecture

This project demonstrates the design and implementation of a highly available, scalable, and secure 3-tier web application on AWS using WordPress.

📌 Architecture Overview

The application follows a 3-tier architecture:

Presentation Layer: Application Load Balancer (ALB)

Application Layer: EC2 instances (Auto Scaling Group)

Data Layer: RDS MySQL (Multi-AZ)

Additional services:

Amazon EFS for shared storage

Bastion Host for secure access

CloudWatch for monitoring

🌐 Architecture Diagram
<img width="526" height="461" alt="image" src="https://github.com/user-attachments/assets/10dbc86e-b52c-49e4-a582-5c931fa9a5d5" />


🚀 Features

Highly available across multiple Availability Zones

Auto Scaling for handling traffic spikes

Secure network design using public/private subnets

Shared file storage using EFS

Managed relational database using RDS (Multi-AZ)

Monitoring and logging with CloudWatch

🧱 AWS Services Used

VPC (Virtual Private Cloud)

EC2 (Elastic Compute Cloud)

ALB (Application Load Balancer)

Auto Scaling Group

RDS (MySQL - Multi-AZ)

EFS (Elastic File System)

IAM (Roles & Policies)

CloudWatch

NAT Gateway

Internet Gateway

🔐 Security Design

EC2 instances are deployed in private subnets

RDS is not publicly accessible

Security Groups restrict traffic between tiers:

ALB → EC2

EC2 → RDS

IAM Roles are used instead of hardcoded credentials

Bastion host enables secure SSH access

⚙️ Setup Steps (Manual - AWS Console)

Create VPC and subnets (public & private)

Configure Internet Gateway and NAT Gateway

Set up route tables

Launch Bastion Host in public subnet

Create ALB in public subnets

Launch EC2 instances in private subnets

Configure Auto Scaling Group

Create RDS MySQL (Multi-AZ)

Create and mount EFS

Install and configure WordPress

Configure CloudWatch monitoring

📊 Non-Functional Requirements
✅ Reliability

Multi-AZ deployment

Auto Scaling and failover mechanisms

✅ Security

IAM roles and Security Groups

Private subnets for sensitive resources

✅ Performance Efficiency

Load balancing and scaling

EFS for shared storage

✅ Operational Excellence

Monitoring via CloudWatch

Automated recovery

✅ Cost Optimization

Right-sized resources

Auto Scaling to minimize idle cost

🧪 Challenges Faced

Configuring EFS mounting across instances

Setting up proper Security Group rules

Connecting WordPress to RDS securely

🔮 Future Improvements

Use Terraform for Infrastructure as Code

Add CI/CD pipeline (GitHub Actions)

Use CloudFront for caching and fast delivery + S3 for static content
