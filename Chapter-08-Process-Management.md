# Chapter 8 - Process Management

# Introduction

A process is a program that is currently running in the Linux operating system.

Linux allows multiple processes to run simultaneously, making it a multitasking operating system.

Process management helps monitor, control, stop, and prioritize running applications.

---

# What is a Process?

A process is an instance of a running program.

Example:

When you run:

```bash
firefox
```

Linux creates a new process.

Examples of processes:

- Chrome
- Firefox
- SSH
- Apache
- Docker
- Jenkins

---

# Process Life Cycle

```
           New
            |
            V
         Running
        /        \
Waiting          Ready
        \        /
          Terminated
```

---

# Process States

| State | Description |
|--------|-------------|
| Running | Process is executing |
| Sleeping | Waiting for an event |
| Stopped | Process paused |
| Zombie | Process finished but entry still exists |
| Terminated | Process completed |

---

# PID (Process ID)

Every running process has a unique Process ID (PID).

Display current shell PID

```bash
echo $$
```

Example Output

```
1254
```

---

# View Running Processes

## ps

Displays currently running processes.

```bash
ps
```

Detailed Output

```bash
ps -ef
```

---

## top

Displays live running processes.

```bash
top
```

Press

```
q
```

to quit.

---

## htop

A user-friendly version of top.

```bash
htop
```

Install Ubuntu

```bash
sudo apt install htop
```

---

# Kill Process

Kill using PID

```bash
kill PID
```

Example

```bash
kill 1234
```

Force Kill

```bash
kill -9 1234
```

---

# Kill by Process Name

```bash
pkill firefox
```

---

# Kill All Processes

```bash
killall firefox
```

---

# Background Process

Run command in background

```bash
sleep 100 &
```

View background jobs

```bash
jobs
```

Bring process to foreground

```bash
fg
```

Send process to background

```bash
bg
```

---

# Process Priority

Linux assigns priority using Nice values.

Range

```
-20   Highest Priority

0     Default

19    Lowest Priority
```

View Priority

```bash
ps -el
```

Start Process with Nice Value

```bash
nice -n 10 command
```

Change Priority

```bash
renice 5 PID
```

---

# Monitor System Performance

CPU Usage

```bash
top
```

Memory Usage

```bash
free -h
```

Disk Usage

```bash
df -h
```

Block Devices

```bash
lsblk
```

CPU Information

```bash
lscpu
```

---

# Useful Commands

Display PID

```bash
pidof sshd
```

Display Process Tree

```bash
pstree
```

Monitor Memory

```bash
vmstat
```

Monitor I/O

```bash
iostat
```

Display Running Services

```bash
systemctl list-units --type=service
```

---

# Process Signals

| Signal | Description |
|---------|-------------|
| SIGTERM (15) | Gracefully stop process |
| SIGKILL (9) | Force stop process |
| SIGHUP (1) | Restart process |
| SIGSTOP | Pause process |
| SIGCONT | Continue paused process |

---

# Jobs Command

Display Background Jobs

```bash
jobs
```

Example Output

```
[1]+ Running sleep 100 &
```

---

# Hands-on Lab

## Step 1

Start a background process

```bash
sleep 300 &
```

---

## Step 2

View background jobs

```bash
jobs
```

---

## Step 3

Display process list

```bash
ps -ef
```

---

## Step 4

Find PID

```bash
pidof sleep
```

---

## Step 5

Kill Process

```bash
kill PID
```

Replace PID with actual value.

---

## Step 6

Monitor system

```bash
top
```

---

# Best Practices

- Use `kill` before `kill -9`.
- Monitor CPU and memory regularly.
- Stop unnecessary processes.
- Check system performance using `top`.
- Use `systemctl` to manage services.

---

# Summary

In this chapter, we learned:

- What is a Process
- Process Life Cycle
- Process States
- PID
- ps
- top
- htop
- kill
- pkill
- killall
- jobs
- fg
- bg
- nice
- renice
- Process Signals

---

# Interview Questions

## 1. What is a process?

A process is a program that is currently running.

---

## 2. What is PID?

PID stands for Process ID. Every running process has a unique PID.

---

## 3. Which command displays running processes?

```bash
ps
```

or

```bash
ps -ef
```

---

## 4. Which command displays live processes?

```bash
top
```

---

## 5. What is the difference between kill and kill -9?

- `kill` sends SIGTERM (graceful termination).
- `kill -9` sends SIGKILL (forcefully terminates the process).

---

## 6. Which command displays background jobs?

```bash
jobs
```

---

## 7. Which command changes process priority?

```bash
renice
```

---

# Practice Commands

```bash
ps

ps -ef

top

sleep 300 &

jobs

pidof sleep

kill PID

free -h

df -h

lscpu

systemctl list-units --type=service
```

---

# Conclusion

Process Management is a fundamental Linux administration skill. Understanding processes, monitoring system performance, managing services, and controlling running applications are essential for Linux Administrators, Cloud Engineers, and DevOps Engineers.
