# wireshark-network-investigation
An academic cybersecurity project investigating three network packet captures to identify suspicious activity, analyse attack behaviour and recommend security improvements.

# Network Traffic Analysis & Incident Response Using Wireshark

## Project Overview

This project was originally completed as part of my Cyber Security degree at Manchester Metropolitan University and later developed into a portfolio investigation.

Using Wireshark, I analysed three network packet capture (PCAP) files to identify suspicious network activity, investigate potential cyberattacks and understand how attackers interact with vulnerable systems.

## Tools & Skills

- Wireshark
- Network Traffic Analysis
- TCP/IP and FTP Protocols
- Packet Filtering
- Incident Response
- Network Forensics

## Investigation 1 — TCP Port Scanning

**Attacker:** 192.168.56.104  
**Target:** 192.168.56.101

I identified approximately 48,174 packets exchanged between the two hosts. Further analysis revealed 22,797 TCP SYN packets targeting different ports, indicating a port-scanning attempt. Port 80 responded with a SYN-ACK, suggesting the HTTP service was accessible.

## Investigation 2 — FTP Brute-Force Attack

**Attacker:** 192.168.56.1  
**Target:** 192.168.56.101

I identified 826 failed FTP login responses followed by successful authentication. Further investigation showed the attacker requesting a confidential document using the FTP RETR command, with the server confirming the transfer.

## Investigation 3 — Unsuccessful FTP Brute-Force Attack

**Attacker:** 192.168.56.1  
**Target:** 192.168.56.102

I identified 4,685 failed FTP login responses, indicating repeated attempts to gain access to the server. Unlike the second investigation, no successful FTP authentication was observed in this capture.

## Security Recommendations

Based on these investigations, I identified several security measures that could help reduce similar attacks:

- Configure firewalls to restrict unnecessary ports.
- Monitor repeated connection and authentication attempts.
- Implement strong password policies and login rate limiting.
- Use secure file transfer protocols such as SFTP instead of FTP.
- Configure alerts to detect suspicious network activity.

## Conclusion

This project helped me develop my understanding of network traffic analysis and incident investigation. It also allowed me to practise identifying suspicious behaviour, interpreting network protocols and documenting security findings using packet-level evidence.

## Supporting Evidence

Wireshark screenshots and a more detailed investigation report will be added to demonstrate the findings from all three PCAP files.
