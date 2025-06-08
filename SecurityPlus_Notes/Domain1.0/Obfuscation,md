# 🔐 Data Protection Concepts Summary

## 1. Trusted Platform Module (TPM)
**Purpose**: Hardware for cryptographic functions on a single device.  
**Functions**:
- Cryptographic processor (random number/key generation)
- Persistent memory (keys burned during manufacturing)
- Versatile memory (stores BitLocker keys, hardware configs)
- Password protected (resistant to brute-force/dictionary attacks)

---

## 2. Hardware Security Module (HSM)
**Purpose**: Large-scale cryptographic operations in enterprise environments.  
**Features**:
- Used in clusters with redundant power/network
- Stores thousands of cryptographic keys securely
- High-end plug-in card or external hardware
- Key backups and cryptographic accelerators

---

## 3. Key Management System (KMS)
**Centralized** management of cryptographic keys for:
- SSL/TLS, SSH, BitLocker, AD, cloud services  
**Functions**:
- Key creation, rotation, association, logging
- On-premises or cloud-based
- Separation of keys from data

---

## 4. Secure Enclave
**Purpose**: Isolated secure processor for protecting secrets  
**Security Features**:
- Own boot ROM
- System boot process monitoring
- True random number generation
- Real-time memory encryption
- Root cryptographic keys
- Hardware AES encryption

---

# 🕵️ Obfuscation & Steganography

## Obfuscation
- Makes data difficult to understand (not encryption)
- Example: Hiding info in plain sight (e.g. steganography)

## Steganography
**Definition**: Hiding messages in media (Greek: "concealed writing")  
**Covertext**: Container file/document  
**Techniques**:
- Image-based (invisible changes)
- Network-based (TCP packet data)
- Invisible watermarks (e.g. printer dots)
- **Audio**: Interlacing secret in audio files
- **Video**: Sequence of stego images; higher data capacity

---

# 💳 Data Protection in Practice

## Tokenization
**Definition**: Replace sensitive data with non-sensitive tokens  
**Use case**: Credit card processing
- Temporary token replaces real number
- Tokens not mathematically related to original data
- **Not** encryption or hashing

## Data Masking
**Purpose**: Hide parts of data from view  
**Use case**: Show only last 4 digits of credit card  
**Techniques**: Substituting, shuffling, masking, encrypting
