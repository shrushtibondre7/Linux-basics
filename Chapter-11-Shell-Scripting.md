# Chapter 11 - Shell Scripting

# Introduction

Shell Scripting is the process of writing a sequence of Linux commands in a file so they can be executed automatically.

Instead of typing commands one by one, we can save them in a script and run them whenever required.

Shell scripting is widely used in Linux Administration, Cloud Computing, and DevOps for automation.

---

# What is a Shell?

A shell is a command-line interpreter that acts as an interface between the user and the Linux kernel.

Popular Linux shells:

- Bash (Bourne Again Shell)
- Sh
- Ksh
- Zsh

Check current shell

```bash
echo $SHELL
```

Example Output

```
/bin/bash
```

---

# What is a Shell Script?

A shell script is a text file containing Linux commands.

The file usually has the extension:

```
.sh
```

Example:

```
backup.sh
```

---

# Create Your First Script

Create a file

```bash
touch hello.sh
```

Open the file

```bash
vim hello.sh
```

Add the following content

```bash
#!/bin/bash

echo "Hello World"
```

Save the file.

---

# Give Execute Permission

```bash
chmod +x hello.sh
```

---

# Run the Script

Method 1

```bash
./hello.sh
```

Method 2

```bash
bash hello.sh
```

Output

```
Hello World
```

---

# Variables

Variables store values.

Example

```bash
#!/bin/bash

name="Shrushti"

echo $name
```

Output

```
Shrushti
```

---

# User Input

```bash
#!/bin/bash

echo "Enter your name"

read name

echo "Welcome $name"
```

---

# Command Line Arguments

Example

```bash
#!/bin/bash

echo $1

echo $2
```

Run

```bash
./script.sh Linux DevOps
```

Output

```
Linux

DevOps
```

---

# Arithmetic Operations

```bash
#!/bin/bash

a=20

b=10

echo $((a+b))

echo $((a-b))

echo $((a*b))

echo $((a/b))
```

---

# If Statement

```bash
#!/bin/bash

num=10

if [ $num -gt 5 ]
then
    echo "Number is greater than 5"
fi
```

---

# If Else

```bash
#!/bin/bash

num=2

if [ $num -gt 5 ]
then
    echo "Greater"
else
    echo "Smaller"
fi
```

---

# For Loop

```bash
#!/bin/bash

for i in 1 2 3 4 5
do
    echo $i
done
```

---

# While Loop

```bash
#!/bin/bash

count=1

while [ $count -le 5 ]
do
    echo $count
    count=$((count+1))
done
```

---

# Functions

```bash
#!/bin/bash

hello(){

echo "Welcome to Linux"

}

hello
```

---

# Important Operators

| Operator | Meaning |
|----------|---------|
| -eq | Equal |
| -ne | Not Equal |
| -gt | Greater Than |
| -lt | Less Than |
| -ge | Greater Than or Equal |
| -le | Less Than or Equal |

---

# Useful Commands

Current Directory

```bash
pwd
```

Current User

```bash
whoami
```

Current Date

```bash
date
```

Hostname

```bash
hostname
```

---

# Sample Backup Script

```bash
#!/bin/bash

tar -czvf backup.tar.gz /home/user/Documents

echo "Backup Completed Successfully"
```

---

# Hands-on Lab

## Objective

Create and execute a simple shell script.

### Step 1

Create script

```bash
touch myscript.sh
```

---

### Step 2

Open script

```bash
vim myscript.sh
```

---

### Step 3

Add

```bash
#!/bin/bash

echo "Welcome to Linux"

date

whoami

pwd
```

---

### Step 4

Give execute permission

```bash
chmod +x myscript.sh
```

---

### Step 5

Run

```bash
./myscript.sh
```

Expected Output

```
Welcome to Linux

Mon Jul 27

ubuntu

/home/ubuntu
```

---

# Best Practices

- Add comments in scripts.
- Use meaningful variable names.
- Test scripts before production.
- Give execute permission only when needed.
- Store scripts in a dedicated directory.

---

# Summary

In this chapter, we learned:

- Shell
- Shell Script
- Variables
- User Input
- Command Line Arguments
- If Statement
- Loops
- Functions
- Operators
- Backup Script

---

# Interview Questions

## 1. What is Shell Scripting?

Shell scripting is writing Linux commands in a file to automate tasks.

---

## 2. Which shell is most commonly used?

```
Bash
```

---

## 3. What is the extension of a shell script?

```
.sh
```

---

## 4. Which command gives execute permission?

```bash
chmod +x filename.sh
```

---

## 5. How do you execute a shell script?

```bash
./script.sh
```

or

```bash
bash script.sh
```

---

## 6. Which command displays the current shell?

```bash
echo $SHELL
```

---

## 7. Which line should appear at the beginning of a Bash script?

```bash
#!/bin/bash
```

---

# Practice Commands

```bash
echo $SHELL

touch hello.sh

chmod +x hello.sh

./hello.sh

bash hello.sh

date

whoami

pwd
```

---

# Conclusion

Shell scripting is one of the most valuable Linux skills for Cloud and DevOps Engineers. It helps automate repetitive tasks, manage servers efficiently, and build deployment and maintenance scripts.
