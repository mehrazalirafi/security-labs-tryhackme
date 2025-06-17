# Summary of Cryptographic Attacks

This document summarizes key cryptographic attack types. 

---

## 1. Cryptographic Attacks

- When you encrypt data and send it, you must consider: Is it really secure? How do you know?
- Attackers may not have the key but can attack the cryptography itself.
- Many weaknesses come from poor implementation rather than the algorithm itself.

---

## 2. Birthday Attack

- With 23 people, there's a ~50% chance of shared birthdays; with 30, it's ~70%.
- Analogous to a **hash collision** in cryptography.
- Attackers brute-force many plaintexts to find two that produce the same hash.
- Defense: Use large hash output sizes to reduce collision probability.

---

## 3. Collisions

- Hash digests should be unique; different inputs should not produce the same hash.
- **MD5 hash**: Collisions were found as early as 1996.
- In 2008, fake CA certificates were generated using MD5 collisions, appearing legitimate.
- Illustrated with two slightly different plaintexts that still yield the same MD5 hash.

---

## 4. Downgrade Attack

- Instead of breaking strong encryption, attackers force systems to use weak ones.
- **SSL Stripping**: Combines an on-path attack and downgrade attack.
  - Attacker intercepts and downgrades HTTPS to HTTP.
  - Victim sends credentials in plaintext HTTP.
  - Attacker reuses the credentials in encrypted HTTPS session with the server.
- Defense: Always enforce HTTPS and use security headers like HSTS.

---
