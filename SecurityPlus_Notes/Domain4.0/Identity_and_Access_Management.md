# Identity and Access Management (IAM) Summary

## 🆔 IAM Fundamentals
- **Purpose**:  
  Securely manage digital identities and resource access  
- **Key Challenges**:
  - Applications accessible anywhere (desktop/browser/mobile)
  - Data distributed across locations (cloud/on-prem)
  - Diverse user types (employees/vendors/customers)
- **Core Principle**:  
  "Right access for right people at right time"

---

## 🔑 IAM Components
| **Component**             | **Function**                                      |
|---------------------------|---------------------------------------------------|
| **Identity Lifecycle**    | Manages digital identity creation → deletion      |
| **Access Control**        | Enforces least-privilege access                  |
| **Authentication (AuthN)**| Verifies user identity (e.g., passwords, MFA)     |
| **Authorization (AuthZ)** | Determines resource permissions                  |
| **Identity Governance**   | Tracks access for compliance/auditing            |

---

## 👤 Account Management
### Provisioning/Deprovisioning
- **Trigger Events**: Hiring, transfers, promotions, separation
- **Process**:
  1. Create/remove accounts
  2. Assign attributes/group permissions
  3. Enforce least privilege (no admin by default)
- **Critical Checkpoint**: Initial access limitation

### Permission Assignments
- **Least Privilege Principle**: 
  - Only necessary access for job functions
  - Group-based permissions (e.g., "Email Users")
- **Key Restrictions**:
  - Private user storage (even on shared devices)
  - No OS privileged access for standard accounts

---

## 🕵️ Identity Proofing Process
1. **Resolution**:  
   System identifies who you claim to be
2. **Validation**:  
   User provides credentials (password, security questions)
3. **Verification/Attestation**:  
   - In-person (passport, ID check)  
   - Automated (credit reports, asset verification)  

---

## 🔐 Authentication Flows
### Standard Access Flow:
```mermaid
graph LR
    A[Client] --> B[Internet]
    B --> C{AuthN?}
    C --> D[Firewall/VPN]
    D --> E[AAA Server]
    E --> F[Internal Resources]
