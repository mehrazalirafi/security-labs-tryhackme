# Password Management & Authentication Summary

## 🔐 Password Security Fundamentals
- **Complexity Requirements**:
  - Mix uppercase/lowercase, numbers, special characters
  - Avoid dictionary words & predictable patterns
  - Minimum 8+ characters (increasing with computing power)
- **Password Entropy**: Measures unpredictability against brute-force attacks
- **Modern Approach**: Use passphrases (e.g., `CorrectHorseBatteryStaple!`)

---

## ⏳ Password Lifecycle Management
| **Aspect**        | **Standard Practice**       | **Critical Systems**      |
|--------------------|-----------------------------|---------------------------|
| **Expiration**     | 30-90 days                  | 7-15 days                 |
| **History Policy** | Prevent reuse (5+ passwords)| Stricter rotation         |
| **Age Monitoring** | Warn before expiration      | Enforced immediate change |

---

## 🔑 Password Management Solutions
### Password Managers
- **Function**: Securely store unique passwords per account
- **Security Features**:
  - AES-256 encryption
  - MFA protection
  - Automatic password generation
- **Types**:
  - **Personal**: Built into OS/browsers (iCloud Keychain, Chrome Password Manager)
  - **Enterprise**: Centralized control/recovery (1Password Teams, LastPass Enterprise)

### Passwordless Authentication
- **Methods**:
  - Biometrics (Face ID, Touch ID)
  - Security keys (FIDO2)
  - PIN-based login
- **Benefits**:
  - Eliminates password reuse risks
  - Reduces phishing vulnerability
- **Implementation**:
  - Often paired with MFA (e.g., Windows Hello + PIN)

---

## ⚡ Just-in-Time (JIT) Permissions
### Core Principles
1. **Least Privilege Enforcement**: No permanent admin rights
2. **Ephemeral Access**: Time-limited credentials
3. **Breach Containment**: Limits attack surface

### Implementation Workflow:
```mermaid
graph LR
    A[User Request] --> B[Central Policy Engine]
    B --> C{Approved?}
    C -->|Yes| D[Generate Temp Credentials]
    D --> E[Time-bound Access]
    E --> F[Automatic Revocation]
    C -->|No| G[Access Denied]
