
# 🔐 Cryptography: Core Concepts

---

## 🧾 Non-repudiation

- **Definition**: Ensures that someone cannot deny the validity of their actions or statements.
- **Example**: Signing a contract ensures non-repudiation — the signer cannot deny having signed it.
- **Cryptographic Relevance**:
  - Proves you really **signed** the message.
  - Others can **verify** your signature.
  - Adds **proof of integrity and origin**.

---

## 📦 Proof of Integrity

- **Goal**: Ensure data has **not changed** during transit or storage.
- **Method**: Use **cryptographic hashes**.
  - Hash = Short string of text representing the data.
  - Examples: Message Digest, Fingerprint.
- **Key Property**: If the **data changes**, the **hash changes**.
- **Note**: Hashes do not identify people — only confirm data integrity.

---

### 🔍 Hashing Example: Gutenberg Encyclopedia

- **Original File**: Gutenberg Encyclopedia Vol 1 (8.1MB).
- **Original Hash**: c7004997a9cff3f9c3423579be58f77389b63b4b08b5e541d327903f99a09db
- **After Changing One Character**: 5c82dcc2e0f359b48fdddf716ca4602941f5e21e26b2edc7bb43942eb715a1c1
- **Conclusion**: Even a **minor change** alters the entire hash, **compromising data integrity**.

---

## 🧾 Proof of Origin

- **Goal**: Confirm that the message:
  - Was **not modified** (integrity)
  - Came from a **verified sender** (authentication)
- **Process**:
  - Ensure the **signature is authentic** (non-repudiation).
  - Sender signs with their **private key**.
  - Receiver verifies using the **public key**.
  - Any change to the message **invalidates** the signature.

---

## ✍️ Creating a Digital Signature

1. Write message (e.g., _You're hired, Bob_)
2. Generate hash of the message using a **hashing algorithm**
3. Encrypt the hash with sender’s **private key** → produces the **digital signature**
4. Send the **plaintext + signature**

---

## ✅ Verifying a Digital Signature

1. Receive **plaintext and digital signature**
2. Use sender’s **public key** to decrypt the signature → get the original hash.
3. Hash the received plaintext yourself.
4. **Compare** both hashes:
   - If they match → message is **authentic and unchanged**.
   - If not → message has been **tampered with**.

