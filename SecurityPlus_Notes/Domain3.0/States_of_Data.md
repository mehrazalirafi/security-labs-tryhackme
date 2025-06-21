
# Summary: Data States, Sovereignty, and Geolocation

This video discusses how data is handled across different states—at rest, in transit, and in use—as well as the implications of data sovereignty and geolocation in managing data security.

---

## 📦 Data States

### 🔒 Data at Rest
- Stored on storage devices (e.g., HDDs, SSDs, USBs)
- Security via:
  - Whole disk encryption
  - Database encryption
  - File or folder-level encryption
- Controlled with permissions (e.g., access control lists)

### 🌐 Data in Transit
- Data transmitted across the network
- Vulnerable as it passes through routers, switches, etc.
- Protection includes:
  - Network-based controls (e.g., firewalls, IPS)
  - Transport encryption (e.g., TLS, IPsec)

### 🧠 Data in Use
- Actively being processed in memory (RAM, CPU cache, registers)
- Data is almost always decrypted
- High-value target for attackers
- Example: **Target breach (Nov 2013)**
  - Attackers captured decrypted credit card data from POS memory

---

## 🌍 Data Sovereignty

- Data is subject to the laws of the country where it's stored
- Legal implications: monitoring, court orders
- Regulations may dictate storage location (e.g., **GDPR** in the EU)
- Important to know: **Where is your data stored?**
  - Compliance laws may prohibit international data transfers

---

## 📍 Geolocation

- Tracks user/device location using:
  - GPS, Wi-Fi (802.11), mobile networks
- Helps manage access:
  - Restrict access from outside countries
  - Enable administrative rights only in secure areas (e.g., office buildings)
- Common use case: media streaming restrictions based on user location

---
