# Firewall Types and Security Controls - Summary

## The Universal Security Control
- **Standard Issue**: Built into home, office, and OS environments.
- **Traffic Flow Control**: All network traffic passes through firewalls.
- **Corporate Data Governance**: Monitors outbound/inbound data for sensitive material.
- **Content Filtering**: Blocks NSFW and parental control-related content.
- **Security Features**: Integrated anti-virus and anti-malware protection.

## Network-Based Firewalls
- **Traffic Filtering**: By port or application (Layer 4 vs. Layer 7).
- **Encryption**: VPN traffic between sites.
- **Layer 3 Functionality**: Acts as a router, manages NAT, and dynamic routing.

## UTM / All-in-One Security Appliance
- **Functions**:
  - Unified Threat Management (UTM)
  - Web security gateway
  - URL/content filtering
  - Malware and spam inspection
  - Routing, switching, and CSU/DSU
  - IDS/IPS
  - Bandwidth shaping
  - VPN endpoint
- **Limitation**: Often Layer 4 only and may have performance constraints when overloaded.

## Next-Generation Firewalls (NGFW)
- **Layer 7 Focus**: Application layer awareness, inspects all data in every packet.
- **Alternate Names**:
  - Application layer gateway
  - Stateful multilayer inspection
  - Deep packet inspection
- **Capabilities**:
  - Full-packet decode
  - Application-based traffic control (e.g., SQL Server, YouTube)
  - Built-in IPS for known vulnerabilities
  - URL and content filtering

## Web Application Firewall (WAF)
- **Specialized Role**: Protects HTTP/HTTPS conversations.
- **Rules-Based Control**: Validates expected vs. unexpected input.
- **SQL Injection & XSS Detection**: Blocks typical web-based attacks.
- **Compliance Focus**: Required for PCI DSS compliance.
- **Logs**: Includes client IP, request type, country, and blocked attack types (e.g., SQLi, XSS).
