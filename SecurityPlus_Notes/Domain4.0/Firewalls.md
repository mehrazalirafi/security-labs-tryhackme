# Firewalls & Intrusion Prevention Systems

## 1. Firewall Types
| Type              | OSI Layer | Key Capabilities                          | Limitations                  |
|-------------------|-----------|------------------------------------------|------------------------------|
| **Traditional**   | L3-L4     | Port/protocol filtering<br>NAT<br>VPN    | No application awareness     |
| **NGFW**          | L7        | Deep packet inspection<br>Application ID<br>SSL decryption | Higher resource requirements |

## 2. Firewall Rule Principles
- **Processing Order**: Top-to-bottom evaluation
- **Rule Specificity**: Most specific rules at top
- **Implicit Deny**: Automatic deny for unmatched traffic
- **ACL Components**:
  - Source/Destination IP
  - Port numbers
  - Protocol (TCP/UDP/ICMP)
  - Time restrictions
  - Application identification (NGFW)

## 3. Web Server Firewall Ruleset Example
| Rule | Remote IP | Remote Port | Local Port | Protocol | Action | Service      |
|------|-----------|-------------|------------|----------|--------|--------------|
| 1    | All       | Any         | 22         | TCP      | Allow  | SSH          |
| 2    | All       | Any         | 80         | TCP      | Allow  | HTTP         |
| 3    | All       | Any         | 443        | TCP      | Allow  | HTTPS        |
| 4    | All       | Any         | 3389       | TCP      | Allow  | RDP          |
| 5    | All       | 53          | Any        | UDP      | Allow  | DNS          |
| 6    | All       | 123         | Any        | UDP      | Allow  | NTP          |
| 7    | All       | Any         | Any        | ICMP     | Deny   | Ping         |

## 4. Network Segmentation
- **Screened Subnet (DMZ)**:
  - Isolates public-facing services
  - Protects internal networks
  - Dual-firewall architecture:
    ```
    Internet → Firewall → Screened Subnet → Firewall → Internal Network
    ```

## 5. Intrusion Prevention Systems (IPS)
- **Detection Methods**:
  - **Signature-based**: Exact pattern matching (e.g., Conficker worm)
  - **Anomaly-based**: Deviations from established baselines
- **Integration**: Typically embedded in NGFWs
- **Rule Customization**:
  - Thousands of pre-configured rules
  - Group-based management
  - Actions: Block, Allow, Alert

## 6. IPS Rule Management Challenges
- **Alert Tuning**: Balancing security vs. false positives
- **Rule Maintenance**: Regular updates for new threats
- **Performance Impact**: Processing overhead for deep inspection
- **Customization Needs**: Environment-specific tuning

## Key Takeaways
1. **Layer Defense**: Combine traditional firewalls with NGFW/IPS
2. **Rule Optimization**: Place specific rules first with implicit deny
3. **Segment Networks**: Use DMZs for public services
4. **Tune Proactively**: Regularly adjust IPS rules to reduce false positives
5. **Inspect Deeply**: Leverage NGFW application awareness for better security
