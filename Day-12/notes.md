# Day 12 - Linux Process Management, Links, wget & curl

## Overview

Today I learned about Linux process management, system information commands, file links, and tools used for downloading files and interacting with web servers.

---

## 1. System Information Commands

### Check Operating System Information

```bash
uname
```

Displays the operating system name.

```bash
uname -a
```

Displays complete system information including kernel version, architecture, hostname, and more.

### Check Logged-in Users

```bash
who
```

Shows all users currently logged into the system.

```bash
whoami
```

Displays the current logged-in user.

---

## 2. Process Management

### List Running Processes

```bash
ps
```

Displays processes running in the current session.

```bash
ps -ef
```

Displays all running processes in the system.

### Check Specific Process

```bash
ps -ef | grep "process_name"
```

Checks whether a specific process is running.

### View Resource Usage

```bash
top
```

Displays real-time system processes and resource usage.

```bash
top &
```

Runs the top command in the background.

### Kill a Process

```bash
kill -9 <PID>
```

Forcefully terminates a process.

Common Signals:

* SIGKILL (9) → Immediate forceful termination
* SIGTERM (15) → Graceful termination (default)

### View User-Specific Processes

```bash
ps -u username
```

Displays all processes owned by a specific user.

### CPU Information

```bash
lscpu
```

Displays detailed CPU architecture information.

---

## 3. Linux Links

A link acts as a shortcut to a file.

### Types of Links

1. Soft Link (Symbolic Link)
2. Hard Link

### Soft Link

```bash
ln -s /path/to/file linkname
```

Characteristics:

* Works like a shortcut.
* Changes in source file are reflected in the link.
* If source file is deleted, the soft link becomes invalid.

### Hard Link

```bash
ln /path/to/file linkname
```

Characteristics:

* Points directly to the inode of the file.
* Changes are reflected in both files.
* Continues to work even if the original file is deleted.

### Inode Information

```bash
ls -i
```

Displays inode numbers.

```bash
stat filename
```

Displays detailed file metadata including inode information.

---

## 4. wget Command

Used to download files from the internet.

### Download a File

```bash
wget https://example.com/file.txt
```

### Save with Different Name

```bash
wget -O newfile.txt https://example.com/file.txt
```

---

## 5. curl Command

A powerful tool used to transfer data between systems and interact with APIs.

### Fetch Webpage Content

```bash
curl www.google.com
```

### Send POST Request

```bash
curl -X POST -d "param1=value1&param2=value2" https://api.example.com/submit
```

### Send Request with Authorization Header

```bash
curl -H "Authorization: Bearer your_token" https://api.example.com/data
```

---

## Key Takeaways

* Learned how Linux manages processes and system resources.
* Understood the difference between soft links and hard links.
* Learned about inode numbers and file metadata.
* Explored wget for downloading files.
* Explored curl for communicating with web servers and APIs.

Day 12 completed successfully. 🚀

