# Day 30 – AWS Lambda

## Overview

Today I learned about one of the important AWS serverless services: **AWS Lambda**.

AWS Lambda allows us to run code without managing or provisioning servers.

---

## What is AWS Lambda?

AWS Lambda is a serverless, event-driven compute service that runs code in response to events.

With Lambda, we can run our code without directly managing EC2 servers.

AWS automatically manages the required infrastructure and executes the code when it is triggered.

---

## How to Create a Lambda Function

Learned the steps to create a Lambda Function:

1. Opened the AWS Lambda service.
2. Clicked on **Create Function**.
3. Selected **Author from Scratch**.
4. Provided a Function Name.
5. Selected the required Runtime.
6. Configured the required permissions and execution role.
7. Created the Lambda Function.

---

## Adding Code to Lambda

Learned how to add code directly inside the Lambda Function code editor.

The Lambda function code is executed whenever the function is triggered.

---

## Testing a Lambda Function

After adding the code:

1. Created a Test Event.
2. Selected the required event configuration.
3. Invoked the Lambda Function.
4. Checked the execution result and response.

This helped me understand how Lambda code is tested and executed.

---

## How to Trigger a Lambda Function

A Lambda Function can be triggered by different AWS services or events.

Learned how Lambda functions can be triggered using events.

The Lambda function executes automatically when the configured event occurs.

---

## Lambda Permissions and IAM Roles

Learned how to provide permissions to Lambda using **IAM Roles**.

The execution role allows the Lambda Function to access other AWS services based on the permissions attached to the role.

---

## Difference Between EC2 and Lambda

### EC2

- Server-based compute service
- Requires server management
- User manages the operating system
- Runs continuously until stopped
- Billing is based on instance usage

### Lambda

- Serverless compute service
- No server management required
- AWS manages the infrastructure
- Runs only when triggered
- Billing is based on requests and execution duration

---

## Lambda Billing

Learned that AWS Lambda billing is based on:

- Number of requests
- Duration of code execution

Lambda is cost-effective because we pay based on usage rather than running a server continuously.

---

## What I Learned

- What is AWS Lambda
- How to create a Lambda Function
- How to add code to a Lambda Function
- How to test a Lambda Function
- How to trigger a Lambda Function
- How to provide permissions using IAM Roles
- Difference between EC2 and Lambda
- How AWS Lambda billing works

---

## Key Takeaway

AWS Lambda is a powerful serverless service that allows us to run code without managing servers. It is useful for event-driven applications and helps reduce infrastructure management and operational overhead.

---
