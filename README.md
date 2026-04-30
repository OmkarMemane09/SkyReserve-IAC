
# AWS EKS Three-Tier Infrastructure using Terraform

This project provisions a production-style three-tier cloud infrastructure on AWS using Terraform. It demonstrates Infrastructure as Code (IaC) principles by automating the setup of a scalable and secure environment, including networking, compute, and container orchestration.

##  Key Features

- Automated infrastructure provisioning using Terraform
- VPC setup with public and private subnets across multiple availability zones
- Secure networking with Internet Gateway, NAT Gateway, and route tables
- Amazon EKS cluster setup for container orchestration
- Managed node groups for scalable worker nodes
- IAM roles and policies for secure access control
- Load balancing for application exposure
- Modular Terraform code structure for reusability

##  Architecture Overview

- **Frontend Tier**: Load balancer for handling incoming traffic
- **Application Tier**: Kubernetes workloads running on EKS
- **Database Tier**: (Optional) Can be extended with RDS or external DB

## Tech Stack

- Terraform (Infrastructure as Code)
- AWS (EKS, EC2, VPC, IAM, ALB)
- Kubernetes
- AWS CLI

##  Project Structure

- `vpc/` → Networking resources
- `eks/` → EKS cluster and node groups
- `iam/` → Roles and policies
- `alb/` → Load balancer configuration
- `main.tf` → Root configuration
- `variables.tf` → Input variables
- `outputs.tf` → Outputs

##  Setup Instructions

### 1. Configure AWS credentials
### 2. Initialize Terraform
```
terraform init
```

### 3. Apply infrastructure
```
terraform apply
```
### 4. Destroy infrastructure
```
terraform destroy
```

##  Learning Outcomes

- Hands-on experience with real-world cloud infrastructure
- Understanding of Terraform state management and dependencies
- Deploying and managing Kubernetes clusters on AWS
- Implementing secure and scalable architecture design

##  Notes

- Ensure proper IAM permissions before deployment
- Clean up resources using `terraform destroy` to avoid unnecessary costs

##  Future Improvements

- Add CI/CD pipeline (Jenkins/GitHub Actions)
- Integrate monitoring (Prometheus, Grafana)
- Add autoscaling and logging
