# Architecture Description

This document provides detailed descriptions of each component used in the AWS-based secure and scalable web application.

## AWS Components

1. **AWS WAF & Shield**: 
   - AWS WAF protects the application by filtering incoming traffic based on rules.
   - AWS Shield provides managed DDoS protection to defend against attacks.

2. **DNS**:
   - Routes requests from users to the application via AWS Route 53.

3. **Public-Facing Application Load Balancer**:
   - Distributes incoming traffic across multiple EC2 instances in different availability zones.
   - Integrated with Auto Scaling to adjust the number of instances based on load.

4. **Auto Scaling Group**:
   - Automatically scales EC2 instances based on demand, ensuring high availability.

5. **EC2 Instances**:
   - Hosts the application code. Instances are spread across multiple availability zones to increase reliability.

6. **AWS CloudWatch**:
   - Monitors the application's health and logs security incidents.
   - Provides insights into application performance and security.

## Network and Security

- Public subnets are configured for load balancers.
- Private subnets for EC2 instances help to increase security.
- AWS WAF rules and Shield provide an additional layer of security.
