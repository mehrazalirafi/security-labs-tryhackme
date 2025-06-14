# Hardware and Firmware Vulnerabilities Summary

## Hardware Vulnerabilities
- We are surrounded by **hardware devices**, many of which lack accessible operating systems.
- These can serve as **entry points** for attacks.
- The rise of **IoT devices** (e.g., smart bulbs, locks, garage doors) means everything is now network-connected.
- The **attack surface** has expanded—traditional defenses need to adapt.

## Firmware
- **Firmware** is the software (OS) inside hardware devices.
- Only **vendors** can patch firmware, assuming they know or care about the issue.
- Example: **Trane Comfortlink II thermostats**
  - 3 vulnerabilities reported in April 2014.
  - First patch: April 2015; Final: January 2016.
  - Demonstrates **slow vendor response** and extended exposure.

## End-of-Life (EOL) and End-of-Service-Life (EOSL)
- **EOL**: Manufacturer stops selling a product but may still support it.
- **EOSL**: No more support or security patches.
- EOSL devices are a **major risk** as no further protections are provided.
- Premium-cost support may exist but is impractical for most.

## Legacy Platforms
- Devices/software often **stay in use too long** (legacy systems).
- May run **EOL/EOSL software** (OS, apps, middleware).
- Risk vs. return must be assessed.
- May require:
  - **Extra firewall rules**.
  - **IPS signatures** for outdated software.
- Mitigation strategies are essential until full replacement is possible.
