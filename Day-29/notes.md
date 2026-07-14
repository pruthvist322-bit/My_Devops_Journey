# Day 29 – AWS Monitoring using CloudWatch & SNS

## Overview

Today I learned one of the most important concepts in AWS: **Monitoring** using **Amazon CloudWatch** and **Amazon SNS (Simple Notification Service)**.

Monitoring helps us continuously track the health and performance of AWS resources. I also learned how to configure alerts that notify us whenever a resource crosses a specified threshold.

---

## What is Monitoring?

Monitoring is the process of observing the performance and health of AWS resources such as EC2 instances. It helps identify issues early and ensures applications are running efficiently.

---

## AWS Services Used

- Amazon CloudWatch
- Amazon SNS (Simple Notification Service)
- Amazon EC2

---

## Hands-on Activity

### Step 1: Create an SNS Topic

First, I created an SNS Topic, which is used to send notifications.

SNS supports multiple subscription types such as:
- Email
- SMS (Mobile Number)
- AWS Lambda
- HTTP/HTTPS Endpoints

---

### Step 2: Create a Subscription

Added an **Email Subscription** to the SNS Topic.

AWS sent a confirmation email, and I confirmed the subscription by clicking the confirmation link.

---

### Step 3: Create a CloudWatch Alarm

Navigated to **CloudWatch → Alarms** and created a new alarm.

Selected the EC2 instance metric:

- CPU Utilization

---

### Step 4: Configure the Alarm

Configured the alarm with the following settings:

- Metric: CPU Utilization
- Threshold: Greater than 80%
- Action: Send notification to the SNS Topic

---

### Step 5: Test the Alarm

Started the EC2 instance and generated CPU load using a stress tool.

Once the CPU utilization exceeded **80%**, the CloudWatch alarm changed to the **ALARM** state.

An email notification was successfully sent to the subscribed email address through SNS.

---

## What I Learned

- What is AWS Monitoring
- Why Monitoring is important
- What is Amazon CloudWatch
- What is Amazon SNS
- How to create an SNS Topic
- How to add an Email Subscription
- How to confirm an SNS Subscription
- How to create a CloudWatch Alarm
- How to monitor EC2 CPU Utilization
- How to configure alarm thresholds
- How CloudWatch and SNS work together to send notifications

---

## Key Takeaway

CloudWatch continuously monitors AWS resources, while SNS sends instant notifications whenever a configured threshold is exceeded. Together, they provide an effective monitoring and alerting solution for cloud infrastructure.

---

