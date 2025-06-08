# 🔐 Hardware and Key Management Security Notes

---

## 🧱 Trusted Platform Module (TPM)

- **Cryptographic Hardware**: Built into devices to perform crypto functions.
- **Cryptographic Processor**:
  - Generates random numbers and encryption keys.
- **Persistent Memory**:
  - Stores unique keys created during manufacturing.
- **Versatile Memory**:
  - Stores config info, encryption keys (e.g., BitLocker).
- **Password Protected**:
  - Immune to brute-force or dictionary attacks.

---

## 🧰 Hardware Security Module (HSM)

- **Used in Large Environments**:
  - Supports clusters, power redundancy.
  - Stores thousands of keys.
- **High-end Cryptographic Hardware**:
  - Dedicated plug-in cards or separate devices.
- **Key Backup**:
  - Securely stores and protects key backups.
- **Accelerated Cryptography**:
  - Offloads encryption workloads from CPUs.

---

## 🔑 Key Management System (KMS)

- **Decentralized Services, Centralized Management**:
  - Works across on-prem and cloud services.
- **Central Console**:
  - Manages keys for SSL/TLS, SSH, BitLocker, AD, etc.
  - Associates keys with specific users.
  - Enables auto-rotation and logging.
- **Separation of Duties**:
  - Keys stored separately from the protected data.

---

## 🛡 Secure Enclave

- **Isolated Secure Processor**:
  - Separate from the main CPU (used in phones, laptops, etc.).
- **Security Features**:
  - Own boot ROM and monitors boot process.
  - Real-time memory encryption.
  - True random number generation.
  - Hardware-level AES encryption.
  - Root cryptographic key storage.
- **Purpose**:
  - Ensures privacy and security even if the device is compromised.

---

## 🔐 Keeping Data Private

- **Data Locations**:
  - Spread across phones, cloud, laptops.
- **Constant Threat Landscape**:
  - Attackers evolve; defenses must stay ahead.
- **Dynamic Data**:
  - Must support secure and flexible updates to stored data.
