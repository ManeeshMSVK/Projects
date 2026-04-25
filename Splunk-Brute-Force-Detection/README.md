# 🔐 Brute Force Detection using Splunk SIEM

## 📌 Project Overview
This project focuses on detecting brute-force attacks by analyzing SSH authentication logs using Splunk SIEM. It involves parsing log data, extracting attacker IP addresses using regular expressions, and aggregating failed login attempts to identify suspicious activity. The results are visualized through an interactive dashboard for effective monitoring and analysis.

## 🛠 Tools Used
- Splunk Enterprise
- Linux auth.log
- SPL (Search Processing Language)

## 📊 Features
- Detect failed login attempts
- Extract attacker IP addresses
- Visualize attack patterns using dashboards


## 📸 Dashboard

<img width="1914" height="546" alt="image" src="https://github.com/user-attachments/assets/ff3c5a92-1ac1-4d59-a940-2beb4edd0890" />


## 🔍 Queries Used

```spl
index=* "Failed password"
| rex "from (?<ip>\d+\.\d+\.\d+\.\d+)"
| stats count as Attempts by ip
| sort - Attempts
```

## 📈 Results
- Identified attacker IP: 192.168.1.10 with 10 failed attempts
- Detected repeated login failures indicating brute-force activity
- Visualized attack patterns using Splunk dashboard

## 💡 Conclusion
This project demonstrates how Splunk SIEM can be used to detect brute-force attacks by analyzing authentication logs. It helps security analysts identify suspicious behavior and respond effectively.
