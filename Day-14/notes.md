# Day 14 - Linux Networking Basics

## Objective

Today I learned networking fundamentals and commands used to test connectivity, inspect ports, analyze traffic, and troubleshoot DNS.

Networking plays a major role in Linux administration, cloud environments, and DevOps workflows.

---

# 1. Ping Command

Ping is used to check whether a server or host is reachable over the network.

## Syntax

```bash
ping <IP-address>
```

Example:

```bash
ping 8.8.8.8
```

Purpose:

* Verify connectivity
* Check whether a server is responding
* Measure response time

---

# 2. lsof (List Open Files)

Linux treats many resources as files, including network ports.

Used to identify which process is using a port.

## Syntax

```bash
sudo lsof -i :<port>
```

Example:

```bash
sudo lsof -i :443
```

Shows the process using HTTPS port.

---

# 3. tcpdump

tcpdump is a packet analysis tool used to capture and inspect network traffic.

Useful for:

* Troubleshooting network issues
* Monitoring packets
* Analyzing requests

## List Interfaces

```bash
sudo tcpdump -D
```

Displays available network interfaces.

---

## Monitor Traffic on Port

```bash
sudo tcpdump port 22
```

Captures SSH traffic.

---

## Monitor Traffic for Specific Host

```bash
sudo tcpdump host 8.8.8.8
```

Displays packets to/from that IP.

---

# 4. Telnet

Telnet is an older remote communication protocol.

Today it is mainly used to test connectivity to a remote port.

Default Port:

```text
23
```

## Syntax

```bash
telnet hostname port
```

Example:

```bash
telnet github.com 443
```

Purpose:

* Test whether a service is reachable
* Validate port accessibility

---

# 5. nslookup (Name Server Lookup)

Used to query DNS information.

Helps convert:

* Domain → IP
* IP → Domain

## Syntax

```bash
nslookup domain-name
```

Example:

```bash
nslookup openai.com
```

Useful for DNS troubleshooting.

---

# 6. dig Command

dig provides detailed DNS information.

## Syntax

```bash
dig domain-name
```

Example:

```bash
dig github.com
```

Useful for:

* DNS debugging
* Viewing records
* Checking domain resolution

---

# Difference Between nslookup and dig

| nslookup            | dig                 |
| ------------------- | ------------------- |
| Basic DNS lookup    | Detailed DNS output |
| Easy to use         | More advanced       |
| Limited information | Rich debugging data |

---

# Key Takeaways

Today I learned:

* Testing connectivity using ping
* Checking active ports using lsof
* Capturing packets using tcpdump
* Testing services using telnet
* DNS troubleshooting using nslookup
* Detailed DNS analysis using dig

Networking is one of the core foundations of DevOps and cloud infrastructure.
