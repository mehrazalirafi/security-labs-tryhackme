# Social Engineering and Malware Tactics

## Impersonation Attacks

Attackers pretend to be someone else, like technical support or financial executives, to gain trust. They use stories and pretexts, often calling under the guise of urgent problems. Tactics include:

- Claiming to be from companies like Microsoft.
- Leaving urgent voicemails from the "US Treasury".
- Offering "0% interest rates" as a reward for good credit.

This form of impersonation builds trust and convinces victims to share personal or financial information.

## Vishing (Voice Phishing)

- Attackers use phone calls to obtain sensitive details.
- They use compelling narratives to request banking or SSN information.
- Instead of directly asking, they construct a convincing scenario to elicit data.

## Identity Fraud

- Attackers use your personal information to open bank or credit accounts.
- Victim’s credit report suffers due to unpaid balances.
- Fraud can extend to tax refunds and government benefits.

## Preventing Impersonation

- Never volunteer sensitive info over the phone or email.
- Legitimate support doesn’t need your password.
- Verify contact identities using official numbers.
- Organizations should enforce a verification culture.

---

## Watering Hole Attacks

These target third-party sites that victims trust and visit frequently:

1. **Goal**: Bypass direct attacks by compromising trusted sites.
2. **Steps**:
   - Identify frequented websites (e.g., coffee shop order systems).
   - Exploit vulnerabilities or send phishing attachments.
   - Infect the site and wait for the target to visit.
3. **Targeting**: Sometimes only specific IPs (e.g., bank networks) are infected.
4. **Case**: In 2017, banks in Poland, Mexico, and Uruguay were targeted.

### Mitigations

- **Defense in Depth**: Multiple overlapping security tools.
- **Firewalls and IPS**: Detect suspicious traffic.
- **Anti-virus**: Recognize generic malicious signatures.

---

## Misinformation & Disinformation

Disinformation campaigns distribute false info to:

- Confuse or divide populations.
- Sway public opinion on social/political matters.
- Employ nation-state actors or advertising to amplify reach.
- Use **social media** as the main platform for delivery.

### The Process

1. Fake users create content.
2. Post on social media.
3. Real users unknowingly share it.
4. The message goes viral.
5. Mass media may cover it, giving it legitimacy.

---

## Brand Impersonation

- Fake websites mimic brands (e.g., Coca-Cola).
- Appear in search results or via ads.
- Users click, get pop-ups ("You won!"), and download malware.

### Result:
- Malware displays ads, steals data, and tracks users.

---

## Finding Malware in Memory

- Malware must run in memory to operate.
- Memory forensics can locate malware in:
  - DLLs
  - Threads
  - Buffers
- Malware can inject itself into legitimate processes to hide and gain elevated privileges.

---

## DLL Injection

A popular memory injection technique:

- **DLL (Dynamic-Link Library)**: Shared code used by many apps.
- Attackers place malicious DLLs on disk.
- The target process loads these DLLs, executing the malware.
- Grants malware the same rights as the host application.
