# AWS Service Catalog for Self-Service Provisioning

Team: Prasanth Ineni, Nayikala Viswa Meghana, Kona Mohana, Para Sree Nithya
Course Code: 24CC3014-P066
Instructor: Padmavathi mam

## Problem
Users depend on administrators to create AWS resources. This is slow and can cause wrong or insecure configurations.

## Solution
AWS Service Catalog lets the administrator publish approved products. Users launch them with one click, and CloudFormation creates the resources automatically.

## Flow
Administrator -> Product -> Portfolio -> Constraint + Access -> User launches -> CloudFormation -> EC2 instance

## AWS services used
- AWS Service Catalog
- AWS CloudFormation
- AWS IAM (LabRole)
- Amazon EC2

## What was created
- Portfolio: Development-Portfolio
- Product: EC2 Development Server (version v1)
- Launch constraint: LabRole
- Access granted to: LabRole
- Provisioned product: my-dev-server (Available)
- CloudFormation stack: created by Service Catalog (CREATE_COMPLETE)
- EC2 instance: DevServer-ServiceCatalog (t3.micro, Running)

## Files
- templates/ec2-dev-server.yaml : CloudFormation template
- screenshots/ : proof of each step
- presentation/ : project slides

## Result
The user launched an approved EC2 server without administrator help, and it followed the approved configuration.
## Repository files
- ec2-dev-server.yaml : CloudFormation template used by the product
- servicecatalog-project.yaml : portfolio, product, constraint and access as code
- portfolio.json, product.json, constraints.json, access.json, provisioned-product.json : configuration exported from AWS
- Screenshots : proof of each step
- AWSProj_ppt1.pptx : project presentation
