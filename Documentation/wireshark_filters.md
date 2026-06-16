# Wireshark Filters Documentation

## Overview

This document contains the Wireshark display filters used during the network traffic analysis project.

The purpose of using filters is to isolate specific types of network communication, analyze packet behavior, and identify possible suspicious activities.

Wireshark filters help security analysts investigate network events efficiently during incident response and threat hunting.

---

# 1. DNS Traffic Analysis

## Filter

```wireshark
dns
```

## Purpose

Used to display Domain Name System (DNS) packets.

DNS converts domain names into IP addresses and is one of the most important protocols to monitor.

## Analysis Performed

Reviewed:

- DNS queries
- DNS responses
- Requested domains
- Resolved IP addresses

## Security Relevance

DNS monitoring can help detect:

- Malicious domain communication
- Command and Control (C2) traffic
- DNS tunneling attempts
- Suspicious external connections


---

# 2. HTTP Traffic Analysis


## Filter

```wireshark
http
```

## Purpose

Used to inspect unencrypted web communication.

## Analysis Performed

Reviewed:

- HTTP GET requests
- HTTP responses
- Host information
- User-Agent information

## Security Relevance

HTTP analysis can reveal:

- Unencrypted data transmission
- Suspicious web requests
- Malicious downloads
- Abnormal browser activity


---

# 3. TCP Traffic Analysis


## Filter

```wireshark
tcp
```

## Purpose

Used to inspect TCP-based communication between systems.

## Analysis Performed

Observed:

- TCP connections
- Packet flow
- Communication behavior


## TCP Three-Way Handshake

Connection establishment process:

1. SYN

Client requests connection


2. SYN-ACK

Server accepts connection


3. ACK

Connection established


## Security Relevance

TCP monitoring helps identify:

- Port scanning
- Failed connections
- Suspicious sessions


---

# 4. TCP SYN Packets


## Filter

```wireshark
tcp.flags.syn == 1
```

## Purpose

Displays TCP connection attempts.


## Security Relevance

A large amount of SYN packets may indicate:

- Port scanning
- SYN flood attacks


---

# 5. TCP Reset Packets


## Filter

```wireshark
tcp.flags.reset == 1
```


## Purpose

Shows connections that were unexpectedly closed.


## Security Relevance

Can indicate:

- Blocked communication
- Failed connection attempts
- Network scanning activity


---

# 6. IP Address Investigation


## Filter

```wireshark
ip.addr == <IP_ADDRESS>
```


Example:

```wireshark
ip.addr == 192.168.56.1
```


## Purpose

Shows all packets related to a specific IP address.


Useful for:

- Tracking host communication
- Investigating suspicious devices
- Incident response


---

# 7. Source IP Filtering


## Filter

```wireshark
ip.src == <IP_ADDRESS>
```


## Purpose

Displays packets sent from a specific machine.


Used to investigate:

- Outbound connections
- Possible compromised hosts


---

# 8. Destination IP Filtering


## Filter

```wireshark
ip.dst == <IP_ADDRESS>
```


## Purpose

Displays packets going toward a specific machine.


Used for:

- Traffic monitoring
- Server communication analysis


---

# 9. ICMP Traffic Analysis


## Filter


```wireshark
icmp
```


## Purpose

Displays ICMP packets such as ping requests.


## Security Relevance

ICMP analysis helps detect:

- Network discovery attempts
- Connectivity testing
- Reconnaissance activity


---

# 10. ARP Traffic Analysis


## Filter

```wireshark
arp
```


## Purpose

Displays Address Resolution Protocol communication.


## Security Relevance

ARP monitoring helps identify:

- Network mapping
- Possible ARP spoofing attacks


---

# Common Investigation Filters


## Show HTTP or DNS Traffic

```wireshark
http || dns
```


## Hide ARP Traffic

```wireshark
!arp
```


## Show Failed TCP Connections

```wireshark
tcp.flags.reset == 1
```


## Find Traffic From One Host

```wireshark
ip.addr == target_ip
```


---

# Analyst Notes

During this project, these filters were used to separate normal network traffic from traffic that required further investigation.

Understanding packet behavior improves:

- Threat detection
- Incident investigation
- Network troubleshooting


---

# Conclusion

Wireshark filtering is a fundamental skill for cybersecurity analysts.

Effective packet filtering allows faster identification of abnormal communication patterns and possible security incidents.
