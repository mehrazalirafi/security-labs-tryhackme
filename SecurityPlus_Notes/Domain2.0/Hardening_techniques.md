# Summary: Security Hardening Techniques

This video covers a wide range of system and network hardening strategies to mitigate threats and secure computing environments.

## System Hardening
- Apply updates and security patches regularly
- Enforce strong password policies and account limitations
- Restrict network access and implement monitoring with antivirus/anti-malware tools

## Encryption
- Use **EFS** for file-level encryption
- Use **FDE** (e.g., BitLocker, FileVault) for full-disk encryption
- Secure all network traffic via VPN and application encryption

## Endpoint Protection
- Stop inbound/outbound attacks
- Harden all types of user devices: desktops, laptops, mobile
- Implement layered security (defense in depth)

## EDR (Endpoint Detection and Response)
- Detect threats using behavior analysis, machine learning, process monitoring
- Investigate and determine root cause
- Respond automatically via APIs: isolate, quarantine, rollback

## Host-Based Firewall
- Software-based control of incoming/outgoing traffic
- Block unknown processes
- Centralized management

## HIPS (Host-Based Intrusion Prevention System)
- Detect known attacks using signatures, heuristics
- Protect application and OS configurations
- Identify anomalies like buffer overflows or registry changes

## Open Ports & Services
- Minimize open ports
- Control access via NGFW or firewalls
- Scan regularly using tools like **Nmap**

## Default Password Changes
- Change default credentials on all systems
- Add extra layers of security like MFA

## Unused Software Removal
- Remove unnecessary apps to reduce attack surface
- Helps simplify update management and minimize vulnerabilities

These hardening steps are essential to maintain a secure infrastructure and reduce exposure to threats.

---
