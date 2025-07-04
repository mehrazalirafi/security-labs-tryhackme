# Digital Forensics & E-Discovery Summary

## Core Processes (RFC 3227 Framework)
1. **Acquisition**  
   - Sources: Disk/RAM, firmware, OS files, network logs, VM snapshots  
   - Critical artifacts: Log files, recycle bins, browser data, temp files  
   - Live collection: Essential for encrypted systems (prevents data loss on shutdown)  

2. **Preservation**  
   - Maintain evidentiary integrity:  
     - Isolate original data  
     - Work exclusively from copies  
   - Legal hold requirements:  
     - Ongoing obligation once notified  
     - Separate ESI (Electronically Stored Information) repository  

3. **Chain of Custody**  
   | Control Measure       | Implementation                     |
   |-----------------------|------------------------------------|
   | Integrity Verification| Cryptographic hashing (SHA-256+)  |
   | Access Tracking       | Digital signatures for all access |
   | Physical Security     | Sealed storage with tamper evidence|
   | Documentation         | Digital tagging of all items      |

4. **Analysis & Reporting**  
   - **Report Components**:  
     - Executive summary of event  
     - Detailed acquisition methodology  
     - Forensic findings (fact-based)  
     - Professional conclusions  
   - **Critical Practice**:  
     - Maintain detailed contemporaneous notes  

## Legal Processes
### E-Discovery vs. Digital Forensics
| **E-Discovery**                | **Digital Forensics**             |
|--------------------------------|-----------------------------------|
| Focus: Data collection         | Focus: Evidence analysis          |
| No intent consideration        | Determines intent/malice          |
| Produces responsive documents  | Recovers deleted/hidden data      |
| Example: Collecting email logs | Example: Proving data tampering   |

### Legal Hold Process
```mermaid
graph LR
A[Legal Counsel Notification] --> B[Identify Custodians]
B --> C[Preserve ESI]
C --> D[Create Separate Repository]
D --> E[Ongoing Preservation]
