# Security Monitoring Fundamentals

## 1. Continuous Security Monitoring
- **24/7/365 Vigilance**: Attackers operate non-stop
- **Critical Monitoring Points**:
  - Authentication systems
  - Public-facing services
  - Data storage locations
  - Remote access channels
- **Real-time Response**:
  - Account access anomalies
  - Firewall rule changes
  - Triggered vulnerability scans
- **Dashboards**: Centralized view of security posture

## 2. Resource Monitoring Focus Areas
| Resource Type       | Key Monitoring Targets                              | Security Indicators                     |
|---------------------|----------------------------------------------------|-----------------------------------------|
| **Systems**         | - Authentication patterns<br>- Service activity<br>- Backup status<br>- Software versions | Unusual logins, failed backups          |
| **Applications**    | - Uptime/response times<br>- Data transfer volumes<br>- Security notifications | Traffic spikes, developer alerts        |
| **Infrastructure**  | - Remote access patterns<br>- Firewall/IPS reports<br>- Cloud services | Attack volume changes, vendor access    |

## 3. Log Management with SIEM
- **Centralized Aggregation**: Consolidates logs from:
  - Servers, firewalls, VPNs
  - Storage systems, cloud services
- **Key Capabilities**:
  - Cross-system correlation
  - Authentication tracking
  - Application access monitoring
  - Data transfer measurement
- **Example Alert**: Repeated failed root login attempts

## 4. Continuous Vulnerability Scanning
- **Why Continuous?**:
  - New threats emerge daily
  - Mobile devices change locations
  - Business applications evolve
- **Scanning Targets**:
  - OS/software versions
  - Device drivers
  - Installed applications
  - Configuration anomalies
- **Value**: Creates actionable security database

## 5. Actionable Reporting
- **Key Report Types**:
  - Patch compliance status
  - Legacy system inventory
  - Vulnerability impact analysis
- **Ad Hoc Reporting**: Prepares for unknown threats
- **Critical Question**: "How many systems are vulnerable to X?"

## 6. Long-term Archiving
- **IBM 2022 Finding**: 9-month average breach identification/containment
- **Archive Requirements**:
  - Extended retention periods
  - Compliance with legal mandates
  - Organizational security policies
- **Value**: Enables historical breach analysis

## 7. Alerting Framework
- **Critical Triggers**:
  - Authentication failures
  - Unusual data transfers
  - Security configuration changes
- **Notification Methods**:
  - SMS/text
  - Email
  - SOC dashboards
- **Actionable Principle**: Right people → Right information → Rapid response

## 8. Alert Response Process
1. **Quarantine**: Contain potential threats
2. **Tuning**: Balance alert accuracy (reduce false positives/negatives)
3. **Remediation**: Address root causes
- **Continuous Improvement**: Alert accuracy improves over time

## Key Takeaways
1. **Assume Breach**: Continuous monitoring is non-negotiable
2. **Centralize Visibility**: SIEM is essential for correlation
3. **Validate Continuously**: Regular scanning complements monitoring
4. **Archive Strategically**: Long-term data enables breach analysis
5. **Tune Alerts**: Quality over quantity in notifications
