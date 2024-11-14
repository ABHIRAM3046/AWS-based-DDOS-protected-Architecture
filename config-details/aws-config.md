# AWS Service Configuration Guide

This guide provides step-by-step instructions for configuring AWS services using the AWS Management Console.

## Step 1: Set Up AWS WAF and Shield

1. Go to **AWS WAF & Shield** in the console.
2. Create a Web ACL and define rules to block unwanted traffic.
3. Enable AWS Shield Standard for DDoS protection.

## Step 2: Configure Route 53 (DNS)

1. In **Route 53**, set up a hosted zone.
2. Add a DNS record pointing to the public-facing load balancer.

## Step 3: Application Load Balancers

1. Create a **public-facing Application Load Balancer** for user-facing traffic.
2. Create a **private-facing Application Load Balancer** for internal communications.
3. Associate security groups with each load balancer.

## Step 4: Configure Auto Scaling Groups

1. Create an Auto Scaling group and link it to the load balancers.
2. Set scaling policies to handle variable traffic loads.

## Step 5: Launch EC2 Instances

1. Create an EC2 instance template to launch instances in the Auto Scaling group.
2. Ensure instances are placed in private subnets and only accessible through load balancers.

For security settings, refer to [Security Settings](security-settings.md).
