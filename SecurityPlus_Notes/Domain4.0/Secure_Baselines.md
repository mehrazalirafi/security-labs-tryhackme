# Secure Baselines Summary

## Definition & Purpose
- **Standardized security configurations** for application environments
- Ensures consistent security posture across all instances
- Covers:
  - Firewall settings
  - Patch levels
  - OS file versions
  - Application configurations
- Requires periodic integrity checks and updates

---

## Establishing Baselines
1. **Create foundational policies**:
   - Start with manufacturer recommendations:
     - OS vendors (e.g., Microsoft)
     - Application developers
     - Appliance manufacturers
   - Example: Windows 10 has >3,000 group policy settings (security subset)

2. **Leverage existing frameworks**:
   - Microsoft Security Compliance Toolkit (SCT)
   - CIS Benchmarks
   - NIST guidelines
   - MDM security baselines (for mobile devices)

---

## Deployment Methods
| Method | Use Case | Tools |
|--------|----------|-------|
| **Group Policy** | Windows domains | Active Directory |
| **MDM** | Mobile/cloud devices | Microsoft Intune |
| **Configuration Managers** | Enterprise-scale | Microsoft Configuration Manager |
| **Scripting/Automation** | Large deployments | PowerShell, Ansible |

**Key Requirement**: Centralized management console for consistency

---

## Maintenance Lifecycle
```mermaid
graph TD
A[Baseline Creation] --> B[Deployment]
B --> C[Continuous Monitoring]
C --> D{Change Needed?}
D -->|Yes| E[Update & Test]
D -->|No| C
E --> B
