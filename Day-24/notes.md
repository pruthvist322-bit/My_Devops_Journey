## Day 24 – AWS Elastic Load Balancer (ELB)

Today I learned one of the most important services in AWS: **Elastic Load Balancer (ELB)**.

A Load Balancer automatically distributes incoming traffic across multiple EC2 instances, improving application availability, scalability, and fault tolerance.

---

### What is a Load Balancer?

A Load Balancer is an AWS service that distributes incoming client requests across multiple servers (EC2 instances), ensuring that no single server becomes overloaded.

---

### Why is a Load Balancer Used?

* Distributes incoming traffic across multiple servers
* Improves application availability
* Prevents a single server from being overloaded
* Provides high availability and fault tolerance
* Automatically routes traffic only to healthy instances

---

### Types of Load Balancers

**1. Application Load Balancer (ALB)**

* Works at Layer 7 (HTTP/HTTPS)
* Used for web applications
* Supports path-based and host-based routing

**2. Network Load Balancer (NLB)**

* Works at Layer 4 (TCP/UDP)
* Designed for high-performance and low-latency applications

**3. Gateway Load Balancer (GWLB)**

* Used for deploying and managing virtual network appliances such as firewalls and intrusion detection systems

**4. Classic Load Balancer (CLB)**

* Legacy load balancer
* Supports basic Layer 4 and Layer 7 load balancing

---

### Hands-on Activity

#### Step 1: Created Two EC2 Instances

Instance Names:

* One
* Two

Configured HTTP (Port 80) in the Security Group.

---

#### Step 2: Installed Apache (httpd)

```bash
sudo yum install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
```

---

#### Step 3: Created Different Web Pages

Server One:

```bash
echo "<h1>Hey I am Goodieee..</h1>" | sudo tee /var/www/html/index.html
```

Server Two:

```bash
echo "<h1>Hey I am Baddiee..</h1>" | sudo tee /var/www/html/index.html
```

---

#### Step 4: Created a Target Group

* Created a Target Group
* Registered both EC2 instances
* Configured health checks

The Target Group determines which EC2 instances receive traffic from the Load Balancer.

---

#### Step 5: Created an Application Load Balancer (ALB)

* Selected Internet-facing Load Balancer
* Added Listener (HTTP – Port 80)
* Attached the Target Group
* Completed the configuration

---

#### Step 6: Verified the Load Balancer

Used the DNS Name provided by the ALB.

Observed requests being distributed between both EC2 instances, confirming that the Application Load Balancer was working successfully.

---

### Key Learning

Elastic Load Balancer is an essential AWS service that improves scalability, availability, and reliability by distributing incoming traffic across multiple EC2 instances.

Day 24 Completed ✅
