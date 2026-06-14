# Unix & Shell Programming

## Part 1: Quick Short Notes (Fundamentals)

### 1. Unix & Linux Fundamentals
*   **Unix:** A family of multitasking, multiuser computer operating systems developed in the 1970s at Bell Labs.
*   **Linux:** An open-source, Unix-like operating system kernel created by Linus Torvalds.
*   **Architecture:**
    *   *Hardware:* Physical components.
    *   *Kernel:* Core of the OS, interacts directly with hardware.
    *   *Shell:* Command-line interpreter that acts as an interface between the user and the kernel.
    *   *Applications:* User-level programs.

### 2. File Management & Linux Commands
*   **Filesystem Hierarchy:** Starts at the root `/`.
    *   `/bin`: Essential binaries (commands).
    *   `/etc`: System configuration files.
    *   `/home`: User home directories.
    *   `/var`: Variable data (logs).
*   **Basic Commands:**
    *   `ls`: List directory contents (`ls -l` for long format, `ls -a` for hidden files).
    *   `cd`: Change directory.
    *   `pwd`: Print working directory.
    *   `mkdir` / `rmdir`: Create / remove directory.
    *   `touch`: Create an empty file or update timestamp.
    *   `rm`: Remove files (`rm -r` for recursive directory removal).
    *   `cp` / `mv`: Copy / Move (rename) files.
*   **File Viewing:** `cat` (concatenate and display), `less` / `more` (page through), `head` / `tail` (view top/bottom lines).
*   **Searching:**
    *   `find`: Search for files in a directory hierarchy.
    *   `grep`: Search for text patterns inside files.

### 3. File Permissions
*   **Types:** Read (`r`, 4), Write (`w`, 2), Execute (`x`, 1).
*   **Categories:** User/Owner (`u`), Group (`g`), Others (`o`).
*   **Command:** `chmod` (change mode).
    *   Example: `chmod 755 file.txt` grants rwx (4+2+1=7) to owner, and rx (4+1=5) to group and others.
*   **Ownership Commands:** `chown` (change owner), `chgrp` (change group).

### 4. Process Management
*   **Process ID (PID):** Unique identifier for every running process.
*   **Commands:**
    *   `ps`: Display currently running processes.
    *   `top` / `htop`: Real-time dynamic view of system processes and resource usage.
    *   `kill`: Send a signal to a process (usually to terminate it). `kill -9 PID` forces termination.
    *   `bg` / `fg`: Move jobs to background / foreground.
    *   `&`: Added to the end of a command to run it in the background.

### 5. Shell Scripting & Automation Basics
*   **Shell Script:** A text file containing a sequence of commands for a UNIX-based operating system. Used for task automation, system administration, and application deployment.
*   **Shebang (`#!`):** The first line of a script indicating which interpreter to use (e.g., `#!/bin/bash`).
*   **Variables:** Assigned without spaces (`NAME="John"`), accessed with `$` (`echo $NAME`).
*   **Control Structures:**
    *   `if [ condition ]; then ... fi`
    *   `for var in list; do ... done`
    *   `while [ condition ]; do ... done`
*   **Automation:** `cron` is a time-based job scheduler. A `crontab` file contains instructions for the cron daemon to run scripts at specific times/intervals.

---

## Part 2: Placement-Related MCQs

1. Which of the following is the core component of the Linux operating system that interacts directly with hardware?

A) Shell

B) GUI

C) Kernel

D) Terminal

**Answer:** Option **C**

**Explanation:**

The Kernel is the core component of Linux. It manages system resources, memory, processes, and provides an interface for software applications to interact with the physical hardware. The Shell is the interface between the user and the kernel.

---

2. What command is used to list all files in a directory, including hidden files?

A) `ls -l`

B) `ls -h`

C) `ls -a`

D) `ls -R`

**Answer:** Option **C**

**Explanation:**

The `ls` command lists directory contents. The `-a` (or `--all`) flag tells it not to ignore entries starting with `.` (which are hidden files and directories in Linux).

---

3. Which of the following file permission settings grants read, write, and execute permissions to the owner, and only read and execute permissions to the group and others?

A) 777

B) 755

C) 644

D) 700

**Answer:** Option **B**

**Explanation:**

Permissions are calculated as Read=4, Write=2, Execute=1.
Owner: Read + Write + Execute = 4 + 2 + 1 = 7.
Group: Read + Execute = 4 + 1 = 5.
Others: Read + Execute = 4 + 1 = 5.
Combining these gives the octal permission `755`.

---

4. Which command is used to search for a specific text pattern inside a file?

A) `find`

B) `awk`

C) `grep`

D) `locate`

**Answer:** Option **C**

**Explanation:**

`grep` stands for Global Regular Expression Print. It processes text line by line and prints any lines which match a specified pattern. `find` is used to search for files themselves based on names or properties, not their contents.

---

5. What is the significance of the "shebang" (`#!/bin/bash`) at the beginning of a shell script?

A) It acts as a comment and is ignored by the system.

B) It tells the operating system which interpreter to use to execute the script.

C) It imports bash libraries required for the script to run.

D) It compiles the script into an executable binary file.

**Answer:** Option **B**

**Explanation:**

The shebang (`#!`) followed by the absolute path to an interpreter (like `/bin/bash` or `/usr/bin/python`) tells the operating system's program loader which interpreter should be used to parse and execute the lines of code in the script.

---

6. Which command forcibly kills a process with a specific Process ID (PID)?

A) `kill -1 PID`

B) `kill -9 PID`

C) `kill -15 PID`

D) `stop PID`

**Answer:** Option **B**

**Explanation:**

The `kill` command sends a signal to a process. The default signal is 15 (SIGTERM), which asks the process to terminate gracefully. `kill -9` sends the SIGKILL signal, which forces the kernel to terminate the process immediately without giving it a chance to clean up.

---

7. Which operator is used to append the output of a command to the end of an existing file?

A) `>`

B) `<`

C) `>>`

D) `|`

**Answer:** Option **C**

**Explanation:**

The `>` operator redirects standard output to a file, overwriting its contents. The `>>` operator appends the output to the end of the file without overwriting the existing data. The `|` (pipe) operator passes output to another command.

---

8. How do you declare and initialize a variable in a bash shell script correctly?

A) `VAR = "Value"`

B) `VAR="Value"`

C) `$VAR="Value"`

D) `int VAR="Value"`

**Answer:** Option **B**

**Explanation:**

In bash, you must not use spaces around the equals sign when assigning a variable. So `VAR="Value"` is correct. `VAR = "Value"` will result in an error because bash will try to execute a command named `VAR`.

---

9. What is the purpose of the `cron` daemon in Linux?

A) To manage network connections.

B) To monitor system memory usage.

C) To schedule commands or scripts to run automatically at specified times or intervals.

D) To encrypt user passwords.

**Answer:** Option **C**

**Explanation:**

`cron` is a time-based job scheduler in Unix-like operating systems. Users can set up cron jobs (stored in a crontab file) to automate repetitive tasks, such as backups or system maintenance, at specific times or intervals.

---

10. Which command provides a dynamic, real-time view of running processes and system resource utilization (CPU, RAM)?

A) `ps`

B) `df`

C) `top`

D) `free`

**Answer:** Option **C**

**Explanation:**

The `top` command (and its enhanced version `htop`) displays a real-time, frequently updated list of processes running on the system, along with memory and CPU usage statistics. `ps` only provides a static snapshot of processes at the moment it was executed.

---
