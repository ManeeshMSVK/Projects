# 🔍 Basic Vulnerability Assessment using Nmap

## 📄 Project Description
This project focuses on performing a basic vulnerability assessment on a simulated Linux server using **Nmap**. The aim was to detect live hosts, open ports, and services running on a target system within a virtual lab environment.

---

## 📊 Step-by-Step Process

### 📌 Step 1: Environment Setup
- Installed **VirtualBox**
- Created a Linux virtual machine (Kali Linux)
- Verified Nmap installation:
```bash
nmap --version
nmap 192.168.1.1
nmap -sP 192.168.1.0/24
nmap -p 1-65535 192.168.1.1
nmap -sV 192.168.1.1
