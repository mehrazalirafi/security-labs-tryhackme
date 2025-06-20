# Network Security Appliances – Summary

This summary covers key concepts on network infrastructure appliances including jump servers, proxies, load balancers, and SIEM systems.

---

## 🔐 Jump Server
- Provides secure access to protected network zones.
- Requires SSH, VPN, or tunneling.
- Acts as a gateway to internal resources.
- Must be **hardened and monitored**.
- **Critical risk** if compromised.

---

## 🌐 Proxy Server
- Acts as an intermediary between users and external resources.
- Can **cache content**, **filter URLs**, and **scan for threats**.
- **Types:**
  - **Explicit Proxy:** Client configures the proxy manually.
  - **Transparent Proxy:** Proxy is invisible to client.

---

## 🧠 Application Proxy
- Understands and interprets **application-specific protocols**.
- Examples: HTTP, HTTPS, FTP.
- May be **single-purpose** or **multipurpose**.

---

## 🔁 Forward Proxy
- Internal proxy used to control **outbound** traffic.
- Users connect to the proxy which then queries the external website.

---

## 🔄 Reverse Proxy
- Manages **inbound** traffic to internal services.
- Protects web servers from direct exposure.
- Can cache repeated external requests.

---

## 🌍 Open Proxy
- **Untrusted**, publicly available proxy.
- Can be used to **bypass security controls**.
- High **security risk** due to unknown management.

---

## ⚖️ Load Balancer
- Distributes network traffic across multiple servers.
- Improves performance and fault tolerance.

### Active/Active
- All servers are active.
- Balances traffic among all nodes.

### Active/Passive
- Some servers are on standby.
- Failover occurs if an active node goes down.

### Features:
- TCP Offload
- SSL Offload
- Caching
- Prioritization (QoS)
- Content Switching

---

## 📡 Sensors and Collectors
- **Sensors** gather logs and traffic info (IPS, firewall, etc.).
- **Collectors** centralize logs (SIEM, syslog).
- **SIEMs** offer:
  - Data correlation
  - Event analysis
  - Reporting dashboards

---

## 📊 Example: SIEM Dashboard
- Visual reports showing:
  - Failed authentications
  - Port scans
  - HTTP access attempts
- Aggregated data from multiple sources for analysis.

---
