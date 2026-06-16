# Network Traffic Analysis & Threat Detection Report


## 1. Introduction


### Project Overview

This project focuses on analyzing captured network traffic using Wireshark in a controlled cybersecurity lab environment.

The objective of this analysis was to understand normal network communication, identify important protocols, inspect packet behavior, and detect possible suspicious activities.

Network packet analysis is an essential skill used by SOC Analysts during:

- Incident response
- Threat hunting
- Malware investigation
- Network troubleshooting


---

## Objective


The main objectives of this project were:

- Capture live network packets
- Analyze different network protocols
- Understand client-server communication
- Identify abnormal traffic patterns
- Document security observations


---

## Lab Environment


### Analyst Machine

Operating System:

- Kali Linux


Tools Used:

- Wireshark
- Linux Terminal


Network Environment:

- Virtual lab network
- Controlled testing environment


---

# 2. Methodology


The analysis followed a structured packet investigation process.


## Step 1: Packet Capture


Tool Used:

Wireshark


Process:

Live network traffic was captured from the active network interface.


Activities performed to generate traffic:

- Web browsing
- DNS requests
- ICMP testing
- Normal system communication


Captured traffic was saved as:

```
network_capture.pcapng
```


Purpose:

To collect packet data for investigation and analysis.


---

# Step 2: Protocol Filtering


Wireshark display filters were used to separate traffic types.


Filters Used:


DNS:

```
dns
```


HTTP:

```
http
```


TCP:

```
tcp
```


ICMP:

```
icmp
```


ARP:

```
arp
```


Filtering allowed focused investigation of individual protocols.


---

# Step 3: Packet Inspection


Packets were manually reviewed to understand:


- Source IP address

- Destination IP address

- Protocol behavior

- Packet flow

- Connection establishment


---

# Step 4: Security Analysis


Traffic was analyzed for indicators such as:


- Unknown connections

- Repeated requests

- Suspicious domains

- Failed connections

- Abnormal packet behavior


---

# 3. Traffic Analysis Findings


# Finding 1: DNS Traffic Analysis


Protocol:

DNS


Filter Used:

```
dns
```


## Observation


DNS queries and responses were successfully identified.


Observed activity:


- Domain name resolution

- DNS request packets

- DNS response packets


## Security Importance


DNS monitoring helps identify:


- Malware communication

- Suspicious domains

- Command and Control communication


## Result


No suspicious DNS communication was identified during the analysis.


Risk Level:

Low


---

# Finding 2: TCP Communication Analysis


Protocol:

TCP


Filter Used:


```
tcp
```


## Observation


TCP communication between devices was observed.


The TCP three-way handshake process was analyzed:


1. SYN

Client initiates connection


2. SYN-ACK

Server responds


3. ACK

Connection established



## Security Importance


TCP analysis helps identify:


- Port scanning attempts

- Unauthorized connections

- Abnormal communication patterns


## Result


Normal TCP connection behavior was observed.


Risk Level:

Low


---

# Finding 3: HTTP Traffic Analysis


Protocol:

HTTP


Filter Used:


```
http
```


## Observation


HTTP communication packets were inspected.


Reviewed:


- HTTP requests

- Server responses

- Headers

- Client-server communication


## Security Importance


Unencrypted HTTP communication can expose:


- Sensitive information

- Session data

- Transmitted content


## Recommendation


Use encrypted HTTPS communication wherever possible.


Risk Level:

Medium


---

# Finding 4: ICMP Traffic Analysis


Protocol:

ICMP


Filter Used:


```
icmp
```


## Observation


ICMP packets generated through network testing were analyzed.


Reviewed:


- Echo requests

- Echo replies


## Security Importance


ICMP monitoring helps identify:


- Network scanning

- Reconnaissance attempts


## Result


No abnormal ICMP activity detected.


Risk Level:

Low


---

# Finding 5: Suspicious Traffic Review


## Investigation


Traffic was reviewed for:


- Unknown external connections

- Excessive connection attempts

- Unusual ports

- Failed communications


## Result


No confirmed malicious network activity was identified.


---

# 4. Security Recommendations


Based on the traffic analysis, the following security practices are recommended:


## Network Protection


- Monitor network traffic regularly

- Investigate unknown connections

- Block unnecessary communication


---

## Secure Communication


Recommendations:


- Prefer HTTPS over HTTP

- Avoid transmitting sensitive information through unencrypted protocols


---

## DNS Security


Recommendations:


- Monitor DNS queries

- Block malicious domains

- Use trusted DNS services


---

## Continuous Monitoring


Organizations should implement:


- SIEM monitoring

- Alert rules

- Log analysis

- Threat detection workflows


---

# 5. Skills Demonstrated


This project demonstrates practical knowledge in:


- Packet Analysis

- Network Security Monitoring

- Wireshark Usage

- TCP/IP Fundamentals

- Threat Investigation

- SOC Analyst Workflow

- Security Documentation


---

# 6. Conclusion


The network traffic analysis successfully demonstrated how packet inspection can be used to understand network behavior and identify potential security issues.

Wireshark filtering techniques were used to investigate DNS, TCP, HTTP, ICMP, and ARP traffic.

Although no malicious activity was discovered, the project strengthened practical understanding of network monitoring and defensive security analysis.

Packet analysis remains an important skill for cybersecurity professionals involved in SOC operations, incident response, and threat detection.


---

# Disclaimer


This project was completed inside a controlled cybersecurity lab environment for educational purposes only.

All captured traffic belongs to authorized systems.
