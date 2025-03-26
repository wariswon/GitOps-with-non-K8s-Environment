# Pull-Based GitOps with Non-Kubernetes Environment on AWS

This project implements a **Pull-Based GitOps Workflow** with **automatic rollback** for AWS infrastructure using **Terraform & AWS Lambda**. It ensures that AWS resources strictly follow Git, and any manual changes are automatically reverted.

## Features
**Pull-Based GitOps** → AWS Lambda pulls changes from GitHub and triggers CodeBuild to apply Terraform.  
**Auto-Revert** → AWS Config detects manual changes, and Lambda restores AWS resources to match Git.  
**Fully Automated Workflow** → No manual intervention required.  

## Folder Structure
- **[`Auto-Pull-Changes/`](./Auto-Pull-Changes/)** → Stores the Lambda function for pulling changes from Git and triggering CodeBuild.  
- **[`Auto-Revert/`](./Auto-Revert/)** → Stores the Lambda function for detecting drift and reverting AWS changes.  
- **[`Resources/`](./Resources/)** → Stores Terraform configurations for provisioning AWS infrastructure.

## How to Use
1️⃣ **Deploy AWS Resources** using Terraform (`Resources/`).  
2️⃣ **Set Up Auto-Pull Changes** (`Auto-Pull-Changes/`).  
3️⃣ **Set Up Auto-Revert** (`Auto-Revert/`).  

Follow the setup instructions in each folder.  

