# Scaling and Load Balancing Configuration

This guide provides instructions for setting up Auto Scaling and Load Balancing.

## Step 1: Create Load Balancers

1. Create a **public-facing Application Load Balancer** to handle incoming traffic.
   - Configure health checks to ensure traffic is routed to healthy instances.
2. Set up a **private-facing Application Load Balancer** for backend traffic.

## Step 2: Configure Auto Scaling Groups

1. In the **Auto Scaling** console, create a new Auto Scaling group.
2. Attach the group to the load balancers.
3. Define scaling policies based on metrics such as CPU utilization.

## Step 3: Scaling Policies

- Configure a target tracking policy to automatically adjust the number of instances.
- Set minimum and maximum instance limits based on expected load.

## Step 4: CloudWatch Alarms for Scaling

- Create CloudWatch alarms to trigger scaling events.
- Example: Increase the instance count if CPU utilization exceeds 75%.
