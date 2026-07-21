# Day 31 – AWS CLI (Command Line Interface)

## Overview

Today I learned one of the most important tools in AWS: **AWS Command Line Interface (AWS CLI)**.

AWS CLI allows us to interact with AWS services directly from the terminal using commands, making it easier to automate tasks and manage AWS resources efficiently.

---

## What is AWS CLI?

AWS Command Line Interface (AWS CLI) is a command-line tool that enables users to create, manage, and configure AWS resources using commands instead of the AWS Management Console.

It helps automate repetitive tasks and is widely used by DevOps Engineers and Cloud Engineers.

---

## Why AWS CLI is Used

- Automate AWS tasks
- Manage AWS resources from the terminal
- Reduce manual work
- Integrate with Shell Scripts
- Faster than using the AWS Management Console
- Useful for Infrastructure Automation

---

## Installing AWS CLI

### On Linux

1. Download the AWS CLI package.
2. Extract the package.
3. Run the installation script.
4. Verify the installation.

Example:

```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
aws --version
```

---

### On Windows

1. Download the AWS CLI Installer from the AWS website.
2. Run the installer.
3. Complete the installation.
4. Open Command Prompt or PowerShell.
5. Verify the installation.

Example:

```bash
aws --version
```

---

## Configuring AWS CLI

Configured AWS CLI using:

```bash
aws configure
```

It asks for:

- AWS Access Key ID
- AWS Secret Access Key
- Default Region
- Output Format (json, text, table)

---

## AWS CLI Commands

Learned how to use AWS CLI commands to manage AWS resources.

Examples:

List S3 Buckets

```bash
aws s3 ls
```

List EC2 Instances

```bash
aws ec2 describe-instances
```

Create an S3 Bucket

```bash
aws s3 mb s3://bucket-name
```

Copy Files to S3

```bash
aws s3 cp file.txt s3://bucket-name/
```

---

## Backup Using AWS CLI

Learned how to create backups using AWS CLI by uploading files and folders to Amazon S3.

AWS CLI makes backup operations simple and efficient.

---

## Hands-on Activity

- Installed AWS CLI
- Configured AWS CLI using Access Keys
- Verified AWS CLI installation
- Executed multiple AWS CLI commands
- Created and managed AWS resources using commands
- Performed backup operations using AWS CLI

---

## What I Learned

- What is AWS CLI
- Why AWS CLI is used
- Steps to install AWS CLI on Linux
- Steps to install AWS CLI on Windows
- How to configure AWS CLI
- How to create AWS resources using CLI commands
- How to perform backups using AWS CLI
- Hands-on practice with AWS CLI commands

---

## Key Takeaway

AWS CLI is one of the most powerful tools for managing AWS resources. It enables automation, simplifies resource management, and is an essential skill for every DevOps Engineer.

---

