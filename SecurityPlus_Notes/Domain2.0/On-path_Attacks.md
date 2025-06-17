# On-Path Network Attacks & ARP Poisoning

## Overview

On-path attacks (formerly known as Man-in-the-Middle) occur when an attacker secretly intercepts and possibly alters communications between two parties. Victims are typically unaware the attack is occurring.

---

## 1. What is an On-Path Attack?

- An attacker places themselves between two devices (e.g., laptop and router).
- Intercepts, monitors, and possibly modifies traffic.
- Appears invisible to both parties.
- Common technique: **ARP Poisoning**.

---

## 2. ARP Poisoning (Spoofing)

**Step-by-step flow:**

1. **Normal Operation**
   - Laptop (192.168.1.9) wants to reach router (192.168.1.1).
   - Sends ARP broadcast: "Who has 192.168.1.1?"
   - Router replies with MAC address `00:09:5b:d4:bb:fe`.
   - Laptop saves this in its ARP cache.

2. **Spoofing Begins**
   - Attacker (192.168.1.14, MAC `aa:bb:cc:dd:ee:ff`) sends unsolicited ARP reply:  
     > “I am 192.168.1.1, and my MAC is aa:bb:cc:dd:ee:ff.”
   - Laptop updates its ARP cache to associate the router's IP with the attacker's MAC.

3. **Result**
   - All traffic meant for the router is sent to the attacker.
   - Attacker can inspect, modify, or block packets.

---

## 3. On-Path Browser Attack

- Malware (Trojan) installed on the same machine as the victim.
- Proxies encrypted traffic internally.
- Captures sensitive data (e.g., bank credentials) before it is encrypted.
- **Advantage:** Works even with HTTPS, since it operates within the victim’s own browser.

**Example Attack Flow:**

- Victim opens their bank's website.
- Logs in with credentials.
- Malware intercepts this data.
- Attacker uses credentials in background to steal money or data.

---
