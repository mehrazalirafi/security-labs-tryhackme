# 🔐 Public Key Cryptography Notes

## 🧱 Public Key Infrastructure (PKI)
- **Definition**: A system of policies, procedures, hardware, software, and people to manage digital certificates.
- **Functions**: Create, distribute, manage, store, and revoke certificates.
- **Complexity**: Requires extensive planning and coordination.
- **Purpose**: Associates certificates with people or devices using a Certificate Authority (CA).
- **Core Idea**: It’s all about **trust**.

---

## 🔐 Symmetric Encryption
- **Single shared key**: Used for both encryption and decryption.
- **Secret key algorithm**: If the key is exposed, a new one must be created.
- **Scalability issue**: Difficult to distribute and manage securely at scale.
- **Performance**: Very fast, low overhead.
- **Usage**: Often used in combination with asymmetric encryption.

---

## 🔐 Asymmetric Encryption
- **Uses two mathematically related keys**:
  - **Public key**: Shared openly.
  - **Private key**: Kept secret.
- **Encryption/Decryption**:
  - Public key encrypts.
  - Only the corresponding private key can decrypt.
- **Security**: You **cannot** derive the private key from the public key.

---

## 🧰 Key Pair Generation
- **Occurs simultaneously** for public and private key.
- Involves:
  - Large random values
  - Prime numbers
  - Heavy mathematical computation
- **Distribution**:
  - Public key can be shared (website, social media, etc.).
  - Private key is kept secret, often password-protected.

---

## 📬 Example: Message Encryption
1. Bob writes: “Hello, Alice.”
2. Encrypts using **Alice’s public key** → ciphertext.
3. Sends ciphertext to Alice.
4. Alice decrypts using her **private key** → retrieves original message.

---

## 🗝️ Key Escrow
- **Definition**: A 3rd party holds your private key.
- **Purpose**:
  - Businesses may need to access employee data.
  - Governments may require access to encrypted partner data.
- **Controversial?** Yes.
  - But may be **required** for continuity and compliance.

