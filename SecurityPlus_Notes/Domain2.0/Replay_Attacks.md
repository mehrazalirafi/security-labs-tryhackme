# Replay Attacks and Session Hijacking

## Replay Attack

- **What it is**: An attacker captures data from a network and reuses it to impersonate a user.
- **How it's done**:
  - Requires access to **raw network data**.
  - Techniques: Network tap, ARP poisoning, or **malware** on the victim's machine.
- **Goal**: Use captured data to trick the system into thinking the attacker is a legitimate user.
- **Important Note**: Replay is *not* an on-path attack—replay doesn’t need to happen in real time.

---

## Pass-the-Hash

- **Definition**: A type of replay attack where the attacker uses the *hashed* version of a password to authenticate without knowing the plaintext.
- **Flow**:
  1. Client authenticates to server, sending a username + hashed password.
  2. Attacker captures that transmission.
  3. Attacker reuses the hash to gain access.
- **Defense**:
  - Use **salts** or session-based hashes.
  - Ensure servers don’t accept reused hashes.

---

## Cookies and Session IDs

- **Cookies**: Small files stored by the browser to manage sessions and preferences.
- **Uses**: Tracking, personalization, and **session management**.
- **Risks**:
  - Not executable but can leak **sensitive data**.
  - Includes session IDs, usernames, and other identifiers.
- **Session IDs**:
  - Stored in cookies.
  - Maintain sessions across page reloads or browser tabs.

---

## Session Hijacking (Sidejacking)

- **What it is**: An attacker steals a **session ID** to impersonate a user.
- **How it works**:
  1. Victim logs in and gets a session ID.
  2. Attacker captures that ID (e.g., via packet sniffing).
  3. Attacker uses the session ID to gain access to the server as the victim.
- **Impact**: Full access to the victim’s authenticated session.

---

## Header Manipulation

- **Information gathering tools**: Wireshark, Kismet.
- **Exploits**: XSS (Cross-site Scripting) can expose session data.
- **Tools for modification**:
  - Modify headers: Tamper, Firesheep, Scapy.
  - Modify cookies: Cookies Manager+ (Firefox add-on).

---

## Prevention Strategies

### 🔒 Encrypt End-to-End

- Prevents session ID capture.
- Requires HTTPS.
- Tools: HTTPS Everywhere, Force-TLS (Firefox).

### 🔐 Encrypt End-to-Somewhere

- Use **VPN** to secure traffic on public or local networks.
- Still leaves traffic exposed past the VPN endpoint.

---
