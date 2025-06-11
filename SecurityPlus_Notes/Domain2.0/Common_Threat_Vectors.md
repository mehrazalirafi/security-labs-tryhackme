# Threat Vectors Summary

_Notes sourced from Professor Messer's video lecture._

## What is a Threat Vector?

- A method used by an attacker to gain access or infect a target
- Also known as **attack vectors**
- IT security professionals monitor and protect against these vectors
- Constant effort is spent identifying and patching vulnerabilities

---

## Message-based Vectors

- One of the most common and effective threat vectors
- Common methods:
  - **Email**: Links to malicious sites, phishing pages
  - **SMS**: Texts with dangerous links
  - **Instant Messaging**: Direct malware/social engineering

### Common Threats:
- **Phishing attacks**
- **Malware delivery via attachments or links**
- **Social engineering scams** (e.g., invoice fraud, crypto scams)

---

## Image-based Vectors

- Harder to detect than text-based threats
- **SVG (Scalable Vector Graphics)** can include:
  - Embedded HTML/JavaScript
  - Potential XSS (Cross-site Scripting) attacks
- **Browsers must validate input** to avoid executing malicious code

---

## File-based Vectors

- Threats can hide in non-executable files like:
  - **PDFs** (may include scripts)
  - **ZIP/RAR files** (malware hidden inside)
  - **Microsoft Office files** (macros, add-ins)

---

## Voice Call Vectors

- **Vishing**: Phishing over the phone
- **Spam over IP**: Mass robocalls via VoIP
- **War dialing**: Still used to find exposed phone systems
- **Call tampering**: Disrupts or hijacks voice communications

---

## Removable Device Vectors

- **USB drives** can bypass firewalls and infect air-gapped systems
- Can emulate keyboards to execute commands
- Used for **data exfiltration** (sneaking data out physically)

---

## Vulnerable Software Vectors

- **Client-based**: Infected executables on local machines
- **Agentless**: Vulnerabilities in server software used by many users
- Regular patching is critical

---

## Unsupported Systems Vectors

- **Old, unpatched systems** are highly vulnerable
- Systems running outdated OS with no vendor support
- Must maintain an updated asset inventory

---

## Unsecure Network Vectors

- **Wireless**: Weak protocols (WEP, WPA, WPA2), rogue APs
- **Wired**: Lacking authentication (e.g., no 802.1X)
- **Bluetooth**: Vulnerabilities, location tracking, exploitation

---

## Open Service Ports

- Open TCP/UDP ports can be exploited via:
  - Misconfigured services
  - Vulnerable applications
- Firewall rules should restrict unnecessary open ports

---

## Default Credentials

- Devices often ship with **default usernames/passwords**
- These must be changed immediately
- Attackers often use sites like [routerpasswords.com](https://www.routerpasswords.com)

---

## Supply Chain Vectors

- Threats introduced during **manufacturing or vendor services**
- **Managed Service Providers (MSPs)** can be targeted
- **Counterfeit equipment** may have malware or backdoors
  - Example: 2020 fake Cisco Catalyst switches
