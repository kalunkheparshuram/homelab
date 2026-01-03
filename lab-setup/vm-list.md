# Virtual Machine Inventory

This document lists all virtual machines used in the segmented VAPT homelab, their roles, security zones, and network connectivity.
The inventory is maintained to ensure clarity of scope during assessment and to prevent accidental testing outside authorized systems.


## Virtual Machine List

| VM Name | Operating System | Zone | Role | Network Adapters |
|------|------------------|------|------|------------------|
| Kali Linux | Kali Linux | Sentinels | Primary attack machine for scanning, exploitation, and validation | NAT Network, Internal (Whonix) |
| Whonix Gateway | Whonix | Sentinels | Anonymized gateway for attack traffic | NAT Network, Internal (Whonix) |
| Debian Server | Debian Linux | Dyson Swarm | Internal server simulation | Internal (Lab Network) |
| Windows Server | Windows Server | Dyson Swarm | Internal enterprise server simulation | Internal (Lab Network) |
| Metasploitable2 | Linux | Contaminated Zone | Intentionally vulnerable host | Internal (Lab Network) |
| OWASP BWA | Linux | Contaminated Zone | Vulnerable web application platform | Internal (Lab Network) |
| DVWA | Linux | Contaminated Zone | Web application vulnerability testing | Internal (Lab Network) |
| Vulnix | Linux | Contaminated Zone | Linux privilege escalation testing | Internal (Lab Network) |
| Windows 7 Ultimate | Windows | Contaminated Zone | Legacy vulnerable Windows host | Internal (Lab Network) |


## Scope Notice
Only systems listed above are included in testing scope.
No production or external systems are targeted.
