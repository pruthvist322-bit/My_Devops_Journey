# Day 27 - AWS VPC Hands-on Lab

## Objective

Learn the fundamentals of AWS networking by creating a Virtual Private Cloud (VPC) with public and private subnets.

## Concepts Learned

* Virtual Private Cloud (VPC)
* Internet Gateway (IGW)
* Route Tables
* NAT Gateway
* Public Subnet
* Private Subnet

## Hands-on Implementation

### Step 1: Created a VPC

* CIDR Block: `10.0.0.0/24`

### Step 2: Created Two Subnets

* Public Subnet
* Private Subnet

Both subnets were assigned different CIDR ranges to avoid overlapping IP addresses.

### Step 3: Created Route Tables

* Public Route Table
* Private Route Table

Each subnet was associated with its respective route table.

### Step 4: Configured Routing

**Public Route Table**

* Added a route to the Internet Gateway (`0.0.0.0/0 → Internet Gateway`) to enable internet access.

**Private Route Table**

* Configured outbound internet access through a NAT Gateway so that instances in the private subnet can access the internet without being publicly accessible.

### Step 5: Created an Internet Gateway

* Attached the Internet Gateway to the VPC.
* Associated it with the public route table.

### Step 6: Launched an EC2 Instance

* Launched an EC2 instance in the public subnet.
* Assigned a public IP address.
* Successfully connected to the instance using SSH, confirming that the VPC networking was configured correctly.

## Architecture

```text
Internet
    │
Internet Gateway
    │
Public Route Table
    │
Public Subnet
    │
EC2 Instance
    │
NAT Gateway
    │
Private Route Table
    │
Private Subnet
```

## Outcome

Successfully built a basic AWS VPC environment with public and private networking components. This hands-on exercise helped me understand how VPCs, subnets, route tables, Internet Gateways, and NAT Gateways work together to provide secure and scalable network architecture in AWS.
