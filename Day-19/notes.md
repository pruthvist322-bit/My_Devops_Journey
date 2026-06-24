Day 19 – Shell Scripting (Inputs, Variables, Loops & Cron Jobs)

Today I continued learning Shell Scripting and explored how automation works in Linux.

Topics Covered:

• Reading user input in shell scripts
• Understanding special shell variables
• Numeric comparison operators
• Conditional statements
• Loop concepts
• Automating tasks using Cron Jobs

Shell Script Input:

#!/bin/bash

echo "Please enter your name:"
read name

echo "Hello, $name! Nice to meet you."

Special Variables:

- $0 → Script name
- $# → Number of arguments
- $* → All arguments
- $@ → Arguments in array format
- $$ → Current process ID
- $! → Last background process ID
- $? → Exit status

Numeric Operators:

- -eq → Equal
- -gt → Greater than
- -lt → Less than
- -ge → Greater than or equal
- -le → Less than or equal
- -ne → Not equal

Concepts Practiced:

• If condition
• If-Else condition
• For loop

Cron Job Commands:

- sudo dnf install cronie

- crontab -e  -->to create a cron tab
- crontab -l  -->to check the number of cronjob available 

- systemctl status cron  -->to check the status of cron

grep cron /var/log/syslog

Cron Syntax:

* * * * * /path/to/script
Where 
- first * is Minute  (0-60)
- Second * is Hour  (0-24)
- Third * is date (1-31)
- Fourth * is Month (1-12)
- fifth * is Day (0-7)

Examples:

Run at 10:00 AM daily:
00 10 * * * /script/path

Run at 1:00 PM every Friday:
00 13 * * 05 /script/path

Run at 1:30 PM Monday–Friday:
30 13 * * 01-05 /script/path

Hands-on:

touch "file_$(date +'%Y%m%d_%H%M%S').txt"

Key Learning:
Shell scripting combined with Cron Jobs helps automate repetitive Linux and DevOps tasks efficiently.
