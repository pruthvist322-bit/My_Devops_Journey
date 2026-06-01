# Day 5 - Linux Basic Commands

## Objective

Today I learned some fundamental Linux commands that are used daily by Linux administrators, Cloud Engineers, and DevOps Engineers.

Since most DevOps tools and servers run on Linux, understanding these commands is very important.

---

# Screen Management

## clear

Used to clear the terminal screen.

```bash
clear
```

---

# File and Directory Listing

## ls

Used to list files and directories.

```bash
ls
```

## pwd

Used to display the current working directory.

```bash
pwd
```

Example Output:

```bash
/home/ec2-user
```

---

# File Creation

## touch

Used to create a file.

```bash
touch file.txt
```

### Creating Multiple Files

```bash
touch one.txt two.java three.pdf
```

This creates multiple files at once.

---

# Different Types of Listings

## ll

Long listing format.

```bash
ll
```

Displays:

* Permissions
* Owner
* Size
* Date
* File Name

---

## ls -al

Shows all files including hidden files.

```bash
ls -al
```

---

## ls -lt

Lists files based on modification time.

```bash
ls -lt
```

Newest files appear first.

---

## ls -lrt

Lists files in reverse time order.

```bash
ls -lrt
```

Oldest files appear first.

---

# Directory Creation

## mkdir

Used to create a directory.

```bash
mkdir folder1
```

### Creating Multiple Directories

```bash
mkdir onefolder twofolder threefolder
```

---

## Nested Directory Creation

```bash
mkdir -p zoo/animals/birds
```

Creates all parent directories automatically.

---

# Viewing Directory Structure

## tree

Used to display folders and files in a tree structure.

```bash
tree
```

If not installed:

```bash
sudo dnf install tree -y
```

---

# Changing Directories

## cd

Move into a directory.

```bash
cd foldername
```

---

## Move One Directory Back

```bash
cd ..
```

---

## Move Two Directories Back

```bash
cd ../..
```

---

# File Editing

Linux provides editors like:

* vi
* nano

I learned and preferred using the vi editor.

---

## Open File in vi

```bash
vi filename.txt
```

---

## Insert Mode

Press:

```text
i
```

to start inserting content.

---

## Exit Without Saving

Press:

```text
Esc
:q!
```

---

## Save and Exit

Press:

```text
Esc
:wq!
```

Meaning:

* w = write
* q = quit

---

# Viewing File Content

## cat

Displays file content.

```bash
cat filename.txt
```

---

# Line Numbers in vi

```text
:set number
```

Displays line numbers.

---

# Delete Operations in vi

## Delete Current Line

```text
dd
```

---

## Delete Entire File Content

```text
:%d
```

---

# Command History

## history

Displays previously executed commands.

```bash
history
```

---

# Key Takeaway

Today I learned essential Linux commands related to:

* File Management
* Directory Management
* Navigation
* File Editing
* Command History


