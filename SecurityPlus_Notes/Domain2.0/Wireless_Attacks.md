# Wireless Deauthentication and RF Jamming

## Wireless Deauthentication Attacks

- **Symptoms**: Users are unexpectedly disconnected from Wi-Fi repeatedly.
- **Cause**: An attacker sends deauthentication frames, exploiting the lack of encryption in 802.11 management frames.
- **Impact**: Users are denied access to the wireless network, creating a **Denial of Service (DoS)** condition.

### Management Frames

- 802.11 wireless uses **management frames** (e.g., association, disassociation, authentication, deauthentication).
- These are essential for network operations but were historically sent in **plaintext**, without validation or encryption.
- Example data includes SSID, MAC addresses, supported rates, and capabilities.

## Preventing Deauth Attacks

- **802.11ac and newer standards** introduced encryption for critical management frames (e.g., deauth, disassoc, channel switch).
- Some frames (beacons, probes) are still sent in the clear and visible via packet capture.

## RF Jamming

- A broader form of DoS where **interfering RF signals** disrupt Wi-Fi communication.
- Causes include:
  - Constant/random noise
  - Legitimate-looking frames
  - Microwave ovens, fluorescent lights (accidental)
  - **Intentional jamming** for malicious purposes

### Detection and Mitigation

- Requires proximity to the access point.
- Detection methods include:
  - **Fox hunting**: using a directional antenna and attenuator to trace the signal.

---
