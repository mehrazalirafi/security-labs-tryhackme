# Centralized Security Management

## 1. Active Directory (Windows Environment)
- **Centralized Database**:
  - Tracks all network resources:
    - Computers and devices
    - User accounts
    - File shares and printers
    - Security groups
- **Core Functions**:
  - Authentication: Single sign-on with AD credentials
  - Access Control: Centralized permission management
  - Account Management: Password resets, account creation/deletion
- **Administration**: Primarily managed through:
  - Active Directory Users and Computers
  - Help desk operations

## 2. Group Policy Management
- **Policy Enforcement**:
  - Applies configurations to users/computers
  - Hierarchy: Local → Domain policies
- **Management Console**:
  - Group Policy Management Editor (GPMC)
- **Key Configuration Areas**:
  | Category          | Examples                          |
  |-------------------|-----------------------------------|
  | **Login Scripts** | Drive mappings, security checks   |
  | **Network Config**| QoS settings, firewall rules      |
  | **Security**      | Password policies, access controls|
  | **System**        | Software deployment, restrictions|
- **Scope**: Hundreds of configurable options for comprehensive control

## 3. Security-Enhanced Linux (SELinux)
- **Fundamental Shift**:
  - Replaces Discretionary Access Control (DAC) with Mandatory Access Control (MAC)
- **Security Model**:
  - **Least Privilege**: Strictly limits application/system access
  - **Breach Containment**: Restricts potential damage scope
- **Implementation**:
  - Kernel-level security enhancements
  - Open-source and included in major distributions (RHEL, Fedora, CentOS)
- **Key Benefit**: Prevents privilege escalation by confining processes to minimal required access

## Implementation Comparison
| Feature          | Active Directory/Group Policy       | SELinux               |
|------------------|-------------------------------------|-----------------------|
| **Environment**  | Windows networks                    | Linux systems         |
| **Control Type** | Centralized administration          | Kernel enforcement    |
| **Auth Method**  | Credential-based                    | Process confinement   |
| **Management**   | Graphical consoles (GPMC)           | Command-line/config   |
| **Security Focus**| Access permissions                 | Application sandboxing|

## Key Takeaways
1. **Centralization Matters**: AD provides single source of truth for Windows networks
2. **Policy Enforcement**: Group Policy enables consistent security configurations
3. **Least Privilege**: SELinux implements strict MAC for critical Linux systems
4. **Hybrid Environments**: Combine AD for authentication with SELinux for Linux server protection
5. **Breach Containment**: Both systems limit attack surface through access controls
