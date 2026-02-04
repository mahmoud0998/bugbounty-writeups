# 🛡️ Vulnversity – TryHackMe CTF Write-Up
## Web Exploitation & Privilege Escalation

> **Platform:** TryHackMe  
> **Room Name:** Vulnversity  
> **Difficulty:** Easy → Medium  
> **Category:** Web Exploitation / Linux Privilege Escalation  
> **Author:** Mahmoud Serhan  

---

## 📌 Overview

**Vulnversity** is a hands-on Capture The Flag (CTF) room on TryHackMe that focuses on
**web application exploitation** and demonstrates a full attack chain starting from
**enumeration**, moving to **file upload exploitation and web shell access**, and ending with
**Linux privilege escalation**.

This room is ideal for beginners who want to understand how real-world web vulnerabilities
can lead to complete system compromise.

---

## 🎯 Objectives

- Enumerate services and web application
- Discover hidden web directories
- Exploit a file upload vulnerability
- Gain Remote Code Execution (Web Shell)
- Escalate privileges to root
- Capture user and root flags

---

## 🧠 Skills Learned

- Network & service enumeration using Nmap
- Web content discovery with Gobuster
- File upload vulnerability bypass techniques
- Web Shell creation and execution
- Linux command execution via browser
- Privilege escalation using sudo misconfiguration
- Understanding real-world web attack flows

---

## 🛠️ Tools Used

- Nmap  
- Gobuster  
- Web Browser  
- PHP Web Shell  
- Linux built-in utilities  

---

## 🔍 Enumeration Phase

### 🔹 Network Enumeration

```bash
nmap -sC -sV -p- <TARGET_IP>
