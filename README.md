# CloudFormation Practice Repository

This repository contains my practice CloudFormation templates for building AWS infrastructure.

## 📁 Templates Included

### **advanced-web-stack.yaml**
A full-stack template that automatically creates:

- VPC  
- Public Subnet  
- Internet Gateway  
- Route Table  
- Security Group  
- EC2 instance with Nginx (via UserData)  
- S3 bucket with tags  
- Outputs including public IP and website URL  

You can deploy this file using AWS CloudFormation Console or AWS CLI.

---

## 🚀 How to Deploy (CLI)

```bash
aws cloudformation create-stack \
  --stack-name cf-practice-stack \
  --template-body file://advanced-web-stack.yaml \
  --parameters ParameterKey=KeyName,ParameterValue=your-keypair
