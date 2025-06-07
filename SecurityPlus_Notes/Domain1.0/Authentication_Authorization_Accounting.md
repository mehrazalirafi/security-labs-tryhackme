
# 🔐 AAA Framework & Authentication Models

---

## AAA Framework Overview

- **Identification**: Declares who you are (e.g., your username).
- **Authentication**: Proves your identity (e.g., password, biometrics).
- **Authorization**: Determines what access you’re granted based on ID and authentication.
- **Accounting**: Logs activity (e.g., login/logout times, data usage).

---

## 👤 Authenticating People

- **Flow**:
  - A client connects over the Internet.
  - A firewall/VPN concentrator asks the AAA server to authenticate the user.
  - If credentials are valid, access is granted to internal services.
- **Key Concept**: Authentication is a gatekeeper for internal resources.

---

## 💻 Authenticating Systems

- **Challenges**:
  - Devices may be remote and unmanaged.
  - Systems can’t type passwords.
- **Solution**: Use **digitally signed certificates** on devices.
- **Use Case**: VPN access, endpoint validation by management software.

---

## 🔐 Certificate Authentication

- Organizations use a **Certificate Authority (CA)** to issue digital certificates.
- Each device gets a unique certificate signed by the CA.
- The certificate is stored on the device and used as an authentication factor.
- **Validation**: The CA’s digital signature proves the certificate is trustworthy.

---

## 🔄 Certificate-Based Authentication Process

1. **Device** holds a certificate signed by a CA.
2. **CA certificate** is trusted because it’s signed by a root authority.
3. During authentication, the system checks:
   - Device cert → signed by CA
   - CA cert → signed by root
   - **Result**: Chain of trust is established.

---

## 🗝️ Authorization Models

### No Authorization Model

- **Direct Mapping**: User → Resource
- **Problems**:
  - Difficult to manage.
  - Doesn’t scale.
  - Hard to understand access reasons.

### Using an Authorization Model

- **Add Abstraction**: User → Role → Resource
- **Advantages**:
  - Reduces complexity.
  - Easier to manage.
  - Scales well for many users/devices.

- **Example**:
  - Role: `Shipping and Receiving`
  - Permissions: `Create shipping labels`, `Track shipments`, `View reports`
