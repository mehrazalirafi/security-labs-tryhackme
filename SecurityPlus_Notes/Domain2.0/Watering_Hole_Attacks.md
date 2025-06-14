# Watering Hole Attack

## 🦓 What is a Watering Hole Attack?
A watering hole attack targets trusted third-party websites that a specific group or organization frequently visits. Instead of attacking the organization directly, the attacker compromises the external sites.

---

## 🧠 Attack Motivation
> “If the mountain won’t come to the attacker, the attacker poisons the mountain’s watering hole.”

### Why attackers use it:
- Users **don't click phishing links**
- Users **ignore suspicious attachments**
- Network is **too secure for direct access**

So instead:
- Attackers **target websites** employees are likely to visit
- These become the "**watering holes**"

---

## 🎯 Execution Strategy
1. **Identify the target group’s frequent sites**
   - Examples: local coffee shop, industry forums, vendor portals
2. **Compromise the third-party site**
   - Use site vulnerabilities
   - Send malicious attachments to employees of that site
3. **Infect all visitors** (or specific IPs)
   - Target only selected victims (e.g., banks)
   - Now the attacker is inside the victim's network

---

## 🧪 Real-World Example: January 2017 Attack
### Affected Institutions:
- Polish Financial Supervision Authority
- National Banking and Stock Commission of Mexico
- State-owned bank in Uruguay

### Technical Details:
- Malicious **JavaScript files** added to their websites
- Only delivered to **specific IP ranges** tied to financial institutions
- Everyone else got the normal (clean) site

### Outcome:
- Whether the attack **succeeded is still unknown**

---

## 🔐 Defense: Watching the Watering Hole

### 1. **Defense-in-Depth**
- Use multiple layers of security controls
- No single tool is foolproof

### 2. **Firewalls and IPS**
- Firewall filters traffic
- Intrusion Prevention Systems inspect deeper for malicious content

### 3. **Antivirus / Anti-malware**
- Signature-based detection can recognize known malware
- Example: Symantec blocked the malicious JS using generic signatures

---

> 🛡️ **Best Practice**: Always monitor outbound traffic to catch unexpected behavior after visiting external sites.
