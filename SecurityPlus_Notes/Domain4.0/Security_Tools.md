# Security Tools & Protocols Overview

## 1. Security Content Automation Protocol (SCAP)
- **Standardization Framework**: Unifies security tools (NGFWs, IPS, scanners)
- **Managed by NIST**: [http://scap.nist.gov](https://scap.nist.gov)
- **Key Functions**:
  - Validate security configurations
  - Confirm patch installations
  - Detect security breaches
- **Automation Benefits**:
  - Cross-tool vulnerability identification
  - Automated remediation workflows
  - Configuration compliance enforcement

## 2. Security Benchmarks
- **CIS Benchmarks**: Industry-standard configurations
  - Cover OS, cloud, mobile devices, applications
  - Example (Mobile): Disable screenshots/recordings, enforce encryption
- **Implementation**:
  - Baseline security settings
  - Continuous compliance monitoring
  - Reference: [https://www.cisecurity.org/cis-benchmarks/](https://www.cisecurity.org/cis-benchmarks/)

## 3. Monitoring Approaches
| Method        | Advantages                          | Limitations                 | Best For               |
|---------------|-------------------------------------|----------------------------|------------------------|
| **Agent-based** | Real-time monitoring<br>Detailed reporting | Requires maintenance<br>Agent updates | Critical servers<br>Compliance systems |
| **Agentless**  | No installation<br>No ongoing updates | No continuous monitoring<br>Limited detail | Temporary devices<br>Guest systems |

## 4. Core Security Technologies
- **SIEM (Security Information & Event Management)**:
  - Centralized log aggregation
  - Cross-system correlation
  - Forensic analysis capabilities
  - Long-term data storage
- **Anti-virus/Anti-malware**:
  - Modern solutions cover all malware types
  - Includes: Trojans, worms, ransomware, fileless malware
- **Data Loss Prevention (DLP)**:
  - Protects: SSNs, credit cards, medical records
  - Deployment: Endpoint clients, cloud email/storage
  - Prevents data exfiltration ("leakage")

## 5. Network Monitoring Protocols
| Protocol | Port  | Functionality                     | Use Case                     |
|----------|-------|-----------------------------------|------------------------------|
| **SNMP** | UDP/161 | Device polling<br>MIB/OID data collection | Performance monitoring<br>Health checks |
| **SNMP Traps** | UDP/162 | Threshold-based alerts<br>Proactive notifications | Critical event response<br>CRC error spikes |
| **NetFlow** | N/A   | Traffic flow analysis<br>Application usage stats | Bandwidth monitoring<br>Top talker identification |

## 6. Vulnerability Scanning
- **Key Characteristics**:
  - Minimally invasive (vs. penetration testing)
  - Identifies open ports/services
  - Detects systems and security devices
- **Scanning Strategy**:
  - External scans (attacker perspective)
  - Internal scans (insider threat focus)
  - Regular scheduling (continuous assessment)
- **Output Analysis**: Critical → High → Medium → Low prioritization

## Key Takeaways
1. **Standardize with SCAP**: Enables cross-tool automation
2. **Implement Benchmarks**: CIS provides security baselines
3. **Hybrid Monitoring**: Combine agent/agentless approaches
4. **Centralize Visibility**: SIEM essential for correlation
5. **Layer Defenses**: AV, DLP, and scanning complement each other
6. **Monitor Proactively**: SNMP traps/NetFlow provide network insights
