# Security Settings

This document describes the security configurations for the AWS-based application.

## AWS WAF Rules

1. Go to **AWS WAF** and configure custom rules.
2. Add rules to:
   - Block IP addresses with known malicious activity.
   - Filter traffic based on geolocation.
   - Rate limit requests to prevent abuse.

## AWS Shield

1. Enable **AWS Shield Standard** for DDoS protection.
2. AWS Shield will automatically protect your application from layer 3 and layer 4 DDoS attacks.

## Security Groups

1. Configure security groups to allow only necessary traffic.
2. For EC2 instances:
   - Allow traffic from private load balancers only.
   - Restrict SSH access.

## IAM Roles

1. Create IAM roles with limited permissions for EC2 instances.
2. Attach roles to EC2 instances for secure access to other AWS services.

## Monitoring with AWS CloudWatch

1. Use **AWS CloudWatch** to monitor security logs.
2. Set up alarms for unusual traffic patterns or security incidents.
