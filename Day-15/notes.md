# Day 15 - Linux Networking Utilities, Firewall & Time Synchronization

## Objective

Today I learned Linux networking tools, firewall management, text utilities, and system time synchronization.

These concepts are important for server administration, monitoring, and maintaining reliable production environments.

---

# 1. netstat

`netstat` is used to display network connections, routing tables, interface statistics, and active ports.

## Show All Network Connections

```bash
netstat -a
```

States:

* LISTEN → Waiting for incoming connections
* ESTABLISHED → Active communication between systems

---

## Show Listening Ports

```bash
netstat -l
```

Displays ports waiting for incoming traffic.

---

## Show Protocol Statistics

```bash
netstat -s
```

Displays statistics grouped by protocol.

---

# 2. iptables (Linux Firewall)

`iptables` is used to control incoming and outgoing network traffic.

## Install iptables

RHEL / Amazon Linux:

```bash
sudo yum install iptables
```

Ubuntu:

```bash
sudo apt install iptables
```

---

## View Available Options

```bash
iptables -h
```

---

## View Existing Rules

```bash
sudo iptables -L -v
```

---

## Block Traffic from Specific IP

```bash
sudo iptables -A INPUT -s 192.168.1.20 -j DROP
```

---

## Allow HTTP Traffic

```bash
sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT
```

---

## Remove Rule

```bash
sudo iptables -D INPUT 1
```

(Removes rule at position 1)

---

# 3. File Viewing Utilities

## more

Displays content page by page.

```bash
more /etc/passwd
```

---

## less

Allows forward and backward navigation.

```bash
less /etc/passwd
```

---

# 4. Sorting & Filtering

## sort

Sort content alphabetically.

```bash
sort users.txt
```

---

## uniq

Remove duplicate lines.

```bash
sort users.txt | uniq
```

---

# 5. Calendar & System Status

## Display Calendar

```bash
cal
```

Show a specific year:

```bash
cal 2027
```

---

## Check Server Uptime

```bash
uptime
```

Displays how long the system has been running.

---

# 6. xargs

Used to pass command output as input arguments.

Example:

```bash
ls | xargs rm
```

(Use carefully)

---

# 7. Time Synchronization (NTP)

Accurate system time is critical for:

* Log analysis
* Production applications
* Database consistency
* Distributed systems

---

## Show Date

```bash
date
```

---

## View Time Settings

```bash
timedatectl
```

---

## View Available Time Zones

```bash
timedatectl list-timezones
```

---

## Set Time Zone

```bash
timedatectl set-timezone Asia/Kolkata
```

---

## Set Date & Time

```bash
timedatectl set-time "2025-01-10 18:30:00"
```

---

## Enable NTP Sync

```bash
timedatectl set-ntp true
```

---

# 8. chronyd

Purpose:
Time synchronization service.

Important Paths:

Configuration:

```bash
/etc/chrony.conf
```

Logs:

```bash
/var/log/chrony
```

Manage Service:

```bash
sudo systemctl restart chronyd
```

---

# Key Takeaways

Today I learned:

* Monitoring connections using netstat
* Managing firewall rules using iptables
* Viewing and filtering files
* Working with calendars and uptime
* Understanding time synchronization using NTP and chronyd

These concepts are essential for Linux administration and DevOps environments.
