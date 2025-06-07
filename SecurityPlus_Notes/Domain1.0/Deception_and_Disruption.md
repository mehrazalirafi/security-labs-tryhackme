# Deception Technologies in Cybersecurity

## Honeypots
- **Purpose**: Attract attackers and trap them in a controlled environment.
- **Typical Attacker**: Often an automated system scanning for vulnerabilities.
- **How it Works**: Simulates real systems to study attacker behavior.
- **Types**: Can be software-based, open-source, or commercial tools.
- **Security Value**: Useful for reconnaissance and improving defenses.
- **Challenge**: Ongoing arms race to make honeypots realistic enough to fool attackers.

## Honeynets
- **Definition**: A collection of interconnected honeypots forming a simulated network.
- **Components**: Mimic real infrastructures like routers, switches, servers, firewalls.
- **Use Case**: Increases realism and traps attackers for longer engagement.
- **Example Resource**: [Project Honeypot](https://projecthoneypot.org)

## Honeyfiles
- **Purpose**: Attract attackers with files containing fake or enticing data.
- **Examples**: `passwords.txt`, confidential-looking documents.
- **Deployment**: Scattered across file shares as bait.
- **Security Mechanism**: Trigger alerts if accessed—acts like a virtual bear trap.

## Honeytokens
- **Definition**: Traceable fake data used to detect data exfiltration or misuse.
- **Examples**:
  - Fake API keys (generate alerts when used)
  - Dummy email addresses (track online leaks)
  - Browser cookies, database entries, pixel trackers
- **Goal**: Identify where the data leaks and who accessed it.
