# Day 7 - Linux Redirection, Pipes, Shells, and System Monitoring

## Objective

Today I learned about Linux redirection, append operations, pipes, shell concepts, environment variables, system monitoring commands, and file viewing commands such as head and tail.

These concepts are widely used in Linux administration, scripting, and DevOps automation.

---

# Output Redirection (>)

Output redirection is used to send the output of one command to a file.

Syntax:

```bash
command > filename
```

Example:

```bash
cat file1 > file2
```

Behavior:

- If the destination file exists, its content will be overwritten.
- If the destination file does not exist, a new file will be created.

---

# Append Redirection (>>)

Append is used to add output to the end of a file.

Syntax:

```bash
command >> filename
```

Example:

```bash
cat file1 >> file2
```

Behavior:

- Existing content is preserved.
- New content is added at the bottom of the file.

### Difference Between > and >>

| Command | Behavior |
|----------|-----------|
| > | Overwrites existing content |
| >> | Appends content to existing file |

---

# Getting Help in Linux

## whatis

Provides a short description of a command.

```bash
whatis pwd
```

---

## --help

Displays command usage and options.

```bash
pwd --help
```

---

## man

Displays detailed manual documentation.

```bash
man pwd
```

---

# System Monitoring Commands

## Check Disk Usage

```bash
du -sh
```

Displays the disk usage of the current directory.

---

## Check File System Size

```bash
df -h
```

Displays disk space usage in human-readable format.

---

## Check Memory Usage

```bash
free -m
```

Displays RAM usage in MB.

---

## Monitor Running Processes

```bash
top
```

or

```bash
htop
```

Displays running processes and resource usage.

---

# Shell Basics

## What is a Shell?

A shell is a software interface between the user and the Linux kernel.

It accepts commands from the user and communicates with the operating system.

### Common Shell Types

1. Bash Shell
2. Korn Shell (ksh)
3. C Shell (csh)

Currently, I am using:

```text
Bash Shell
```

---

## View Available Shells

```bash
cat /etc/shells
```

---

## Check Current Shell

```bash
echo $SHELL
```

---

# Environment Variables

## View All Environment Variables

```bash
env
```

---

## Create Environment Variable

```bash
export VAR_NAME=value
```

Example:

```bash
export NAME=DevOps
```

---

## Remove Environment Variable

```bash
unset VAR_NAME
```

Example:

```bash
unset NAME
```

---

# Pipe Operator (|)

A pipe sends the output of one command as input to another command.

Syntax:

```bash
command1 | command2
```

---

## Example 1

```bash
ls -l | wc -l
```

Counts the number of lines from ls output.

---

## Example 2

```bash
cat filenames.txt | xargs touch
```

Creates multiple files using names stored in a file.

---

## Example 3

```bash
cat filenames.txt | xargs rm
```

Deletes files listed in a file.

---

# Head Command

Displays the beginning of a file.

```bash
head filename
```

By default, displays the first 10 lines.

---

## First 15 Lines

```bash
head -15 filename
```

---

# Tail Command

Displays the end of a file.

```bash
tail filename
```

By default, displays the last 10 lines.

---

## Last 2 Lines

```bash
tail -2 filename
```

---

## Monitor Live Updates

```bash
tail -f filename
```

Continuously monitors new content added to the file.

---

# Combining Head and Tail with Pipes

## Display 5th Line

```bash
head -5 filename | tail -1
```

---

## Display Lines 3 to 5

```bash
head -5 filename | tail -3
```

---

# Key Takeaway

Today I learned:

- Output Redirection (>)
- Append Redirection (>>)
- Linux Help Commands
- Disk and Memory Monitoring
- Shell Basics
- Environment Variables
- Pipe Operator (|)
- Head and Tail Commands
- Combining Commands Using Pipes

One of the most interesting concepts today was learning how pipes allow multiple commands to work together, making Linux much more powerful and efficient.
