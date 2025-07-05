# Summary of Security Logs and Monitoring

## Key Log Types and Their Importance
1. **Security Log Files**  
   - Track blocked/allowed traffic, exploit attempts, DNS sinkhole traffic  
   - Provide critical documentation of traffic flows and attack summaries  
   - Enable correlation with other logs in SIEM systems  

2. **Firewall Logs**  
   - Record source/destination IPs, ports, and traffic disposition  
   - Next-Gen Firewalls (NGFW) log applications used, URL categories, and anomalies  

3. **Application Logs**  
   - OS-specific: Windows Event Viewer, Linux/macOS `/var/log`  
   - Must be parsed/filtered in SIEMs to extract relevant security data  

4. **Endpoint Logs**  
   - Capture logon events, policy changes, processes on devices  
   - Critical for correlating IPS events with device status in SIEMs  

5. **Network Logs**  
   - From switches, routers, VPNs: routing updates, auth issues, security events  
   - Example: Automatic blocking of TCP SYN flood attacks  

6. **Metadata**  
   - Contextual data: Email headers, device GPS, file attributes  
   - Reveals hidden details (sending servers, author info, locations)  

7. **Vulnerability Scans**  
   - Identify: Missing security controls, misconfigurations (open shares), unpatched vulnerabilities  

## Security Analysis Tools
- **SIEM Systems**  
  - Centralize log correlation and analysis  
  - Enable cross-log investigation of security events  

- **Automated Reports**  
  - Generate common security summaries  
  - Require human review and careful configuration  

- **Dashboards**  
  - Real-time overview of critical security status  
  - Customizable for instant visibility (not for deep analysis)  

- **Packet Captures (e.g., Wireshark)**  
  - Analyze traffic at packet level  
  - Verify security controls and identify anomalies  

## Key Takeaways
- Log consolidation in SIEMs enables comprehensive threat detection  
- Different log types provide unique security insights (network, endpoint, application)  
- Automated tools require human oversight for effective security monitoring  
- Metadata and packet-level data offer crucial forensic context  
- Regular vulnerability scanning is essential for identifying security gaps  
