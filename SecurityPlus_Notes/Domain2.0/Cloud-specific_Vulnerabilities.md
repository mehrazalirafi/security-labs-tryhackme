## ☁️ Security in the Cloud

### Key Issues
- **Widespread Adoption**  
  Nearly every organization now uses cloud services.

- **Sensitive Data at Risk**  
  Sensitive data stored in the cloud is highly attractive to attackers.

- **Lack of Proper Protections**  
  - 76% of organizations don’t use **MFA** (Multi-Factor Authentication) for management console access.

- **Neglected Best Practices**  
  - 63% of cloud production code is **unpatched**.  
  - Many vulnerabilities have **CVSS ≥ 7.0**, indicating **high or critical severity**.

---

## 🛠️ Attacking the Service

- **Denial of Service (DoS)**  
  Basic attack type aimed at taking systems offline.

- **Authentication Bypass**  
  Exploits weak or misconfigured login mechanisms.

- **Directory Traversal**  
  Takes advantage of misconfigured web server paths to access restricted files.

- **Remote Code Execution (RCE)**  
  Executes arbitrary code via unpatched vulnerabilities.

---

## 🧠 Attacking the Application

- **Web Application Vulnerabilities**  
  - Notable examples: **Log4j** and **Spring Cloud Function**  
  - Easy to exploit, high reward

- **Cross-Site Scripting (XSS)**  
  - Caused by poor input validation  
  - Allows attackers to inject and execute malicious scripts

- **Out-of-Bounds Write**  
  - Writes data into unauthorized memory space  
  - Can lead to **crashes**, **data corruption**, or **RCE**

- **SQL Injection**  
  - Allows direct access and control over backend databases  
  - Often used to extract sensitive data

---
