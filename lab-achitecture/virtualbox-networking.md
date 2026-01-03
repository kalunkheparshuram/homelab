## VirtualBox Network Configuration

The lab uses three distinct network types:

### 1. NAT Network
Purpose:
- Internet access for updates and tool usage

Attached To:
- Kali Linux
- Whonix Gateway
- Selected servers (when required)

Risk:
- Carefully monitored to prevent data leakage


### 2. Internal Network – Whonix
Purpose:
- Isolated anonymized attack traffic
- Ensures attack machines do not expose real host identity

Attached To:
- Whonix Gateway
- Kali Linux (second adapter)


### 3. Internal Network – Lab Network
Purpose:
- Simulates internal corporate LAN
- Used for scanning, enumeration, exploitation

Attached To:
- Vulnerable machines
- Selected servers
