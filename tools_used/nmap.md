# Nmap – Network Reconnaissance & Enumeration

## Role in VAPT
Nmap is used during the reconnaissance and enumeration phases to identify live hosts, exposed ports, services, and operating systems within the internal lab network.


## Skills Demonstrated
- Network Security Assessment
- Reconnaissance & Enumeration
- Security Misconfiguration Identification
- Vulnerability Assessment (pre-scanning phase)


## Usage Approach

### Host Discovery
Used to identify active systems within the lab network.
This helps define the actual attack surface before deeper testing.

### Port & Service Enumeration
Service version detection is used to:
- Identify outdated services
- Map services to known CVEs
- Detect unnecessary exposed services

### OS Fingerprinting
Used to:
- Tailor exploitation strategy
- Identify legacy systems (e.g., Windows 7)


## Example Commands

```bash
nmap -sn 192.168.56.0/24
nmap -sS -sV -O -T4 192.168.56.101
```
