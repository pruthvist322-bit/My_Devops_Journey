# Day 8 - Linux File Permissions and Access Control Lists (ACLs)

## Overview

Today's session focused on understanding Linux file permissions, directory permissions, and Access Control Lists (ACLs). We explored different methods of assigning permissions, practiced multiple permission-related tasks, and learned how ACLs provide more granular access control.

---

## Topics Covered

### 1. Difference Between Files and Directories

Linux represents files and directories differently through permission notation:

| Type      | Example      |
| --------- | ------------ |
| File      | `-rw-r--r--` |
| Directory | `drwxr-xr-x` |

* `-` indicates a file.
* `d` indicates a directory.

---

### 2. Understanding Linux Permissions

Linux permissions are represented by:

| Permission | Symbol | Value |
| ---------- | ------ | ----- |
| Read       | r      | 4     |
| Write      | w      | 2     |
| Execute    | x      | 1     |

Example:

```bash
chmod 755 file.txt
```

Permission Breakdown:

* Owner → 7 (4+2+1 = rwx)
* Group → 5 (4+1 = r-x)
* Others → 5 (4+1 = r-x)

I prefer using the numeric (binary) permission method because it is quick, simple, and widely used in real-world environments.

---

### 3. Changing Permissions with chmod

Common commands:

```bash
chmod 755 file.txt
chmod 644 file.txt
chmod 700 script.sh
```

Tasks practiced:

* Granting permissions
* Removing permissions
* Testing various permission combinations
* Understanding permission inheritance

---

### 4. Recursive Permission Changes

Applied permissions to all files and subdirectories using recursive mode.

```bash
chmod -R 755 mydirectory
```

The `-R` option allows permissions to be applied recursively throughout the directory structure.

---

### 5. Directory Permissions

Learned how permissions behave differently on directories:

| Permission  | Directory Function            |
| ----------- | ----------------------------- |
| Read (r)    | View directory contents       |
| Write (w)   | Create/Delete files           |
| Execute (x) | Enter or access the directory |

Understanding directory permissions is critical for securing Linux systems.

---

### 6. Access Control Lists (ACLs)

ACLs provide more flexible permission management than traditional Linux permissions.

#### View Existing ACLs

```bash
getfacl file.txt
```

#### Grant Permissions to a User

```bash
setfacl -m u:username:rwx file.txt
```

#### Grant Permissions to a Group

```bash
setfacl -m g:groupname:r-x file.txt
```

#### Set Default ACLs for a Directory

```bash
setfacl -m d:u:username:rwx dir/
```

#### Remove ACL Permissions

```bash
sudo setfacl -x u:username file.txt
```

---

## Key Learnings

* Understood the difference between file and directory permissions.
* Learned numeric permission representation using 4, 2, and 1.
* Practiced permission management using `chmod`.
* Applied permissions recursively using `-R`.
* Explored directory-specific permission behavior.
* Learned how ACLs provide fine-grained access control.
* Used `getfacl` and `setfacl` to manage advanced permissions.

---

## Commands Practiced

```bash
chmod 755 file.txt
chmod -R 755 directory/
getfacl file.txt
setfacl -m u:username:rwx file.txt
setfacl -m g:groupname:r-x file.txt
setfacl -m d:u:username:rwx dir/
setfacl -x u:username file.txt
```

---

## Conclusion

Today's learning strengthened my understanding of Linux security fundamentals through file permissions, directory permissions, and ACL management. These concepts are essential for system administration, DevOps, cloud environments, and production server management.


