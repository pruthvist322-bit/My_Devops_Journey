## Day 23 – AWS EC2 Advanced Concepts

Today I continued learning AWS EC2 and explored advanced concepts related to EC2 pricing models, Amazon Machine Images (AMI), and Snapshots.

Topics Covered:

• Spot Instances

Spot Instances allow users to use AWS's unused EC2 capacity at a significantly lower price than On-Demand instances.

Advantages:

* Cost-effective
* Suitable for fault-tolerant workloads
* Ideal for testing, batch processing, and data analysis

Limitation:

* AWS can terminate the instance if the capacity is required.

---

• Savings Plans

Savings Plans help reduce AWS compute costs by committing to a consistent amount of usage for 1 or 3 years.

Benefits:

* Lower pricing than On-Demand
* Flexible across instance families and regions
* Best for predictable workloads

---

• Reserved Instances

Reserved Instances provide discounted pricing in exchange for committing to a specific instance type for 1 or 3 years.

Benefits:

* Significant cost savings
* Suitable for applications that run continuously
* Reserved capacity for long-term workloads

---

• Dedicated Hosts

Dedicated Hosts are physical servers dedicated to a single AWS customer.

Why they are used:

* Meet compliance requirements
* License-specific software
* Complete control over host placement
* Isolation from other AWS customers

---

• Amazon Machine Image (AMI)

AMI is a preconfigured template used to launch EC2 instances.

It contains:

* Operating System
* Software Packages
* Application Configuration
* Storage Configuration

---

• Creating an AMI

Learned how to:

* Select an existing EC2 instance
* Create an Image (AMI)
* Configure image settings
* Save the AMI for future use

---

• Launching an EC2 Instance using an AMI

Steps Learned:

* Select My AMIs
* Choose the required AMI
* Configure instance settings
* Launch the EC2 instance

---

• Snapshot

A Snapshot is a backup of an Amazon EBS volume.

Benefits:

* Backup and recovery
* Disaster recovery
* Restore data quickly
* Create new volumes from snapshots

---

Key Learning:

Understanding EC2 pricing models, AMIs, and Snapshots helps optimize cloud costs while improving infrastructure management and disaster recovery strategies.
