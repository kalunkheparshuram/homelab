# Network Adapter Configuration

This document explains how VirtualBox network adapters are configured to simulate realistic enterprise network segmentation.
The design enforces isolation between attacker, server, and vulnerable zones while allowing controlled attack paths.


## Network Types Used

### 1. NAT Network

**Purpose**
- Provide controlled internet access for updates and tooling
- Prevent direct exposure of internal lab networks to the internet

**Attached To**
- Kali Linux
- Whonix Gateway
- Selected servers (temporarily, when required)

**Security Consideration**
- No vulnerable machines are directly connected
- Prevents accidental outbound attacks


### 2. Internal Network – Whonix

**Purpose**
- Dedicated internal network for anonymized attack traffic
- Separates attacker traffic from host and lab networks

**Attached To**
- Whonix Gateway
- Kali Linux (secondary adapter)

**Security Consideration**
- Ensures attack tools route through Whonix
- Reduces host fingerprinting risk


### 3. Internal Network – Lab Network

**Purpose**
- Simulates an internal corporate LAN
- Used for reconnaissance, scanning, exploitation, and lateral movement

**Attached To**
- Kali Linux
- Metasploitable2
- OWASP BWA
- DVWA
- Vulnix
- Windows 7 Ultimate
- Internal servers (Debian, Windows Server)

**Security Consideration**
- No direct internet access
- Fully isolated from host and external networks


## Design Rationale
Multiple adapters allow realistic attack simulation while maintaining  strict isolation between zones.