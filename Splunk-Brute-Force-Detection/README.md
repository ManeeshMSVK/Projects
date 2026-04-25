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

## 📈 Results
- Identified attacker IP: 192.168.1.10 with 10 failed attempts
- Detected repeated login failures indicating brute-force activity
- Visualized attack patterns using Splunk dashboard


## 📸 Dashboard

<img width="1920" height="1320" alt="Dashboard" src="https://github.com/user-attachments/assets/1a5a0197-ddf2-4941-b9ff-b05aab1b664e" />

## 🔍 Queries Used

```spl
index=* "Failed password"
| rex "from (?<ip>\d+\.\d+\.\d+\.\d+)"
| stats count as Attempts by ip
| sort - Attempts

## 💡 Conclusion
This project demonstrates how Splunk SIEM can be used to detect brute-force attacks by analyzing authentication logs. It helps security analysts identify suspicious behavior and respond effectively.
