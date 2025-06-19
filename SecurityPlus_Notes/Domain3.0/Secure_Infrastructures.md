# Summary: Network Architecture and Security Zones

This video discusses how secure network architecture is designed using zone-based concepts, device placement, and minimizing attack surfaces.

## Device Placement
- Each network is unique, but security design often shares common elements.
- **Firewalls** are key to separating trusted and untrusted zones, providing perimeter defense.
- Additional devices like **honeypots, jump servers, load balancers, and sensors** enhance security.

## Security Zones
- **Zone-based architecture** is more flexible than using IP ranges.
- Networks are divided into zones like:
  - **Trusted**
  - **Untrusted**
  - **Screened**
  - **Internal/External**
- This segmentation allows for simpler, more granular **security policies**:
  - E.g., Trusted to Untrusted, Untrusted to Screened.

## Attack Surface
- Refers to all the possible points where an attacker could enter or extract data.
- Includes vulnerabilities in:
  - Application code
  - Open ports
  - Authentication processes
  - Human error
- Strategies to **minimize attack surface**:
  - Code auditing
  - Blocking unused ports
  - Monitoring network traffic in real-time

## Connectivity and Encryption
- **Every part of the network connection contributes to security**, including physical and logical layers.
- **Secure cabling** prevents physical tampering.
- **Application-level encryption** protects data even if packets are intercepted.
- **Network-level encryption** (e.g., IPsec, VPNs) ensures secure site-to-site or remote access connections.
