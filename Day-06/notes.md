# Day 6 - Linux File Management and Text Processing Commands

## Objective

Today I continued learning Linux commands and explored file management, text replacement, user privileges, copying/moving files, and word counting commands.

These commands are commonly used by Linux Administrators and DevOps Engineers in day-to-day operations.

---

# String Replacement in vi Editor

## Replace All Occurrences

```bash
:%s/str1/str2/g
```

Replaces all occurrences of `str1` with `str2` in the entire file.

---

## Replace in a Specific Line

```bash
:1 s/str1/str2/g
```

Replaces the string only in line 1.

---

## Replace Within a Range of Lines

```bash
:1,3 s/str1/str2/g
```

Replaces the string from line 1 to line 3.

---

## Search for a String

```bash
:/string
```

Moves the cursor to the first occurrence of the string.

Press:

```text
n
```

to move to the next occurrence.

---

## Replace From a Specific Line to End of File

```bash
:5,$ s/str1/str2/g
```

Replaces the string from line 5 to the end of the file.

---

# File and Directory Deletion

## Delete a File

```bash
rm filename
```

Used to delete files.

---

## Delete an Empty Directory

```bash
rmdir dirname
```

Used to remove only empty directories.

---

## Delete Files and Directories Forcefully

```bash
rm -rf dirname
```

Where:

* r = recursively
* f = forcefully

⚠️ Use this command carefully because deleted files cannot be recovered easily.

---

# Super User (Root) Access

## Login as Root User

```bash
sudo su
```

or

```bash
sudo bash
```

---

## What is sudo?

```bash
sudo command
```

Runs a command with super user privileges.

Example:

```bash
sudo dnf install tree -y
```

---

# Copy Files and Directories

## Copy a File

```bash
cp sourcefile destination
```

Example:

```bash
cp file1 devops/dir1/
```

---

## Copy a Directory

```bash
cp -r source_directory destination
```

Example:

```bash
cp -r project1 backup/
```

---

# Move Files and Directories

## Move a File

```bash
mv source destination
```

Example:

```bash
mv onefile jan/feb/
```

---

## Rename a File

```bash
mv oldfilename newfilename
```

Example:

```bash
mv notes.txt day6-notes.txt
```

---

# Word Count Commands

## Count Lines, Words, and Characters

```bash
wc filename
```

---

## Count Number of Lines

```bash
wc -l filename
```

---

## Count Number of Words

```bash
wc -w filename
```

---

## Count Number of Characters

```bash
wc -c filename
```

---

# Echo Command

## Print Text

```bash
echo "I am printing"
```

Displays the text on the terminal.

Example Output:

```text
I am printing
```

---

# Key Takeaway

Today I learned:

* String replacement using vi editor
* File and directory deletion
* Root user access and sudo commands
* Copying and moving files/directories
* Renaming files
* Word counting commands
* Using the echo command

