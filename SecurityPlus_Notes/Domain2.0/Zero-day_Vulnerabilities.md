# Vulnerabilities and Zero-Day Attacks

---

## 🛠️ General Vulnerabilities

- **Prevalence**: Most applications contain unknown vulnerabilities.
- **Discovery**:
  - Security researchers try to find and responsibly disclose them.
  - Attackers try to find them first and keep them secret.
- **Risk**: If attackers discover vulnerabilities before vendors do, they can exploit them without any defenses in place.

---

## 🕳️ Zero-Day Attacks

- **Definition**: Exploiting a vulnerability unknown to the vendor with no patch available.
- **Vendor Status**: Unaware of the issue, thus no fix exists yet.
- **Defensive Challenge**: Hard to protect against an unknown flaw.
- **Response**: Security teams race to patch once the attack is known.

---

## 🧠 Learn More: CVE Database

- **CVE**: Common Vulnerabilities and Exposures
- **Official Source**: [https://cve.mitre.org](https://cve.mitre.org)
- Central index for publicly known cybersecurity vulnerabilities.

---

## 🔥 Recent Zero-Day Attacks (2023)

- **April 2023 — Google Chrome**
  - Memory corruption, sandbox escape.

- **May 2023 — Microsoft**
  - Secure boot vulnerability.
  - Allowed UEFI-level self-signed code execution.

- **May 2023 — Apple iOS & iPadOS**
  - Three separate zero-day patches:
    - Sandbox escape.
    - Disclosure of sensitive information.
    - Arbitrary code execution.
