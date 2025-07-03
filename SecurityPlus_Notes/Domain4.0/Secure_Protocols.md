# Securing Network Communications

## 1. Unencrypted Protocol Risks
- **Vulnerable Protocols**:
  - Telnet (remote access)
  - FTP (file transfer)
  - SMTP/IMAP (email)
  - HTTP (web traffic)
- **Threat**: All traffic sent in clear text → Credential theft, data interception
- **Verification Method**: Packet capture analysis

## 2. Secure Protocol Alternatives
| Application        | Insecure Protocol | Secure Protocol | Encryption Method |
|--------------------|-------------------|-----------------|-------------------|
| Remote Access      | Telnet            | SSH             | AES, ChaCha20     |
| Web Browsing       | HTTP              | HTTPS           | TLS 1.2/1.3       |
| Email Access       | IMAP/POP3         | IMAPS/POP3S     | SSL/TLS           |
| File Transfer      | FTP               | SFTP/FTPS       | SSH/TLS           |
| Directory Services | LDAP              | LDAPS           | TLS               |

## 3. Port Selection & Security
- **Common Port Mappings**:
  - HTTP: 80 (unencrypted)
  - HTTPS: 443 (encrypted)
  - SMTP: 25 vs SMTPS: 465/587
  - IMAP: 143 vs IMAPS: 993
- **Critical Considerations**:
  - Port ≠ Security: Configured encryption is essential
  - Verification: Always confirm encryption via packet capture
  - Default Ports: Can be changed but complicates security

## 4. Transport-Level Encryption
| Method               | Implementation                     | Security Level         | Use Cases                 |
|----------------------|------------------------------------|------------------------|---------------------------|
| **WPA3 Wireless**    | Device-level encryption            | Strong (AES-256)       | Office/remote work        |
| **VPN Tunneling**    | End-to-end encrypted connection    | Very strong (IPsec)    | Remote access, site links |
| **MACsec (802.1AE)** | Link-layer encryption              | Strong                 | Data center interconnects |
| **TLS Everywhere**   | Application-specific implementation| Varies by configuration| Web/app communications    |

## VPN Implementation
```mermaid
graph LR
    A[Remote User] -->|Encrypted<br>Tunnel| B[VPN Concentrator]
    B --> C[Corporate Network]
    C --> D[Internet Resources]
