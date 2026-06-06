# Day 9 - Linux User and Group Management

## Objective

Today I learned how Linux users and groups are managed, how to create and delete users, assign passwords, modify user properties, and understand password policies.

---

# Creating Users

## Create a User

```bash
sudo useradd username
```

Creates a new user account.

---

## Create User with Home Directory

```bash
sudo useradd -m -s /bin/bash username
```

Options:

* `-m` → Creates a home directory
* `-s` → Specifies the login shell

---

## Alternative Method

```bash
sudo adduser username
```

Creates:

* User
* Home Directory
* Default Settings

---

# Viewing Users

Linux stores user information in:

```bash
cat /etc/passwd
```

To view all users:

```bash
sudo cat /etc/passwd
```

---

## Display Only Usernames

```bash
cut -d: -f1 /etc/passwd
```

This displays only the usernames.

---

# Groups in Linux

When a user is created, a group with the same name is usually created automatically.

To view groups:

```bash
sudo cat /etc/group
```

---

## Display Only Group Names

```bash
cut -d: -f1 /etc/group
```

---

# Setting Passwords

To assign a password:

```bash
sudo passwd username
```

The system prompts for the password twice.

Passwords are stored in encrypted form.

---

# Login to Another User

Using SSH:

```bash
ssh username@public-ip-address
```

Example:

```bash
ssh devuser@13.233.xxx.xxx
```

---

# Enable Password Authentication

By default, password authentication may be disabled.

Edit SSH configuration:

```bash
sudo vi /etc/ssh/sshd_config
```

Find:

```text
PasswordAuthentication no
```

Change to:

```text
PasswordAuthentication yes
```

Save and exit.

---

# Restart SSH Service

After modifying SSH configuration:

```bash
sudo service sshd restart
```

This step is mandatory for changes to take effect.

---

# Delete Users

```bash
sudo userdel username
```

Deletes a user.

---

# Group Management

## Create Group

```bash
sudo groupadd groupname
```

---

## Delete Group

```bash
sudo groupdel groupname
```

---

# Modify Username

```bash
sudo usermod -l new_username old_username
```

Example:

```bash
sudo usermod -l devopsuser testuser
```

---

# Change User Shell

```bash
sudo chsh -s /bin/bash username
```

Changes the default shell.

---

# Password Policies

View password configuration:

```bash
sudo vi /etc/login.defs
```

Important Parameters:

```text
PASS_MAX_DAYS 90
PASS_MIN_DAYS 0
PASS_WARN_AGE 7
```

### Meaning

* PASS_MAX_DAYS → Password expires after 90 days
* PASS_MIN_DAYS → Minimum days before changing password again
* PASS_WARN_AGE → Warn user 7 days before password expiry

---

# Key Takeaway

Today I learned:

* Creating and deleting users
* Creating and deleting groups
* Setting user passwords
* Understanding SSH user login
* Modifying usernames
* Changing user shells
* Viewing Linux user and group databases
* Understanding password expiration policies

These concepts are fundamental for Linux Administration, Security, and DevOps practices.
