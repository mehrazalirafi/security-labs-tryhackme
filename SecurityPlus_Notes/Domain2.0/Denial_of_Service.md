
# Denial of Service (DoS) and Distributed Denial of Service (DDoS) Attacks

## Denial of Service (DoS)

- **Force a service to fail**
  - Overload the service

- **Exploit vulnerabilities**
  - Take advantage of a design failure
  - Keep systems patched!

- **Make a system unavailable**
  - For competitive advantage

- **Smokescreen for another exploit**
  - Example: DNS spoofing

- **Simple DoS**
  - Just turn off the power

---

## Friendly DoS (Unintentional)

- **Unintentional DoSing**
  - Not always caused by an attacker

- **Network DoS**
  - Layer 2 loop without STP

- **Bandwidth DoS**
  - Large downloads over small bandwidth (e.g., Linux distro over DSL)

- **Physical causes**
  - Water line breaks in data center

---

## Distributed Denial of Service (DDoS)

- **Multiple devices used**
  - Overwhelm bandwidth or system resources

- **Botnets**
  - Thousands/millions of infected systems
  - Example: Zeus botnet (3.6 million PCs)

- **Asymmetric threat**
  - Attacker needs fewer resources than the victim

---

## DDoS Reflection and Amplification

- **Amplify small attacks**
  - Reflect requests off public devices/services

- **Turn internet against the victim**
  - Misuse of open protocols (e.g., NTP, DNS, ICMP)

- **Protocol abuse**
  - Minimal checks on these protocols

---

## DNS Amplification DDoS

- **Amplified response from DNS**
  - Small query (e.g., 15 bytes)
  - Large response (e.g., 1300 bytes)
  - Amplification ratio ~86x

### Attack Steps:
1. Botnet receives command from C&C
2. Sends spoofed DNS queries to open resolvers
3. DNS servers respond to the victim’s IP
4. Victim is overwhelmed by amplified traffic
