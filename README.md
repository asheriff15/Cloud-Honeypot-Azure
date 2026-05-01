# Cloud Honeypot Deployment — Microsoft Azure

![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Microsoft%20Azure-blue)
![Tool](https://img.shields.io/badge/Honeypot-T--Pot-orange)
![SIEM](https://img.shields.io/badge/SIEM-Elastic%2FKibana-yellow)

## Overview

Deployed a cloud-based honeypot on Microsoft Azure to capture and analyze real-world attack traffic. The environment was intentionally exposed to the public internet to attract malicious actors, with all activity logged and analyzed through T-Pot's built-in Elastic/Kibana stack. This project demonstrates cloud infrastructure deployment, network security configuration, threat analysis, and attacker behavior identification.

---

## Tools & Technologies

| Category | Tool |
|---|---|
| Cloud Provider | Microsoft Azure |
| Operating System | Ubuntu 24.04 |
| Honeypot Framework | T-Pot |
| Log Analysis | Elastic / Kibana |
| Network Security | Azure Network Security Groups (NSG) |
| Access | SSH (restricted to admin IP) |

---

## Architecture

> Add architecture diagram here showing Azure VM, NSG rules, exposed ports, and T-Pot components

---

## Project Walkthrough

### Phase 1 — Azure VM Deployment
- Created a Resource Group in Microsoft Azure
- Deployed an Ubuntu 24.04 virtual machine
- Configured VM size to support T-Pot resource requirements

> Add screenshot of Azure VM overview here

### Phase 2 — Network Security Group Configuration
- Configured NSG inbound rules to expose honeypot ports publicly to the internet
- Restricted SSH administrative access (port 64295) to personal IP only
- All other management ports blocked from public access

> Add screenshot of NSG rules here

### Phase 3 — T-Pot Installation
- Created a non-root user account for security best practices
- Cloned the T-Pot repository and ran the installation script
- Selected Hive installation type for full honeypot suite
- Verified all services running post-installation

> Add screenshot of T-Pot web GUI here

### Phase 4 — Telemetry Verification
- Confirmed exposed listeners were active and accepting connections
- Verified ingested events appearing in Elastic/Kibana dashboard
- Confirmed attack map receiving live traffic

> Add screenshot of Kibana dashboard with live events here

### Phase 5 — Attacker Activity Analysis
- Analyzed source IPs by geolocation and reputation
- Identified scanning and brute-force behavior patterns
- Investigated targeted services and attack techniques

> Add screenshot of attack analysis findings here

---

## Key Findings

| Finding | Detail |
|---|---|
| Top attacking countries | *Fill in after analysis* |
| Most targeted service | *Fill in after analysis* |
| Highest volume attack type | *Fill in after analysis* |
| Notable IPs flagged | *Fill in after analysis* |

---

## Skills Demonstrated

- Cloud infrastructure deployment (Microsoft Azure)
- Network security group configuration and access control
- Honeypot deployment and configuration (T-Pot)
- Log ingestion and analysis (Elastic/Kibana)
- Threat intelligence analysis (IP reputation, geolocation)
- Attacker behavior identification (scanning, brute-force)
- Linux administration (Ubuntu, SSH, systemctl)

---

## Lessons Learned

*Fill in after completing the project — what surprised you, what you would do differently, what you learned about real attacker behavior*

---

## References

- [T-Pot GitHub Repository](https://github.com/telekom-security/tpotce)
- [Microsoft Azure Documentation](https://docs.microsoft.com/en-us/azure)
