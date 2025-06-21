
# Data Security Concepts – Summary

This document summarizes the key data security concepts.

---

## Geographic Restrictions

- **Network Location**: Uses IP subnet to identify location; less effective on mobile devices.
- **Geolocation**:
  - GPS: Most accurate on mobile devices.
  - 802.11 Wireless: Moderately accurate using SSID databases.
  - IP Address: Least accurate.
- **Geofencing**: 
  - Controls access based on location.
  - Example: Restrict app use to inside the corporate office.

---

## Protecting Data

- **Primary Task**: Organizations rely on secure, accessible data.
- **Ubiquity of Data**: Stored on drives, networks, and CPUs.
- **Data Protection Measures**:
  - Use of encryption.
  - Security policies.
  - Access permissions.

---

## Encryption

- **Definition**: Converts plaintext to unreadable ciphertext.
- **Reversible**: Requires the correct key for decryption.
- **Confusion**: Ciphertext is drastically different from plaintext.
- **Example**: "Hello, world." encrypted using PGP becomes unreadable ciphertext.

---

## Hashing

- **Purpose**: Converts data into a short, fixed string.
- **One-Way**: Cannot recover original data.
- **Use Cases**:
  - Store passwords.
  - Verify file integrity.
  - Digital signatures (authenticity, integrity, non-repudiation).
- **Collision Resistance**: Different inputs should result in different hashes.
- **Example**: Minor changes in input drastically change the SHA-256 hash output.

---

## Obfuscation

- **Purpose**: Makes code hard to read while keeping functionality.
- **Use Cases**:
  - Protect intellectual property.
  - Conceal malicious code.
- **Example**: A simple PHP script to echo "Hello World" can be made unreadable but functional.

---

## Masking

- **Type**: A form of obfuscation.
- **Function**: Hides sensitive parts of data (e.g., credit card numbers).
- **Use Case**: Protecting PII.
- **Techniques**: Substitution, shuffling, masking out with asterisks, encryption.

---

## Tokenization

- **Process**: Replace sensitive data with non-sensitive tokens.
- **Use Case**: Common in credit card transactions (e.g., contactless payments).
- **Security**:
  - One-time use tokens.
  - No encryption needed.
  - Tokens are not mathematically related to original data.

---

## Segmentation

- **Problem**: One large database is a single point of failure.
- **Solution**: Divide data into smaller, isolated parts.
- **Benefit**: Attackers must breach multiple systems.
- **Security Tuning**: More sensitive data gets stronger protection.

---

## Permission Restrictions

- **Access Control**:
  - Not just usernames/passwords.
  - Use of authentication policies (e.g., MFA).
- **Authentication Process**: 
  - Includes password rules, factor policies, and additional checks.
- **Post-Login**:
  - Users receive only the permissions necessary.
  - Prevents unauthorized access to sensitive data.

---
