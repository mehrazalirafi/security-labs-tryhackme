# Intro to Defensive Security – Summary

**Objective:**  
Understand how to **prevent**, **detect**, and **respond** to cyber intrusions using tools and practices employed by blue teams.

## Core Concepts:
- **Preventing intrusions** and **detecting/responding** to attacks.
- Blue teams handle defensive operations in cybersecurity.

## Key Practices:
- User security awareness and training  
- Asset documentation and patch management  
- Deployment of firewalls & IPS  
- Network logging and device monitoring

## Security Operations Center (SOC):
- Monitors networks/systems for suspicious activity.
- Handles:
  - Vulnerabilities
  - Policy violations
  - Unauthorized access
  - Intrusions
- Uses tools like **SIEM** for event correlation and alerting.

## Threat Intelligence:
- Collects and analyzes data about potential/active threats.
- Helps predict adversary behavior (e.g., state actors, ransomware groups).
- Sources: forums, network logs, public databases.
- Goal: **Threat-informed defense**

## DFIR (Digital Forensics & Incident Response):
### Digital Forensics:
- Investigates cybercrimes using:
  - File system artifacts
  - Memory dumps
  - Log files
  - Network packet analysis

### Incident Response Process:
1. **Preparation**
2. **Detection & Analysis**
3. **Containment, Eradication, Recovery**
4. **Post-Incident Review**

## Malware Analysis:
- Understand malware like viruses, trojans, and ransomware.
- **Static Analysis**: Study code without execution.
- **Dynamic Analysis**: Observe behavior in a sandbox environment.

## SIEM Simulation (Hands-on):
- Investigated alerts:
  - Failed logins
  - Suspicious IPs (e.g., 143.110.250.149)
- Verified IP reputation → Confirmed malicious
- Escalated to SOC lead → Blocked on firewall
- **Flag:** `THM{THREAT-BLOCKED}`
