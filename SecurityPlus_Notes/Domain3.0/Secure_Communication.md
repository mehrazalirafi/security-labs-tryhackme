# VPN, SD-WAN, and SASE - Summary

## Virtual Private Networks (VPNs)
- **Purpose**: Encrypt private data over public networks.
- **VPN Concentrator**: Handles encryption/decryption; often integrated with firewalls.
- **Deployment Options**:
  - Hardware-based or software-based
  - Client software may be integrated with OS

## Encrypted Tunnels
- **Function**: Secure data using encryption over the Internet.
- **Tunnel Mode (IPsec)**:
  - Original packet (IP Header + Data) is encrypted.
  - New IP header, IPsec headers, and trailers wrap the encrypted data.
  - Decrypted at the VPN concentrator.

## SSL/TLS VPN (Secure Sockets Layer VPN)
- **Protocol**: Uses TCP/443 (SSL/TLS), avoids firewall issues.
- **No Heavy Clients**: Can run in a browser or with lightweight clients.
- **Authentication**: Flexible—uses credentials, certificates, or shared passwords.
- **Use Case**: Remote access for individual users.
- **Always-On Option**: Automatically connects on device startup.

## Site-to-Site IPsec VPN
- **Persistent Connection**: Always-on or nearly always-on.
- **Firewalls as Endpoints**: No need for client-side configuration.
- **Use Case**: Connects entire remote sites to corporate networks.

## SD-WAN (Software Defined WAN)
- **Cloud-Oriented**: WAN built for modern cloud architectures.
- **Direct Access**: Allows remote sites to connect directly to cloud apps (bypassing data center hops).
- **Improves Efficiency**: Reduces latency and bandwidth issues for cloud services.

## SASE (Secure Access Service Edge)
- **Modern VPN Alternative**: Integrates networking and security in the cloud.
- **Security-as-a-Service**: Combines SD-WAN, firewall, threat protection, DLP, and more.
- **Close to Cloud Services**: Located near app hosting for performance.
- **Universal Clients**: Used across home, mobile, and office environments.

## Summary: Choosing Effective Controls
- **VPN**:
  - Use SSL/TLS for user access
  - Use IPsec tunnels for site-to-site connections
- **SD-WAN**:
  - Best for optimizing connectivity to the cloud
  - Lacks deep security functions alone
- **SASE**:
  - End-to-end security and network optimization
  - Requires strategic implementation
