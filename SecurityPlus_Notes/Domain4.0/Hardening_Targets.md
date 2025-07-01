# System Hardening Guide
> *Security principles for technology infrastructure*  

## Core Principles
- 🛡️ **Never trust defaults**: Always reconfigure security settings
- 🔄 **Patch aggressively**: Prioritize updates for exposed systems
- 🔀 **Segment everything**: Limit lateral movement
- 🔐 **Enforce least privilege**: Minimal access for accounts/services
- 📚 **Leverage vendor guides**: Manufacturer hardening docs first

---

## Device-Specific Hardening
| System Type          | Key Risks                  | Critical Hardening Steps                     |
|----------------------|---------------------------|---------------------------------------------|
| **Mobile Devices**   | Physical vulnerability    | • MDM enforcement<br>• Data containerization<br>• Automatic OS updates |
| **Workstations**     | User-installed software   | • Automated patching (OS/apps)<br>• Uninstall unused software<br>• Group Policy enforcement |
| **Network Gear**     | Default credentials       | • RADIUS/TACACS+ auth<br>• Management VLANs<br>• Firmware updates |
| **Cloud Infrastructure** | Overprivileged access | • Harden management workstations<br>• C2C backups<br>• EDR on all endpoints |
| **Servers**          | Unpatched services        | • Service pack updates<br>• Host-based firewalls<br>• Account lockout policies |
| **SCADA/ICS**        | Safety system compromise  | • Air-gapped networks<br>• Physical access controls<br>• Zero internet access |
| **Embedded Systems** | Difficult patching        | • Immediate security updates<br>• Service minimization<br>• Default credential replacement |
| **RTOS**             | Schedule manipulation     | • Deterministic process isolation<br>• Encrypted communications<br>• Host-based firewalls |
| **IoT Devices**      | Weak defaults             | • Dedicated VLANs<br>• Default password changes<br>• Firmware update priority |

---

## Implementation Checklist
1. **Assess** inventory and risk exposure
2. **Prioritize** critical infrastructure (servers/network first)
3. **Automate** patching and configuration management
4. **Segment** networks (VLANs/firewalls)
5. **Validate** backups before major changes
6. **Monitor** with EDR/IDS solutions
