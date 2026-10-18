# jenkins-tf-aws
Infrastructure automation repository utilizing Jenkins CI/CD pipelines to provision and manage AWS cloud resources via Terraform.

# Jenkins + Terraform AWS Infrastructure Project
Overview
This project demonstrates how to integrate Jenkins pipelines with Terraform to automate AWS infrastructure provisioning.  
The pipeline is parameterized to support both apply and destroy actions, enabling flexible creation and teardown of resources directly from Jenkins.

Features
- Jenkins pipeline with multiple stages:
  - Checkout: Pulls Terraform code from GitHub.
  - Init: Runs `terraform init` to configure backend and providers.
  - Plan: Previews infrastructure changes.
  - Action: Executes `terraform apply` or `terraform destroy` based on user input.
  - Parameterized pipeline (action) for flexible deployments.

- AWS resources provisioned:
  - Custom VPC (172.16.0.0/16)
  - Security Group with rules for SSH (22) and Jenkins UI (8080)
  - EC2 Instance (Ubuntu, t2.micro) tagged for Jenkins


- Tech Stack
  - Jenkins (Pipeline as Code)
  - Terraform (Infrastructure as Code)
  - AWS (EC2, VPC, Security Groups)
  - GitHub (Version Control)

Files
- Jenkinsfile → Defines CI/CD pipeline stages.
- main.tf → Terraform configuration for AWS resources.
- variables.tf → Input variables for region, AMI, instance type, tags.

Skills Demonstrated
- CI/CD automation with Jenkins
- Infrastructure provisioning with Terraform
- AWS networking and compute setup
- Parameterized pipelines for flexible workflows
- GitHub integration with Jenkins

---
