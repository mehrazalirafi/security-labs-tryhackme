# Summary: DNS and Domain Attacks

---

**DNS Poisoning Techniques:**
- **Modify the DNS Server:** Difficult due to protections, requires hacking into the server.
- **Modify the Client Host File:** Host file overrides DNS queries; needs elevated access on the client.
- **Send a Fake DNS Response:** Real-time redirection via on-path (man-in-the-middle) attacks.

---

**How DNS Spoofing Works:**
- A legitimate DNS server resolves `professormesser.com` to a valid IP.
- An attacker gains control over the DNS server and changes the mapping to a malicious IP (100.100.100.100).
- Users are unknowingly redirected to the attacker’s server.

---

**Domain Hijacking:**
- Gaining control over the domain registration allows full control of DNS redirection.
- Methods include brute force, phishing, and compromising associated email accounts.
- Does not require access to the DNS or hosting servers.

---

**Real-World Incident:**
- On October 22, 2016, 36 domains of a Brazilian bank were hijacked for 6 hours.
- Attackers became the bank’s IP, affecting 5 million customers and $27 billion in assets.
- Sensitive data exposure occurred, but the full impact was not disclosed.

---

**URL Hijacking:**
- Registering domains with common typos (e.g., `professormessers.com`) for:
  - Ad revenue
  - Selling to original owner
  - Redirection to competitors
  - Phishing or malware distribution

---

**Common Typosquatting Variants:**
- Outright misspellings (e.g., `professormessOr.com`)
- Typing errors (e.g., `professormeser.com`)
- Variants with extra or missing characters
- Alternate top-level domains (e.g., `.org` instead of `.com`)
