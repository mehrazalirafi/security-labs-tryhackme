# Encryption Overview

## Encrypting Stored Data
- **Data at rest** (e.g., SSD, USB drive, cloud storage) should be encrypted.
- **Full-disk/volume encryption**: Tools like BitLocker (Windows), FileVault (macOS).
- **File encryption**: EFS (Encrypting File System in Windows), or third-party tools.

## Database Encryption
- **Transparent encryption**: Encrypts entire DB with a symmetric key.
- **Record-level encryption**: Encrypts only sensitive columns, e.g., SSNs, with separate symmetric keys.

## Transport Encryption
- Protects **data in transit**.
- **HTTPS**: Encryption built into web applications.
- **VPN (Virtual Private Network)**:
  - **Client-based** VPN: Uses SSL/TLS.
  - **Site-to-site** VPN: Uses IPsec.

## Encryption Algorithms
- Numerous types exist; both parties must agree on the algorithm.
- The algorithm is usually **public**, but the **key** is secret.
- Choice depends on **security level**, **speed**, and **complexity**.

## DES vs AES Comparison
- **DES (Data Encryption Standard)**: Older, 64-bit blocks, multiple permutation rounds.
- **AES (Advanced Encryption Standard)**: Newer, supports 128/192/256-bit keys, faster and more secure.

## Cryptographic Keys
- The **key** determines output (ciphertext, hash, or digital signature).
- Algorithms are public, but **key secrecy** is critical.

## Key Lengths
- **Longer keys = more secure** (resist brute-force).
- **Symmetric encryption**: Commonly 128-bit or more.
- **Asymmetric encryption**: Often 3072-bit or longer.

## Key Stretching
- Strengthens weak keys by **repeating hashing** (e.g., hash of hash).
- Slows down brute-force attacks significantly.
