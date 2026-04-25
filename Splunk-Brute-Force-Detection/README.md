# 🔐 Brute Force Detection using Splunk SIEM

## 📌 Project Overview
This project detects brute-force attacks by analyzing SSH authentication logs using Splunk SIEM.

## 🛠 Tools Used
- Splunk Enterprise
- Linux auth.log
- SPL (Search Processing Language)

## 📊 Features
- Detect failed login attempts
- Extract attacker IP addresses
- Visualize attack patterns using dashboards

## 📸 Dashboard

![Dashboard](screenshots/dashboard.png)

## 🔍 Queries Used

```spl
index=* "Failed password"
| rex "from (?<ip>\d+\.\d+\.\d+\.\d+)"
| stats count as Attempts by ip
| sort - Attempts
