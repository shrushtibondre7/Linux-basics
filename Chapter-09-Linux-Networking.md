# Chapter 9 - Linux Networking

# Introduction

Networking is the process of connecting computers and devices so they can communicate and exchange data.

Linux provides many built-in networking tools that help administrators monitor, troubleshoot, and manage network connections.

Networking knowledge is essential for Linux Administrators, Cloud Engineers, and DevOps Engineers.

---

# Basic Networking Terms

## IP Address

An IP (Internet Protocol) Address is a unique address assigned to every device connected to a network.

Example:

```
192.168.1.10
```

---

## MAC Address

A MAC (Media Access Control) Address is the physical address of a network interface card (NIC).

Example

```
08:00:27:5B:8A:11
```

---

## Hostname

Hostname is the name assigned to a Linux machine.

Display hostname

```bash
hostname
```

Detailed information

```bash
hostnamectl
```

---

## DNS

DNS (Domain Name System) converts domain names into IP addresses.

Example

```
google.com

↓

142.250.192.14
```

---

## Gateway

A gateway connects one network to another.

Example:

Your home router acts as the default gateway.

---

# Check IP Address

Modern command

```bash
ip addr
```

or

```bash
ip a
```

Older command

```bash
ifconfig
```

---

# Display Network Interfaces

```bash
ip link
```

---

# Display Routing Table

```bash
ip route
```

or

```bash
route -n
```

---

# Check Internet Connectivity

```bash
ping google.com
```

Stop ping

```
Ctrl + C
```

---

# DNS Lookup

```bash
nslookup google.com
```

or

```bash
dig google.com
```

---

# Check Open Ports

```bash
ss -tuln
```

Older command

```bash
netstat -tuln
```

---

# Check Listening Services

```bash
ss -l
```

---

# Download Files

Using wget

```bash
wget https://example.com/file.zip
```

Using curl

```bash
curl https://example.com
```

Download file

```bash
curl -O https://example.com/file.zip
```

---

# Display Active Connections

```bash
ss
```

---

# Check Network Configuration

```bash
nmcli device status
```

---

# Restart Network Service

Ubuntu

```bash
sudo systemctl restart NetworkManager
```

Check Status

```bash
systemctl status NetworkManager
```

---

# Firewall

Ubuntu (UFW)

Check status

```bash
sudo ufw status
```

Enable firewall

```bash
sudo ufw enable
```

Disable firewall

```bash
sudo ufw disable
```

Allow SSH

```bash
sudo ufw allow ssh
```

Allow HTTP

```bash
sudo ufw allow 80
```

---

# Important Networking Files

Hosts File

```text
/etc/hosts
```

DNS Configuration

```text
/etc/resolv.conf
```

Hostname

```text
/etc/hostname
```

---

# Useful Networking Commands

Current User

```bash
whoami
```

Hostname

```bash
hostname
```

Kernel Information

```bash
uname -a
```

IP Address

```bash
ip addr
```

Routing Table

```bash
ip route
```

DNS Lookup

```bash
nslookup google.com
```

Internet Connectivity

```bash
ping google.com
```

Listening Ports

```bash
ss -tuln
```

Download File

```bash
wget https://example.com/file.zip
```

---

# Common Ports

| Port | Service |
|------|----------|
| 20/21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 110 | POP3 |
| 143 | IMAP |
| 443 | HTTPS |
| 3306 | MySQL |
| 5432 | PostgreSQL |
| 6379 | Redis |
| 8080 | Tomcat |

---

# Hands-on Lab

## Objective

Learn basic Linux networking commands.

### Step 1

Check hostname

```bash
hostname
```

---

### Step 2

Check IP Address

```bash
ip addr
```

---

### Step 3

Check Routing Table

```bash
ip route
```

---

### Step 4

Test Internet

```bash
ping google.com
```

---

### Step 5

Check Open Ports

```bash
ss -tuln
```

---

### Step 6

Check DNS

```bash
nslookup google.com
```

---

### Step 7

Check Firewall

```bash
sudo ufw status
```

---

# Best Practices

- Use SSH instead of Telnet.
- Keep firewall enabled.
- Close unused ports.
- Use HTTPS whenever possible.
- Verify network connectivity before troubleshooting applications.

---

# Summary

In this chapter, we learned:

- IP Address
- MAC Address
- DNS
- Gateway
- Hostname
- ip command
- ping
- nslookup
- dig
- ss
- wget
- curl
- Firewall
- Network Configuration

---

# Interview Questions

## 1. What is an IP Address?

An IP address uniquely identifies a device on a network.

---

## 2. What is DNS?

DNS converts domain names into IP addresses.

---

## 3. Which command displays the IP address?

```bash
ip addr
```

---

## 4. Which command checks network connectivity?

```bash
ping
```

---

## 5. Which command displays open ports?

```bash
ss -tuln
```

---

## 6. Which file stores hostname?

```text
/etc/hostname
```

---

## 7. Which port is used by SSH?

```
22
```

---

## 8. Which port is used by HTTPS?

```
443
```

---

## Practice Commands

```bash
hostname

hostnamectl

ip addr

ip link

ip route

ping google.com

nslookup google.com

ss -tuln

curl https://google.com

wget https://example.com/file.zip

sudo ufw status
```

---

# Conclusion

Linux Networking is a core skill for system administration and DevOps. Understanding IP addressing, DNS, routing, ports, and troubleshooting commands is essential for managing Linux servers and cloud infrastructure.
