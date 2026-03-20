# Basic-Intrusion-Detection-Wireshark
This project simulates suspicious network activity and demonstrates basic intrusion detection techniques using Wireshark. The goal is to identify abnormal traffic patterns such as port scanning, repeated connections, and unusual port usage.
asic Intrusion Detection using Wireshark

## Overview
This project simulates suspicious network activity and demonstrates basic intrusion detection techniques using Wireshark. The goal is to identify abnormal traffic patterns such as port scanning, repeated connections, and unusual port usage.


## Objectives
Capture and analyze network traffic
Establish baseline (normal behavior)
Simulate suspicious activity
Detect anomalies using packet analysis
Identify SYN scan patterns and unusual traffic

## Tools Used
Wireshark
Nmap
Windows Command Prompt

## Methodology
1. Baseline Traffic Analysis
Captured normal browsing activity (Google, YouTube) to understand standard traffic behavior.


2. Traffic Capture
Wireshark capture with filter:

ip.addr == 192.168.0.0/24

3. Suspicious Activity Simulation
Simulated port scanning using:

nmap -p- 127.0.0.1

4. Detection Techniques
SYN Scan Detection
tcp.flags.syn == 1 && tcp.flags.ack == 0
Unusual Ports
tcp.port not in {80 443 53}
DNS Monitoring
dns
Traffic Analysis
Used:

Statistics → Conversations
Statistics → Endpoints

## Key Findings
Observed high SYN packet activity during scan simulation
Identified repeated connection attempts across multiple ports
Detected non-standard ports used during scanning
Baseline traffic dominated by HTTPS (port 443)

## Security Analysis
SYN packet spikes indicate scanning behavior
Traffic patterns during simulation differ significantly from normal browsing
No external malicious activity detected (controlled environment)

## Conclusion
Successfully simulated and detected suspicious activity using Wireshark. Demonstrated basic intrusion detection capabilities and understanding of attack patterns.


## Learning Outcomes
Understanding of port scanning behavior
Identification of SYN scan patterns
Differentiation between normal and abnormal traffic
Practical intrusion detection techniques

## Screenshots
<img width="1920" height="1080" alt="8" src="https://github.com/user-attachments/assets/81f08049-8440-4335-9b88-3f2b685a080d" />
<img width="1202" height="758" alt="7" src="https://github.com/user-attachments/assets/2017238f-1e19-4e67-9426-1c6d670eb88a" />
