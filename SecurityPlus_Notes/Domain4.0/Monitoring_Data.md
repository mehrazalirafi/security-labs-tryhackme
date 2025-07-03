# File Integrity Monitoring (FIM) & Data Loss Prevention (DLP) Summary

## 📁 File Integrity Monitoring (FIM)
- **Purpose**:  
  Monitors critical OS/application files to detect unauthorized changes  
  - Files that should rarely change (e.g., executables) vs. frequently changing files (e.g., cached data)  

- **Key Tools**:  
  - **Windows**: System File Checker (SFC) - Scans/repairs critical OS files  
  - **Linux**: Tripwire - Real-time file change monitoring  
  - **Host-based IPS**: Combines intrusion prevention with FIM capabilities  

---

## 🛡️ Data Loss Prevention (DLP)
### Core Functions
1. **Locate sensitive data**:  
   SSNs, credit card numbers, medical records  
2. **Prevent unauthorized transmission**:  
   Block "data leakage" to attackers  

### Implementation Types
| **Location**       | **Data State** | **Description**                     |
|---------------------|---------------|-------------------------------------|
| Workstations/Endpoints | Data in use   | Monitors active memory (Endpoint DLP) |
| Network            | Data in motion| Analyzes traffic in transit         |
| Servers            | Data at rest  | Scans stored files                  |

### Key DLP Solutions
- **USB Blocking**:  
  - Controls removable media access (e.g., DoD banned USB drives after 2008 "agent.btz" worm)  
  - Managed via endpoint DLP agents  
- **Cloud-based DLP**:  
  - Sits between users and internet  
  - Blocks custom data strings, malware, and cloud storage transfers  
- **Email DLP**:  
  - Critical for inbound/outbound threats:  
    - **Inbound**: Blocks phishing, impostors, malicious keywords  
    - **Outbound**: Prevents sensitive data transmission (e.g., W-2 forms, wire transfers)  
  - Example: Boeing data leak (2016) - Hidden spreadsheet columns exposed 36k employees' PII  

---

## 💡 Key Takeaways
- **FIM** focuses on detecting *unauthorized file changes*  
- **DLP** focuses on preventing *sensitive data exfiltration*  
- Layered DLP approach (endpoint + network + cloud) is essential  
- Email remains the highest-risk vector for data leaks  
