# IP Addressing Scheme

This document describes the IP addressing approach used in the homelab.
Static and DHCP assignments are used to ensure predictable targeting
during vulnerability assessment.


## Network Segments

### NAT Network
- IP Assignment: DHCP (VirtualBox-managed)
- Purpose: Internet connectivity only
- Example Range: 10.0.2.0/24


### Internal Network – Whonix
- IP Assignment: DHCP (Whonix-managed)
- Purpose: Anonymized attacker traffic routing
- Example Range: 10.152.152.0/18


### Internal Network – Lab Network
- IP Assignment: Static (preferred)
- Purpose: Internal assessment and exploitation
- Example Range: 192.168.56.0/24


## Sample IP Allocation (Lab Network)

| VM | IP Address | Notes |
|----|-----------|------|
| Kali Linux | 192.168.56.10 | Attacker pivot |
| Metasploitable2 | 192.168.56.101 | Primary vulnerable target |
| OWASP BWA | 192.168.56.102 | Web testing |
| DVWA | 192.168.56.103 | Web testing |
| Vulnix | 192.168.56.104 | Privilege escalation |
| Windows 7 | 192.168.56.105 | Legacy Windows testing |
| Debian Server | 192.168.56.201 | Internal server |
| Windows Server | 192.168.56.202 | Internal server |


## Operational Notes
- Static IPs simplify repeatable testing
- Address ranges are documented to avoid scope confusion
- IP reuse is avoided during assessments