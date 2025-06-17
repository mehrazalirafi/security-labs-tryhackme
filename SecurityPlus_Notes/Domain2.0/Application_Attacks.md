
# Application Attacks Summary

This document summarizes key application attack types discussed in the video.

---

## 1. Injection Attacks
- **Code injection**: Attacker inserts malicious code into a data stream.
- **Caused by**: Poor input validation.
- **Examples**: SQL, HTML, XML, LDAP injections.

---

## 2. Buffer Overflow
- **Definition**: Overwriting a memory buffer leading to data spilling into adjacent memory.
- **Challenge**: Requires extensive testing to avoid crashing the application.
- **Impact**: Can allow attackers to gain control if the overflow is reliable and repeatable.

---

## 3. Replay Attacks
- **Mechanism**: Captures and reuses network traffic (e.g., credentials).
- **Sources**: ARP poisoning, network tap, malware.
- **Purpose**: To impersonate a user by replaying valid session data.
- **Note**: Not an on-path attack.

---

## 4. Privilege Escalation
- **Goal**: Gain higher or lateral access by exploiting vulnerabilities.
- **Types**:
  - **Vertical**: User gains admin or system privileges.
  - **Horizontal**: User A accesses User B's resources.
- **Mitigations**:
  - Apply patches.
  - Use antivirus/antimalware.
  - Enable Data Execution Prevention (DEP).
  - Enable Address Space Layout Randomization (ASLR).

---

## 5. CVE-2023-29336 Example
- **Vulnerability**: Win32k Kernel Elevation of Privilege.
- **Affected Systems**: Windows Server (2008–2016), Windows 10.
- **Impact**: Attacker gains SYSTEM privileges.

---

## 6. Cross-Site Request Forgery (CSRF)
- **Attack Type**: One-click/session riding using a trusted browser session.
- **Impact**: Can execute unauthorized actions like transferring funds or posting content.
- **Mitigation**: Use anti-forgery tokens (cryptographic).

---

## 7. Directory Traversal
- **Goal**: Access files outside the web server root (e.g., `../../../Windows/system.ini`).
- **Causes**: 
  - Server misconfiguration.
  - Poorly written application code.
- **Detection**: Look for `../` patterns in URLs or logs.

---
