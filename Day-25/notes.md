# Day 25 – AWS Auto Scaling Groups (ASG)

## Overview

Today I learned one of the most important AWS services: **Auto Scaling**.

Auto Scaling automatically adds or removes EC2 instances based on application demand. It helps maintain application availability while optimizing infrastructure costs.

---

## What is Auto Scaling?

AWS Auto Scaling is a service that automatically adjusts the number of EC2 instances according to CPU utilization or other monitoring metrics.

It helps applications remain highly available without manual intervention.

---

## Why Auto Scaling is Used

- Automatically increases servers during high traffic.
- Removes unnecessary servers when traffic decreases.
- Improves High Availability.
- Optimizes infrastructure cost.
- Ensures better application performance.

---

## Hands-on Activity

For today's lab, I continued using the infrastructure created yesterday:

- Existing EC2 Instances
- Existing Target Group
- Existing Application Load Balancer (ALB)

---

## Step 1 – Start EC2 Instances

Started the previously created EC2 instances:

- One
- Two

Verified that both instances were in the **Running** state.

---

## Step 2 – Verify Target Group

- Opened **Target Groups**
- Verified that both EC2 instances were registered.
- Checked that the health status of both instances was **Healthy**.

---

## Step 3 – Verify Load Balancer

Opened the Application Load Balancer.

Checked the **Resource Map** to ensure:

- Load Balancer
- Listener
- Target Group
- EC2 Instances

were all connected successfully.

---

## Step 4 – Create Auto Scaling Group

Navigated to:

EC2 → Auto Scaling Groups → Create Auto Scaling Group

Provided:

- Auto Scaling Group Name

---

## Step 5 – Create Launch Template

Created a **Launch Template**.

The Launch Template stores all the instance configurations such as:

- Amazon Machine Image (AMI)
- Instance Type
- Key Pair
- Security Group
- Storage
- User Data

Every new EC2 instance created by the Auto Scaling Group uses this template.

---

## Step 6 – Select Availability Zones

Selected all required Availability Zones.

This improves High Availability.

---

## Step 7 – Attach Load Balancer

Selected:

Attach to an Existing Load Balancer

Chose the existing Target Group created earlier.

---

## Step 8 – Configure Group Size

Configured:

Desired Capacity : 1

Minimum Capacity : 1

Maximum Capacity : 4

---

## Step 9 – Configure Scaling Policy

Selected:

Target Tracking Scaling Policy

Metric Used:

Average CPU Utilization

Target CPU Utilization:

40%

---

## Step 10 – Create Auto Scaling Group

Reviewed all configurations and created the Auto Scaling Group.

---

## Step 11 – Verify Auto Scaling

Observed:

- A new EC2 instance was automatically launched by the Auto Scaling Group.
- The instance was automatically registered in the Target Group.
- The Application Load Balancer Resource Map showed the newly created instance.

---

## Step 12 – Generate Load

Connected to the newly created EC2 instance.

Installed stress tool.

Generated CPU load to increase CPU utilization.

Example:

Current CPU Utilization = 80%

Target CPU Utilization = 40%

Current Capacity = 2 Instances

As CPU utilization increased above the configured threshold, the Auto Scaling Group automatically launched additional EC2 instances.

When CPU utilization returned to normal, unnecessary instances were automatically terminated.

---

## Key Learning

AWS Auto Scaling continuously monitors application load and automatically launches or terminates EC2 instances based on demand.

When combined with an Application Load Balancer, it provides a highly available, scalable, and cost-efficient infrastructure.

---

**Day 25 Completed ✅**
