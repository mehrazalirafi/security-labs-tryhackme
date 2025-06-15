
# Malware Deep Dive

## Virus

- **Definition**: Malware that can replicate itself, but requires user action to begin (e.g., clicking a file).
- **Spreads via**: File systems or networks.
- **Impact**:
  - Some viruses are quiet, others cause system problems or downtime.
  - Anti-virus software is essential and must be updated frequently.

### Types of Viruses:
- **Program viruses**: Embedded within applications.
- **Boot sector viruses**: Load during system startup.
- **Script viruses**: Run via OS or browser scripts.
- **Macro viruses**: Use macro languages in tools like Microsoft Office.
- **Fileless viruses**:
  - Operate in memory only.
  - Exploit vulnerabilities (e.g., Flash, Java).
  - Evade file-based detection by never writing to disk.
  - Often use PowerShell to run further payloads.
  - Add persistence via autostart registry entries.

---

## Worms

- **Definition**: Malware that replicates itself without user input.
- **Spreads through**: Networks, exploiting vulnerabilities.
- **Traits**:
  - Self-propagating and fast-spreading.
  - Doesn’t need user interaction.
  - Difficult to contain once inside.

### Defense Against Worms:
- **Firewalls and IDS/IPS** can block worm propagation.
- **Prevention** is more effective than remediation.

---

## Case Study: WannaCry Worm

- **Exploits**: EternalBlue vulnerability.
- **Steps**:
  1. Infects one vulnerable system.
  2. Installs a backdoor and downloads WannaCry ransomware.
  3. Searches for other vulnerable systems across the network.
  4. Repeats infection and encryption process.
- **Impact**: Combines worm and ransomware behaviors for massive damage.
