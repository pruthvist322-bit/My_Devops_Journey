# Day 17 – Linux Storage Partitioning & Mounting

Today I learned about **Storage Partitioning and Mounting in Linux** and how Linux manages disks and file systems.

## Understanding Storage in Linux

Storage devices (HDDs/SSDs/Volumes) are used to store data, and Linux provides tools to manage them efficiently.

### Understanding File Systems – ext4

I explored **ext4 (Fourth Extended Filesystem)**:

* Improved performance
* Supports large storage volumes
* Reliable journaling support
* Widely used default Linux filesystem

### Simple Analogy

* **Disk → Library Building**
* **Filesystem (ext4) → Library Management System**
* **Directories → Book Shelves**
* **Files → Books**
* **Inodes → Catalog Cards**
* **Data Blocks → Actual Pages of Books**

## Viewing Existing Storage

Used the following command to inspect available disks and partitions:

```bash
lsblk
```

Example output:

```bash
NAME      MAJ:MIN RM SIZE RO TYPE MOUNTPOINTS
xvda      202:0    0   8G  0 disk
├─xvda1   202:1    0   8G  0 part /
├─xvda127 259:0    0   1M  0 part
└─xvda128 259:1    0  10M  0 part /boot/efi
```

## Practical Exercise – Adding a New Volume in AWS

### Step 1: Attach New Volume

Created and attached a new EBS volume from AWS Console.

Verify:

```bash
lsblk
```

---

### Step 2: Partition the Disk

```bash
sudo fdisk /dev/xvdb
```

Actions inside fdisk:

* `n` → New partition
* `p` → Primary partition
* Enter → Default partition number
* Enter → Default first sector
* `+1G` → Create 1 GB partition
* `w` → Save and exit

Verify:

```bash
lsblk
```

---

### Step 3: Format Partition with ext4

```bash
sudo mkfs.ext4 /dev/xvdb1
```

---

### Step 4: Create Mount Point

```bash
sudo mkdir /mnt/newdisk
```

---

### Step 5: Mount the Partition

```bash
sudo mount /dev/xvdb1 /mnt/newdisk
```

Verify:

```bash
df -h
```

## Key Takeaways

- Learned storage architecture in Linux
- Understood ext4 filesystem
- Practiced disk partitioning using fdisk
- Formatted storage and mounted partitions
- Attached and managed AWS storage volumes

