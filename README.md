# Wireshark Network Traffic Analysis

## Project Overview
This project documents hands-on analysis of network traffic captured from my own test environment using Wireshark. The investigation covers DNS resolution, the TCP three-way handshake, and TLS 1.3 encrypted communication.

## Tools Used
- Wireshark
- Windows 11
- TCP/IP, DNS, and TLS protocols

## Investigations

### 1. DNS Traffic Analysis
- Filtered DNS queries and responses for example.com.
- Identified A and AAAA DNS records.
- Examined DNS responses and resolved IP addresses.

![DNS Analysis](screenshots/01-dns-analysis.png)

### 2. TCP Three-Way Handshake
- Identified SYN, SYN-ACK, and ACK packets.
- Verified the connection establishment process.
- Analyzed TCP flags using Wireshark.

![TCP Handshake](screenshots/02-tcp-handshake.png)

### 3. TLS 1.3 Traffic Analysis
- Inspected Client Hello and Server Hello messages.
- Identified the negotiated TLS 1.3 version.
- Examined the TLS_AES_128_GCM_SHA256 cipher suite.
- Observed encrypted application data.

![TLS Analysis](screenshots/03-tls-analysis.png)

## Key Learning Outcomes
- Understanding DNS name resolution
- Analyzing TCP connection establishment
- Identifying TLS handshake messages
- Recognizing encrypted network traffic
- Documenting network investigations

## Disclaimer
All analysis was performed for educational purposes using traffic captured from my own environment.
