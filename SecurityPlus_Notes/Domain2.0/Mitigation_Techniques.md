# Mitigation Techniques – Video Summary

This discusses various mitigation techniques used to reduce the impact of security events in an IT environment.

## 1. Patching
- **Importance**: Essential for system stability and fixing security vulnerabilities.
- **Monthly Updates**: Incremental and vital for system health.
- **Third-party Updates**: Issued by app developers and device manufacturers.
- **Auto-update**: Convenient but not always ideal in enterprise environments.
- **Emergency Patches**: Out-of-band updates may be necessary for active vulnerabilities.

## 2. Encryption
- **Purpose**: Prevent unauthorized access to application data.
- **File-level Encryption**: Encrypting individual files (e.g., Windows EFS).
- **Full Disk Encryption (FDE)**: Encrypts the entire drive (e.g., BitLocker, FileVault).
- **Application Data Encryption**: Managed by apps; ensures data remains secure regardless of storage method.

## 3. Monitoring
- **Goal**: Detect and log security events across systems.
- **Sources**: Firewalls, switches, routers, servers, etc.
- **SIEM**: Centralized log and event management using Security Information and Event Management systems.
- **Benefits**: Enables quick detection, correlation, and analysis of incidents.

## 4. Least Privilege
- **Principle**: Users only receive permissions necessary for their roles.
- **Account Limitation**: Applications and users should operate with minimal rights.
- **Admin Rights**: Restricting administrative privileges limits potential damage from threats.

## 5. Configuration Enforcement
- **Posture Assessment**: Checks device status during login.
- **Checks**:
  - OS patches
  - EDR version
  - Firewall status
  - Certificate validity
- **Non-compliant Devices**: Moved to restricted VLANs until compliant.

## 6. Decommissioning
- **Policy**: Must follow formal procedures.
- **Focus**: Typically on storage devices like HDDs, SSDs, USB drives.
- **Methods**: Recycle for internal use or physically destroy to prevent data recovery.

---
