The **CIA Triad** is a foundational model in cybersecurity that outlines three primary objectives to protect information:

## 1. Confidentiality

- **Definition**: Ensuring that sensitive information is only accessible to those who are authorized to view it.
- **Goal**: Prevent unauthorized access or disclosure of data.
- **Key Mechanisms**:
  - **Encryption**: Converts data into a secure format that can only be read with the proper key.
  - **Access Controls**: Restricts access to systems or data based on roles or permissions.
  - **Two-Factor Authentication (2FA)**: Adds an extra layer of verification (e.g., password + mobile code).

---

## 2. Integrity

- **Definition**: Ensures that data remains accurate, consistent, and unaltered unless by authorized means.
- **Goal**: Detect and prevent unauthorized modifications.
- **Key Mechanisms**:
  - **Hashing**: Converts data to a fixed-length hash value to verify its integrity.
  - **Digital Signatures**: Cryptographic validation that ensures the sender is legitimate and data hasn't been changed.
  - **Certificates**: Public Key Infrastructure (PKI) tools that verify digital identities.
  - **Non-repudiation**: Guarantees that a sender cannot deny sending a message or transaction.

---

## 3. Availability

- **Definition**: Ensures that systems and data are accessible to authorized users whenever needed.
- **Goal**: Maintain uptime and system performance even during failures or attacks.
- **Key Mechanisms**:
  - **Redundancy**: Backup systems or components ready to take over if primary ones fail.
  - **Fault Tolerance**: System design that allows continued operation even when part of the system fails.
  - **Patching**: Regular updates to fix bugs, improve stability, and close vulnerabilities.
