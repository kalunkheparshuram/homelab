### Dyson Swarm – Server Zone
Purpose:
- Simulates internal production servers
- Hosts Debian and Windows server machines
- Intended to represent post-compromise lateral movement targets

Threat Model:
- Assumed to be protected by internal segmentation
- Accessible only after pivoting or misconfiguration

Screenshot:
![Dyson Swarm](screenshot/dyson-swarm.png)

### Sentinels – Attacker Zone
Purpose:
- Dedicated offensive security machines
- Kali Linux and Whonix Gateway used for controlled attack operations

Security Design:
- Internet access via NAT Network
- Internal Whonix network for anonymized testing
- Segregated from vulnerable zone to avoid accidental contamination

Screenshot:
![Dyson Swarm](/screenshot/sentinels.png)

### Contaminated Zone – Vulnerable Zone
Purpose:
- Deliberately vulnerable systems for exploitation testing
- Includes Metasploitable2, OWASP BWA, DVWA, Vulnix, Windows 7 Ultimate

Risk Level:
- Fully exploitable
- Used to simulate real-world vulnerable assets

Screenshot:
![Dyson Swarm](screenshot/contaminated-zone.png)