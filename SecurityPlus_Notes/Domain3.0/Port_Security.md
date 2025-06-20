# Port Security, EAP, and IEEE 802.1X – Summary

This summary outlines port-based authentication, Extensible Authentication Protocol (EAP), and 802.1X integration.

---

## 🔒 Port Security
- Authentication is required before granting network access.
- **Username and password** commonly used.
- Implemented on **wired and wireless networks**.
- Provides an additional layer of control at switch ports or access points.

---

## 🧩 Extensible Authentication Protocol (EAP)
- **Framework** for authentication (not a protocol itself).
- Supports many authentication methods defined by RFCs.
- Vendors can create custom EAP methods.
- **Integrates with 802.1X** to control access before authentication completes.

---

## 🧷 IEEE 802.1X
- Known as **Port-based Network Access Control (NAC)**.
- Blocks network access until authentication is successful.
- Works in tandem with EAP.
- Requires a backend **authentication database** (e.g., RADIUS, LDAP, TACACS+, Kerberos).

---

## 🔄 802.1X Components
- **Supplicant** – the client (e.g., user device).
- **Authenticator** – the access control device (e.g., switch or access point).
- **Authentication Server** – validates credentials (e.g., RADIUS server).

---

## 🔁 Authentication Process
1. **Initialization**: Supplicant connects, no access is allowed.
2. **EAP Request**: Authenticator asks for identity.
3. **EAP Response**: Supplicant sends identity.
4. **Access Request**: Authenticator forwards info to authentication server.
5. **Challenge/Response**: Server requests credentials, supplicant provides them.
6. **Success**: If valid, server tells authenticator to allow access.

---
