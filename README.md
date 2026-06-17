# Network Traffic Analysis & Threat Detection

## 📌 Project Overview

This project demonstrates network packet analysis and threat investigation using Wireshark in a controlled cybersecurity lab environment.

The goal of this project is to capture live network traffic, analyze different protocols, identify communication patterns, and investigate possible suspicious activity.

This project follows a basic SOC Analyst workflow:

- Traffic Collection
- Packet Filtering
- Protocol Analysis
- Threat Investigation
- Security Documentation

---

## Why I Built This

After learning vulnerability assessment, I wanted to understand how defenders investigate network activity after communication happens.

I created this project to practice the workflow followed by SOC analysts when reviewing packet captures and identifying suspicious behavior.

This project improved my understanding of:

- Packet inspection
- Network protocols
- Traffic filtering
- Threat investigation
- Security monitoring

---

# 🎯 Objectives

The main objectives of this project are:

- Capture and analyze network packets
- Understand TCP/IP communication
- Analyze DNS and HTTP traffic
- Identify suspicious network behavior
- Practice SOC investigation methodology
- Document findings professionally


---

# 🖥️ Lab Environment


## Analyst Machine

Operating System:

- Kali Linux


Tools:

- Wireshark
- Linux Terminal


Environment:

- Virtual cybersecurity lab


---

# 🛠️ Tools Used


| Tool | Purpose |
|-|-|
| Wireshark | Packet capture and analysis |
| Kali Linux | Security analysis environment |
| Terminal | File management and documentation |


---

# 📂 Repository Structure


```
Network-Traffic-Analysis-Threat-Detection/

├── README.md
│
├── PCAP-Files/
│   └── network_capture.pcapng
│
├── Screenshots/
│   ├── packet_capture.png
│   ├── dns_analysis.png
│   ├── tcp_handshake.png
│   └── http_analysis.png
│
├── Analysis/
│   ├── dns_analysis.md
│   ├── tcp_analysis.md
│   └── suspicious_findings.md
│
├── Documentation/
│   ├── wireshark_filters.md
│   ├── packet_analysis_steps.md
│   ├── tools_used.md
│   └── lessons_learned.md
│
├── Indicators/
│   └── indicators_of_compromise.md
│
└── Report/
    └── network_analysis_report.md
```


---

# 🔎 Methodology


## 1. Traffic Capture


Wireshark was used to capture live network packets from the active network interface.


Captured data included:

- DNS requests
- TCP connections
- HTTP communication
- ICMP packets


The capture file was stored for offline investigation.


---

# 2. Protocol Analysis


Different Wireshark filters were applied to separate network traffic.


Filters used:


## DNS Analysis

```
dns
```


Used to inspect:

- Domain queries
- DNS responses
- External communication


---

## TCP Analysis


```
tcp
```


Used to analyze:

- Connection establishment
- TCP handshake
- Communication flow


---

## HTTP Analysis


```
http
```


Used to inspect:

- Web requests
- Server responses
- Unencrypted communication


---

# 📊 Analysis Summary


| Protocol | Purpose | Finding |
|-|-|-|
|DNS|Domain resolution analysis|Normal activity observed|
|TCP|Connection inspection|Successful connections identified|
|HTTP|Web traffic inspection|Reviewed unencrypted communication|
|ICMP|Network testing analysis|No abnormal activity detected|


---

# 🚨 Threat Investigation


Traffic was reviewed for suspicious indicators including:


- Unknown external connections
- Suspicious domains
- Repeated failed connections
- Unusual protocols
- Abnormal packet behavior


Result:

No confirmed malicious activity was detected during this analysis.


---

# 🛡️ Security Recommendations


Recommended security practices:


- Monitor network traffic regularly

- Investigate unknown connections

- Prefer encrypted HTTPS communication

- Analyze DNS activity for suspicious domains

- Implement SIEM monitoring for larger environments


---

# 🧠 Skills Demonstrated


This project demonstrates:

- Network Traffic Analysis

- Wireshark Packet Investigation

- TCP/IP Understanding

- SOC Analyst Investigation Workflow

- Threat Detection Basics

- Security Reporting

- Documentation Skills


---

# 🚀 Future Improvements


Planned improvements:

- Analyze malware PCAP samples

- Add Suricata IDS detection

- Generate alerts from suspicious traffic

- Forward logs into a SIEM platform

- Map suspicious behavior with MITRE ATT&CK

---

# How To Reproduce The Analysis


Clone repository:

```bash
git clone https://github.com/rahil33/Network-Traffic-Analysis-Threat-Detection.git

---

# 📌 Conclusion


This project provided hands-on experience in analyzing network communication and understanding how security analysts investigate network activity.

Packet analysis is a fundamental skill used in SOC operations, threat hunting, and incident response.


---

# Disclaimer


This project was completed in a controlled lab environment for cybersecurity learning purposes.

Only authorized network traffic was captured and analyzed.
