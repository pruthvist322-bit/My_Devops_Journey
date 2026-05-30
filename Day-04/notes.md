# Day 4 - Creating and Connecting to an AWS EC2 Instance

## Objective

Today I learned how to create an AWS EC2 Instance (Virtual Server) and connect to it using both:

- EC2 Instance Connect (Browser)
- SSH Client (Local Terminal)

---

## What is EC2?

EC2 (Elastic Compute Cloud) is a service provided by AWS that allows users to create and manage virtual servers in the cloud.

An EC2 Instance is simply a virtual machine running on AWS infrastructure.

---

# Step 1: Login to AWS

1. Open AWS Console
2. Enter the root email address
3. Enter the password
4. Login successfully

AWS Console Home Page will open.
<img width="1919" height="899" alt="Screenshot 2026-05-30 111442" src="https://github.com/user-attachments/assets/0c81bd30-e162-45e6-a69d-f108db5c55b3" />

---

# Step 2: Open EC2 Service

1. Search for EC2 in the AWS search bar
2. Click on EC2

EC2 Dashboard opens.

---

# Step 3: Launch an Instance

There are two ways:

## Method 1

Click:

Launch Instance

from the EC2 Dashboard.

## Method 2

Click:

Instances

from the left menu and then click:

Launch Instance

from the top-right corner.

Both methods open the Launch Instance page.

---

# Step 4: Configure the Instance

## Instance Name

Provide a name for the server.

Example:

MyServ1

---

## Select Operating System

Choose an AMI (Amazon Machine Image).

Example:

Amazon Linux 2023

---

## Instance Type

Select an instance type.

I selected:

t3.micro

Specifications:

- 2 vCPU
- 1 GiB Memory

---

# Step 5: Create a Key Pair

## What is a Key Pair?

A Key Pair is used for secure authentication while connecting to the EC2 instance.

It acts like a password but is much more secure.

---

## Creating Key Pair

1. Click Create New Key Pair
2. Enter Key Pair Name

Example:

MyServKey

3. Select:

PEM

format (used mainly for Linux)
<img width="1067" height="123" alt="Screenshot 2026-05-30 114050" src="https://github.com/user-attachments/assets/7c325bdf-6de8-44e0-bf3b-b9681cf9d13e" />

4. Click Create Key Pair

The .pem file gets downloaded automatically to your system.
---

# Step 6: Launch Instance

Keep the remaining settings as default.

Click:

Launch Instance

AWS starts creating the EC2 Instance.

---

# Step 7: View Instance Details

After launching:

1. Go to Instances
2. Select your Instance

You can see:

- Instance ID
- Public IP Address
- Private IP Address
- Instance State
<img width="1918" height="890" alt="Screenshot 2026-05-30 114354" src="https://github.com/user-attachments/assets/4875f276-0063-4722-abad-041076db08b5" />

---

# Step 8: Connect to Instance

Select the Instance and click:

Connect

You will see:

- EC2 Instance Connect
- SSM Session Manager
- SSH Client
- EC2 Serial Console

<img width="1908" height="833" alt="Screenshot 2026-05-30 120154" src="https://github.com/user-attachments/assets/d26d296a-6b8b-46d9-92b6-d48c5f455898" />

---

# Method 1: EC2 Instance Connect

1. Select EC2 Instance Connect
2. Click Connect

AWS opens a browser-based Linux terminal.

You can immediately start executing Linux commands.

Example:

ls
pwd

<img width="1919" height="865" alt="Screenshot 2026-05-30 115946" src="https://github.com/user-attachments/assets/0a989ddd-9b74-4504-9f70-91d5e0504a14" />


---

# Method 2: SSH Client

Open the SSH Client tab.

AWS provides a command similar to:

ssh -i "MyServKey.pem" ec2-user@Public-IP

Steps:

1. Open Terminal or PowerShell
2. Navigate to the folder containing the PEM file
3. Paste the SSH command
4. Press Enter

First-time connection message:

Are you sure you want to continue connecting (yes/no)?

Type:

yes

and press Enter.

Successfully connected to the Linux server.
<img width="1756" height="710" alt="Screenshot 2026-05-30 120628" src="https://github.com/user-attachments/assets/d4957f7a-85a3-4f7e-94f6-25d99155db65" />


---

# Key Concepts Learned

## Public IP

Used to connect from outside AWS.

## Private IP

Used for internal communication inside AWS.

## Instance ID

Unique identifier for every EC2 Instance.

## Key Pair

Used for secure login authentication.

---

# Key Takeaway

Today I successfully created my first AWS EC2 instance and connected to it using both the AWS browser terminal and SSH from my local machine.

This was my first hands-on experience managing a Linux server in the cloud.
