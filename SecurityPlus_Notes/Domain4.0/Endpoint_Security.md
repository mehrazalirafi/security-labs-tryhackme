# Endpoint Security & Threat Response Summary

## 🔒 Endpoint Protection Fundamentals
- **Definition**: User-facing devices (desktops, laptops, mobiles) accessing applications/data
- **Key Threats**:
  - Inbound attacks (exploits)
  - Outbound attacks (data exfiltration)
- **Defense Strategy**: 
  - Multi-layered protection (defense-in-depth)
  - Cross-platform coverage (Windows, macOS, Linux, iOS, Android)

---

## 🌐 Edge Control vs. Access Control
| **Control Type** | **Location**      | **Management**                     | **Characteristics**          |
|------------------|-------------------|------------------------------------|------------------------------|
| **Edge Control** | Network perimeter | Firewall rules                     | Static, rarely changes       |
| **Access Control**| Anywhere (inside/outside) | User/group/location/application rules | Dynamic, easily revoked/changed |

---

## 🩺 Posture Assessment (Device Health Checks)
### Why Required?
- BYOD (Bring Your Own Device) risks
- Malware infections
- Unauthorized applications
- Missing security controls

### Key Checks:
- Trusted device status
- Antivirus status & update level
- Corporate application compliance
- Disk encryption (especially mobiles)
- OS-agnostic (all platforms covered)

### Assessment Methods:
| **Method**         | **Installation**       | **Operation**                                  | **Limitations**          |
|---------------------|------------------------|-----------------------------------------------|--------------------------|
| Persistent Agents   | Permanent              | Runs anytime, monitors files/apps             | Requires regular updates |
| Dissolvable Agents  | Temporary (no install) | Runs during assessment, self-terminates       | Limited to assessment   |
| Agentless NAC       | None (AD-integrated)   | Runs at Active Directory login/logoff         | Cannot be scheduled      |

### ❌ Handling Assessment Failure:
1. Quarantine device to restricted network
2. Notify administrators
3. Provide limited access for remediation
4. Re-assess after fixes

---

## 🛡️ Threat Detection & Response
### EDR (Endpoint Detection and Response)
- **Core Functions**:
  - Detect (behavioral analysis, ML, process monitoring)
  - Investigate (root cause analysis)
  - Respond (auto-isolate/quarantine/rollback)
- **Deployment**: Lightweight endpoint agent
- **Key Advantage**: Automated response (no technician needed)

### XDR (Extended Detection and Response)
- **Evolution Beyond EDR**:
  - Correlates endpoint + network + cloud data
  - Reduces false positives/missed detections
  - Accelerates investigations
- **Enhanced Capabilities**:
  - Network anomaly detection
  - Cloud activity monitoring

### 👤 User Behavior Analytics (UBA)
- **Function**: Baseline normal activity → detect anomalies
- **Monitoring Scope**:
  - User actions
  - Host activities
  - Network traffic patterns
  - Data repository access
- **Detection Methods**:
  - Rule-based policies
  - Statistical analysis
  - Real-time pattern matching

---

## 🔑 Key Takeaways
- **Defense-in-depth** is essential for endpoint security
- **Access control** must be dynamic; **edge control** remains static
- **Posture assessments** are critical for BYOD environments
- **XDR** > EDR through cross-data correlation
- **Automated response** significantly reduces threat impact time
