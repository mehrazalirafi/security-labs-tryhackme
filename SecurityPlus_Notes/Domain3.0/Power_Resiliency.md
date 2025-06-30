# Power Resiliency Summary

## Importance of Power Resiliency
- Power is the foundation of all technology systems
- Critical to engineer for outages (minutes to days)
- Power typically provided by third parties (uncontrollable availability)
- Requires mitigation strategies for:
  - Short outages (minutes/hours)
  - Long-term issues (natural disasters)

---

## Uninterruptible Power Supply (UPS)
### Core Function
- Short-term backup power for:
  - Blackouts (complete power loss)
  - Brownouts (voltage drops)
  - Surges (voltage spikes)

### UPS Types
| Type | Functionality | Use Case |
|------|---------------|----------|
| **Offline/Standby** | Switches to battery when main power fails | Basic protection |
| **Line-interactive** | Adjusts voltage during brownouts | Areas with frequent voltage fluctuations |
| **On-line/Double-conversion** | Continuously runs on battery power | Critical systems (no transfer delay) |

### Key Features
- Automatic system shutdown before battery depletion
- Configurable battery capacity (runtime varies by load)
- Multiple outlet options
- Phone/Ethernet line surge suppression

---

## Generators
### Core Function
- Long-term power backup (hours/days)
- Requires fuel storage (diesel, natural gas, etc.)

### Implementation
- Powers entire buildings or designated circuits
- Generator-powered outlets often specially marked
- Typical startup time: 1-2 minutes

### Critical Consideration
- **Use UPS during generator startup** to bridge power gap

---

## Power Backup Strategy
```mermaid
graph LR
A[Power Outage] --> B{UPS Activates}
B --> C{Outage Duration}
C -->|Short-term| D[UPS Maintains Systems]
C -->|Long-term| E[Generator Starts]
E --> F[UPS Covers Startup Gap]
F --> G[Generator Powers Systems]
