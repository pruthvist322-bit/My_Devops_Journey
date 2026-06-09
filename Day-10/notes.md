# Day 10 - Passwordless SSH Authentication Between Linux Servers

## Objective

Today I learned how to establish a passwordless SSH connection between two Linux servers using SSH public and private key authentication.

This method is commonly used in DevOps automation, Ansible, CI/CD pipelines, and server administration.

---

# Understanding the Setup

I created two AWS EC2 instances:

1. Host Server
2. Target Server

Goal:

- Connect from Host Server to Target Server
- Avoid entering passwords every time
- Use SSH key-based authentication

---

# Step 1: Change Hostnames

To avoid confusion between servers, I changed the hostname of each server.

### Host Server

```bash
sudo hostnamectl set-hostname hostserver
```

### Target Server

```bash
sudo hostnamectl set-hostname targetserver
```

After changing the hostname:

```bash
exit
```

Logout and login again to see the updated hostname.

---

# Step 2: Generate SSH Keys on Host Server

Login to the Host Server and generate an SSH key pair.

```bash
ssh-keygen -t rsa
```

Press Enter for all prompts.

This creates:

```text
id_rsa       -> Private Key
id_rsa.pub   -> Public Key
```

Location:

```bash
~/.ssh/
```

Verify:

```bash
cd ~/.ssh
ll
```

---

# Step 3: View Public Key

Display the public key:

```bash
cat id_rsa.pub
```

Copy the entire output.

---

# Step 4: Add Public Key to Target Server

Login to the Target Server.

Move to:

```bash
cd ~/.ssh
```

Open:

```bash
vi authorized_keys
```

Paste the copied public key.

OR append it using:

```bash
echo "public_key_content" >> authorized_keys
```

Save and exit.

---

# Understanding authorized_keys

The file:

```text
~/.ssh/authorized_keys
```

contains the list of public keys that are allowed to access the server.

If a matching private key exists on another server, SSH login will happen automatically.

---

# Step 5: Connect Without Password

From Host Server:

```bash
ssh ec2-user@<Target-Server-Public-IP>
```

Example:

```bash
ssh ec2-user@13.xx.xx.xx
```

Result:

- No password prompt
- Successful login to Target Server

---

# Files Involved

| File | Purpose |
|--------|---------|
| id_rsa | Private Key |
| id_rsa.pub | Public Key |
| authorized_keys | Stores allowed public keys |

---

# Key Takeaway

Today I learned:

- What SSH key authentication is
- Difference between Public and Private Keys
- How to generate SSH keys
- How authorized_keys works
- How to establish passwordless SSH communication between servers

