# Wireless & Mobile Security Hardening Guide

## Core Security Principles
- **Encryption First**: All wireless/cellular data must be encrypted
- **Zero Trust Access**: Treat all connections as potentially hostile
- **Continuous Monitoring**: Regularly scan for rogue devices/access points
- **Policy Enforcement**: MDM mandatory for all business-access devices

---

## Key Security Areas

### 📶 Wireless Network Security
1. **Site Surveys**
   - Conduct pre-deployment spectrum analysis
   - Identify existing APs and interference sources
   - Create signal **heat maps** for coverage optimization
   - Schedule quarterly re-surveys

2. **Wi-Fi Hardening**
   - WPA3 encryption mandatory
   - Disable WPS and legacy protocols
   - Separate guest/corporate networks (VLAN isolation)
   - Monitor for:
     - Rogue access points
     - Evil twin attacks
     - Deauthentication attacks

3. **Survey Tools**
   - Built-in OS utilities for basic scanning
   - Third-party tools (NetSpot, Ekahau) for advanced analysis
   - Spectrum analyzers for non-WiFi interference detection

### 📱 Mobile Device Strategies
| Model       | Ownership     | Key Security Controls                  |
|-------------|---------------|----------------------------------------|
| **BYOD**    | Employee      | • MDM-enforced containerization<br>• Remote wipe capability<br>• Automatic compliance checks |
| **COPE**    | Corporate     | • Full device control<br>• Personal/corp data partitioning<br>• Selective remote wipe |
| **CYOD**    | Corporate     | • User-selected from approved list<br>• Standardized security profile<br>• Mandatory MDM enrollment |

### 📡 Connectivity Security
| Technology | Risks                  | Hardening Measures                     |
|------------|------------------------|----------------------------------------|
| **Cellular** | • Location tracking<br>• IMSI catching<br>• Base station spoofing | • VPN mandatory<br>• Disable unused services (hotspot)<br>• Monitor for unusual data usage |
| **Bluetooth** | • Bluejacking<br>• Bluesnarfing<br>• Unauthorized pairing | • Disable when unused<br>• Non-discoverable mode<br>• Reject unprompted pairing requests<br>• Limit paired device list |
| **Wi-Fi**    | • On-path attacks<br>• Packet sniffing<br>• Evil twins | • Always use VPN<br>• Disable auto-connect<br>• Certificate-based authentication<br>• Network access control (NAC) |

---

## Mobile Device Management (MDM) Essentials
- **Policy Enforcement**:
  - Mandatory device encryption
  - Screen lock requirements (biometrics/PIN)
  - App whitelisting/blacklisting
- **Data Protection**:
  - Containerization for corporate data
  - Selective wipe capabilities
  - Disable removable media
- **Access Control**:
  - Geo-fencing restrictions
  - Context-aware authentication
  - Jailbreak/root detection
- **Lifecycle Management**:
  - Automated provisioning/deprovisioning
  - Lost device tracking
  - Remote lock/wipe

---

## Implementation Checklist
1. [ ] Perform comprehensive wireless site survey
2. [ ] Deploy MDM solution with BYOD/COPE policies
3. [ ] Encrypt all wireless connections (WPA3 Enterprise)
4. [ ] Segment networks: Corporate/Guest/IoT
5. [ ] Disable legacy protocols (WEP, WPS)
6. [ ] Enforce VPN for all remote/mobile connections
7. [ ] Establish device retirement/recycling procedures
8. [ ] Train users on Bluetooth/Wi-Fi security risks
9. [ ] Implement cellular data monitoring
10. [ ] Schedule quarterly security audits

## Critical Maintenance Practices
- **Monthly**: 
  - Review MDM compliance reports
  - Audit paired Bluetooth devices
- **Quarterly**:
  - Re-run wireless site surveys
  - Update BYOD/COPE acceptance policies
  - Test remote wipe capabilities
- **Annually**:
  - Review cellular carrier security
  - Refresh encryption certificates
  - Validate incident response plans

## Security Resources
- NIST SP 800-48 (Wireless Security)
- OWASP Mobile Security Testing Guide
- GSMA Mobile Security Guidelines
- CIS Wireless Access Points Benchmark
