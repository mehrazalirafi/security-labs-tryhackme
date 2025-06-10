# Cryptographic Hashes and Digital Signatures

## Hashes
- Represent data as a short string of text
  - Also called a message digest or fingerprint
- **One-way trip**
  - Impossible to recover original message from the hash
  - Useful for storing passwords and ensuring confidentiality
- **Integrity Verification**
  - Used to confirm a downloaded document matches the original
- **Digital Signature Use**
  - Enables authentication, non-repudiation, and integrity

---

## Hash Example (SHA256)
- SHA256: 256-bit hash (64 hexadecimal characters)
- Even a minor change in input results in a drastically different hash

Example:
```text
Input: "My name is Professor Messer."  
SHA256: 19da9a2e26f3bff67f0522f962851c42542b8659333ac53397c8d65aa7a3f871

Input: "My name is Professor Messer!"  
SHA256: 54381cae1eea10892d81c8688d06d1928b4ee8495061a792864f83092b033aea
```

---

## Collisions
- Hash functions:
  - Accept input of any size, output fixed-size string
  - Should generate unique hashes for different inputs
- **Collision**: Same hash for different inputs
  - Indicates vulnerability
- **MD5** is vulnerable to collisions
  - Discovered in 1996
  - Should not be used for anything important

---

## Practical Hashing Use Cases
### 1. Verifying Downloads
- Hash posted on the site
- Downloaded file’s hash should match posted hash

### 2. Password Storage
- Store **salted hash**, not raw password
- Hash comparison done during login
- Original password is never known by the server

---

## Adding Salt
- Salt: Random data added to password before hashing
- Each user gets a unique salt
- Makes rainbow table attacks ineffective
- Slows down brute-force attempts

Example:
```text
Password: dragon
Salts: gsEVx, LTBkP, HTsBK, MnNEt
Hashes (different for each salted input)
```

---

## Digital Signatures
- Prove message was not changed (Integrity)
- Prove message source (Authentication)
- Prevent signature forgery (Non-repudiation)

### Process:
- Sign with **private key**
- Verify with **public key**
- Message content usually remains unencrypted

---

## Creating a Digital Signature
1. Create a hash of the message
2. Encrypt hash using sender’s private key
3. Send plaintext + digital signature

---

## Verifying a Digital Signature
1. Decrypt signature using sender’s public key → obtain hash
2. Hash the received plaintext again
3. Compare the two hashes
4. If equal → signature is verified
