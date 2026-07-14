# Day 28 – AWS S3 (Simple Storage Service) & CloudFront (CDN)

## Overview

Today I learned about **Amazon S3 (Simple Storage Service)**, one of the most widely used storage services in AWS. I also explored **Amazon CloudFront (CDN)** and learned how it improves the performance of static websites.

---

## What is Amazon S3?

Amazon S3 (Simple Storage Service) is an object storage service provided by AWS that allows users to securely store and retrieve data from anywhere over the internet.

It is highly durable, scalable, secure, and cost-effective.

---

## Objects That Can Be Stored in S3

Amazon S3 can store almost any type of file, including:

- Images
- Videos
- Audio Files
- PDF Documents
- ZIP Files
- Backup Files
- Log Files
- Website Files (HTML, CSS, JavaScript)
- Application Data

---

## S3 Permissions

Learned different ways to manage access to S3 buckets:

- Bucket Policies
- IAM Policies
- ACL (Access Control Lists)
- Public Access Block Settings

These permissions help control who can view or modify bucket contents.

---

## S3 Properties

Some important properties of Amazon S3 include:

- Versioning
- Static Website Hosting
- Server-side Encryption
- Lifecycle Rules
- Event Notifications
- Logging
- Object Lock
- Tags

---

## S3 Lifecycle

The S3 Lifecycle feature helps automatically manage objects throughout their lifecycle.

Examples:

- Move objects to cheaper storage classes
- Archive old files
- Automatically delete unnecessary files after a specific period

This helps optimize storage costs.

---

## Creating an S3 Bucket

Steps performed:

- Opened Amazon S3
- Clicked **Create Bucket**
- Entered a globally unique bucket name
- Selected AWS Region
- Configured bucket settings
- Created the bucket successfully

---

## Uploading Files and Folders

Learned how to upload:

- Individual files
- Multiple files
- Entire folders

into an S3 bucket.

---

## Hosting a Static Website

Configured an S3 bucket to host a static website.

Steps:

- Enabled Static Website Hosting
- Uploaded HTML, CSS, and JavaScript files
- Configured the Index Document
- Generated the Website Endpoint URL

Successfully accessed the hosted website through the S3 endpoint.

---

## Bucket Permissions for Static Website

To make the website publicly accessible:

- Disabled Block Public Access
- Added Bucket Policy
- Allowed public read access for website files

This enabled users to access the hosted website through the browser.

---

## Amazon CloudFront (CDN)

Learned about Content Delivery Networks (CDN).

A CDN stores copies of website content at multiple edge locations worldwide so users receive content from the nearest location.

This significantly improves website performance and reduces latency.

---

## Creating a CloudFront Distribution

Created a CloudFront Distribution by:

- Selecting the S3 Bucket as the Origin
- Configuring default settings
- Creating the Distribution
- Using the generated CloudFront Domain Name

Accessed the website using the CloudFront URL and observed improved response time.

---

## Advantages of Amazon S3

- Highly Durable
- Highly Scalable
- Cost Effective
- Easy Static Website Hosting
- Secure Storage
- Supports Lifecycle Management
- Integrates with Multiple AWS Services

---

## Advantages of CloudFront (CDN)

- Faster Content Delivery
- Reduced Latency
- Improved Website Performance
- Global Edge Locations
- Better User Experience
- Enhanced Security

---

## Key Learning

Amazon S3 is an excellent service for storing and hosting static website content, while Amazon CloudFront improves website performance by delivering content through global edge locations.

Together, S3 and CloudFront provide a secure, scalable, and high-performance solution for static web hosting.

---

**Day 28 Completed ✅**
