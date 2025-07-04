# Access Control Models Summary

## 🔐 Core Concepts
- **Authorization**: Policy enforcement determining resource access rights
- **Least Privilege Principle**:  
  - Minimum permissions required for job functions
  - Applies to both users and applications
  - Critical for limiting attack surfaces

---

## 🧩 Access Control Models
| **Model** | **Control Mechanism** | **Key Characteristics** | **Security Level** | **Common Use Cases** |
|-----------|------------------------|-------------------------|--------------------|----------------------|
| **MAC**<br>(Mandatory) | OS-enforced labels | <ul><li>Predefined security levels (Confidential/Secret/Top Secret)</li><li>Admin-controlled permissions</li><li>Users cannot modify</li></ul> | ⭐⭐⭐⭐⭐ | Military, government systems |
| **DAC**<br>(Discretionary) | Data owner decisions | <ul><li>Owner controls access permissions</li><li>Flexible but user-dependent</li><li>Common in OS (Windows/macOS/Linux)</li></ul> | ⭐⭐ | General business environments |
| **RBAC**<br>(Role-Based) | Organizational roles | <ul><li>Permissions tied to job functions</li><li>Group-based implicit permissions</li><li>Centralized administration</li></ul> | ⭐⭐⭐⭐ | Enterprise corporate networks |
| **ABAC**<br>(Attribute-Based) | Multiple contextual factors | <ul><li>Considers: IP, time, action type, data relationship</li><li>"Next-gen" contextual awareness</li><li>Complex rule combinations</li></ul> | ⭐⭐⭐⭐⭐ | Cloud environments, modern applications |
| **Rule-Based** | System-enforced policies | <ul><li>Admin-defined conditions (non-user)</li><li>Applied to objects via ACLs</li><li>Examples: browser restrictions, time limits</li></ul> | ⭐⭐⭐ | Network access controls |

---

## ⏰ Time-of-Day Restrictions
- **Implementation**:
  - Common in security devices
  - Rarely standalone control
- **Examples**:
  - Training room network: Midnight-6AM blocked
  - Conference rooms: Limited after 8PM
  - R&D databases: 8AM-6PM only
- **Challenges**:
  - Complex in 24/7 environments
  - Timezone considerations for global organizations

---

## 🔑 Key Principles
1. **Least Privilege is Fundamental**  
   - Never grant administrative rights unnecessarily
2. **Model Selection Depends on**:
   - Business requirements
   - Security sensitivity
   - Administrative overhead
3. **Hybrid Approaches**:
   - Combine models (e.g., RBAC + Time Restrictions)
   - ABAC as evolution of rule-based systems
4. **Enforcement Methods**:
   - System-level (MAC)
   - Owner-controlled (DAC)
   - Policy-driven (RBAC/ABAC)
