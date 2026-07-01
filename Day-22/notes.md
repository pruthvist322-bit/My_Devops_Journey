## Day 22 – AWS EC2 (Elastic Compute Cloud)

Today I learned about AWS EC2 service and explored how virtual servers are created and configured in AWS.

Topics Covered:

• What is EC2

Amazon EC2 (Elastic Compute Cloud) is a service provided by AWS to create and manage virtual servers in the cloud.

---

Types of EC2 Instances

Different instance families are available based on workloads:

* General Purpose
* Compute Optimized
* Memory Optimized
* Storage Optimized
* Accelerated Computing

Each type is selected based on performance requirements.

---

Name Tag

Name Tag is used to identify and organize AWS resources.

Example:
Dev-Server
Test-Server
Production-Server

Benefits:

* Easy identification
* Better resource management

---

AMI (Amazon Machine Image)

AMI is a template used to launch EC2 instances.

It contains:

* Operating System
* Application configuration
* Storage settings

Types of AMIs Learned:

1. Quick Start AMIs

* AWS provided images

2. AWS Marketplace AMIs

* Third-party provided images

3. Community AMIs

* Shared publicly by AWS users

---

Instance Type

Instance type defines:

* CPU
* Memory
* Storage
* Networking capacity

Examples:

* t2.micro
* t3.micro

---

Key Pair

Key Pair is used for secure access to EC2 instances.

Components:

* Public Key
* Private Key

Steps Learned:

* Create Key Pair
* Download key (.pem)
* Use key while connecting

---

Security Groups

Security Groups act as virtual firewalls.

Inbound Rules:

* Control incoming traffic

Outbound Rules:

* Control outgoing traffic

Learned:

* Creating Security Groups
* Applying Inbound Rules
* Applying Outbound Rules

---

Storage Configuration

Learned:

* Configuring storage
* Adding additional volumes
* Managing EC2 storage

---

User Data (Optional)

User Data allows running scripts automatically during instance launch.

Example:

* Install packages
* Configure server
* Execute startup tasks

---

Key Learning:

EC2 provides scalable virtual servers and understanding AMI, Security Groups, Storage, and Key Pairs is essential for deploying infrastructure in AWS.


