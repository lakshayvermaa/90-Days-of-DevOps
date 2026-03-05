# Day 04 - Linux File Permissions

Today I studied **Linux File Permissions**, which are an important part of Linux security and access control.

Linux is a **multi-user operating system**, meaning multiple users can work on the same system simultaneously.  
To prevent unauthorized access or modification of files, Linux assigns **permission rules to every file and directory**.

---

# 1. Ownership Levels

Each file in Linux has three categories of users:

| Category | Meaning |
|--------|--------|
| User (Owner) | The person who created the file |
| Group | A collection of users who share the same permissions |
| Others | Everyone else on the system |

---

# 2. Permission Types

Linux defines three types of permissions for each category.

| Permission | Symbol | Meaning | Numeric Value |
|-----------|--------|--------|---------------|
| Read | r | View file contents | 4 |
| Write | w | Modify file or directory | 2 |
| Execute | x | Run the file as a program | 1 |

---

# 3. Checking File Permissions

To check permissions of a file or directory:

```bash

-rw-rw-r-- 1 ubuntu ubuntu 27 Oct 6 05:51 hello.txt
ls -l
