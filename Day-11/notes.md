# Day 11 - Linux Text Processing and File Searching Commands

## Objective

Today I learned some of the most powerful Linux commands used for searching, filtering, modifying, and analyzing files.

These commands are widely used by Linux Administrators, DevOps Engineers, and Site Reliability Engineers (SREs).

---

# Grep Command

`grep` is used to search for a specific pattern or string inside a file.

## Syntax

```bash
grep "pattern" filename
```

### Case Sensitive Search

```bash
grep "error" logfile.txt
```

### Case Insensitive Search

```bash
grep -i "error" logfile.txt
```

---

## Common Grep Options

### Display Filenames Containing a Pattern

```bash
grep -l "pattern" *
```

### Display Matching Lines Only

```bash
grep -h "pattern" *
```

### Display Matching Lines with Line Numbers

```bash
grep -n "pattern" *
```

### Count Matching Lines

```bash
grep -c "pattern" *
```

### Print Lines That Do NOT Match

```bash
grep -v "pattern" *
```

### Print Lines Ending with a Character

```bash
grep "x$" *
```

### Print Lines Starting with a Character

```bash
grep "^I" *
```

### Search Multiple Patterns

```bash
grep -e "pattern1" -e "pattern2" filename
```

### Recursive Search Inside Directories

```bash
grep -r "error" .
```

---

# Sed Command (Stream Editor)

`sed` is used to modify text in a file without opening it in an editor.

## Replace Text

```bash
sed 's/old/new/g' filename
```

This displays the output on the terminal without changing the original file.

---

## Modify Original File

```bash
sed -i 's/old/new/g' filename
```

---

## Replace in Specific Lines

### First Line

```bash
sed '1 s/old/new/g' filename
```

### Line 3 to 5

```bash
sed '3,5 s/old/new/g' filename
```

### Line 5 to End

```bash
sed '5,$ s/old/new/g' filename
```

---

## Print Specific Lines

### Print 5th Line

```bash
sed -n '5p' filename
```

### Print Lines 4 to 10

```bash
sed -n '4,10p' filename
```

### Print From 5th Line to End

```bash
sed -n '5,$p' filename
```

---

## Delete Specific Line

```bash
sed '5d' filename
```

Deletes line 5 in the output without affecting the original file.

---

# Awk Command

`awk` is used to process files column-wise.

---

## Print First Column

```bash
awk '{print $1}' filename
```

---

## Print Second and Third Columns

```bash
awk '{print $2,$3}' filename
```

---

## Print Last Column

```bash
awk '{print $NF}' filename
```

---

## Print Last Two Columns

```bash
awk '{print $(NF-1),$NF}' filename
```

---

## Print Second Last Column

```bash
awk '{print $(NF-1)}' filename
```

---

# Find Command

`find` is used to locate files and directories.

## Syntax

```bash
find . -name "filename"
```

`.` represents the current directory.

---

## Common Examples

### Find All .txt Files

```bash
find . -name "*.txt"
```

### Find Files Only

```bash
find . -type f -name "filename"
```

### Find Directories Only

```bash
find . -type d -name "directory"
```

### Find Empty Files

```bash
find . -type f -empty
```

### Find Empty Directories

```bash
find . -type d -empty
```

### Find All Empty Files and Directories

```bash
find . -empty
```

### Find Files Modified More Than 60 Days Ago

```bash
find . -type f -mtime +60
```

### Find Files Modified Within Last 30 Days

```bash
find . -type f -mtime -30
```

### Find Files Modified Within Last 15 Minutes

```bash
find . -type f -mmin -15
```

### Find Files with Permission 644

```bash
find . -type f -perm 644
```

### Find Non-Empty Files

```bash
find . -type f ! -empty
```

### Find Files Larger Than 1 KB

```bash
find . -type f -size +1k
```

---

# Key Takeaway

Today I learned:

* Grep for searching patterns
* Sed for modifying file content
* Awk for processing column-based data
* Find for locating files and directories

These commands are essential for log analysis, troubleshooting, automation, and day-to-day Linux administration.
