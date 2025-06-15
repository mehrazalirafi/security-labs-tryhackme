# Common Security Misconfigurations

---

## 🔓 1. Open Permissions

- **Issue**: Misconfigured access settings leave systems exposed.
- **Example**: _June 2017 – 14 million Verizon records exposed_ via an open Amazon S3 bucket.
- **Risk**: Hackers scan cloud services for open permissions.
- **Mitigation**: Review and secure all permission settings on cloud and internal resources.

---

## 👤 2. Unsecured Admin Accounts

- **Issue**: Use of weak or default passwords on privileged accounts.
- **Common Weak Passwords**: `123456`, `ninja`, `football`
- **Mitigation**:
  - Disable direct root or admin login.
  - Use `su` or `sudo` for elevated access in Linux.
  - Use “Run as Administrator” in Windows.
  - Limit the number of accounts with administrative privileges.

---

## 📡 3. Insecure Protocols

- **Examples**: Telnet, FTP, SMTP, IMAP (transmit data in plaintext).
- **Risk**: Sensitive data can be captured using tools like Wireshark.
- **Mitigation**: Use encrypted alternatives:
  - **Telnet → SSH**
  - **FTP → SFTP**
  - **IMAP → IMAPS**
  - **HTTP → HTTPS**

---

## 🐑 4. "Wall of Sheep" at DEFCON

- **What It Shows**: Public demonstration of real credentials captured over insecure protocols.
- **Purpose**: Emphasizes the dangers of sending credentials in plaintext.
- **Lesson**: Always use secure protocols when transmitting sensitive data.

---

## ⚙️ 5. Default Settings

- **Issue**: Devices shipped with default usernames and passwords.
- **Example Tool**: **Mirai Botnet**
  - Exploits default credentials in IoT devices.
  - Targets: Cameras, routers, doorbells, etc.
  - Contains over 60 default configurations.
  - Released as open-source — accessible by attackers.
- **Mitigation**: Immediately change default credentials on all network-connected devices.

---

## 🌐 6. Open Ports and Services

- **Issue**: Services open ports that could allow external access.
- **Mitigation**:
  - Use firewalls to manage allowed traffic.
  - Carefully configure firewall rule sets (they can be complex).
  - Perform periodic audits and penetration tests.
  - Always double- and triple-check exposed ports.
