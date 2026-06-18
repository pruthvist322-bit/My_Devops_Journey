## Day 16 – NFS (Network File System) Setup in AWS EC2
Overview

Today I learned how to configure NFS (Network File System) in Linux using AWS EC2 instances.

NFS allows multiple servers to access and share files over a network as if they were stored locally.

Architecture Used
- 1 NFS Server (shared storage)
- 2 NFS Clients (access shared storage)
- Amazon Linux EC2 Instances
- Same VPC and Security Group
- Opened Port 2049 for NFS communication

### Step 1: Configure NFS Server
##### Connect to EC2 Server
sudo hostnamectl set-hostname NFS-SERVER
#### Install NFS Packages

Amazon Linux:
sudo yum update -y
sudo yum install -y nfs-utils

Ubuntu:
sudo apt update -y
sudo apt install -y nfs-common nfs-kernel-server

#### Create Shared Directory:
sudo mkdir /nfs_share
sudo chown -R nobody:nobody /nfs_share
sudo chmod 777 /nfs_share
Configure Export File
sudo vi /etc/exports

#### Add:
/nfs_share *(rw,sync,no_root_squash)

#### Options:
rw → Read/Write access
sync → Immediate disk writes
no_root_squash → Allows root access (use carefully)
Start NFS Service
sudo systemctl enable nfs-server
sudo systemctl start nfs-server

#### Export the folder:
sudo exportfs -rav

#### Verify:
sudo systemctl status nfs-server

### Step 2: Configure NFS Client
#### Set hostname:
sudo hostnamectl set-hostname NFS-CLIENT

#### Install package:
sudo yum update -y
sudo yum install -y nfs-utils

#### Create Mount Directory
sudo mkdir /mnt/nfs_mount
#### Mount Shared Folder
sudo mount <NFS-SERVER-IP>:/nfs_share /mnt/nfs_mount

#### Verify:

df -h
ls /mnt/nfs_mount

#### What I Learned
- What NFS is and why shared storage is used
- Difference between Server and Client configuration
- Exporting directories using /etc/exports
- Mounting remote storage
- Verifying mounts using df -h
- Importance of Security Group rules (Port 2049)
