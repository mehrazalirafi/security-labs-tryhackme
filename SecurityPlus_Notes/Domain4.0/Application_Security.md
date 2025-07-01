# Secure Coding Concepts Summary

## 🔒 Core Principles
- **Security vs. Timelines**: Security is often secondary to development speed
- **Testing Imperative**: QA must include security validation
- **Inevitable Vulnerabilities**: All code has flaws that will be exploited

## 🛡️ Key Security Practices
1. **Input Validation**
   - Define/document expected input formats
   - Normalize and sanitize ALL inputs (e.g., zip code formats)
   - Fuzz testing reveals validation gaps

2. **Secure Cookies**
   - Never store sensitive data
   - Enable "Secure" attribute (HTTPS-only transmission)
   - Browser-stored data ≠ secure storage

3. **Static Code Analysis (SAST)**
   - Automatically detects vulnerabilities:
     - Buffer overflows
     - SQL injections
     - Access control issues
   - Limitations: Misses crypto/auth flaws
   - Requires manual verification (false positives)

4. **Code Signing**
   - Verifies authenticity and integrity
   - Developer signs code with private key
   - CA validates developer identity
   - Alerts users to tampered code

5. **Sandboxing**
   - Isolates applications from critical resources
   - Implementation examples:
     - Virtual machines
     - Mobile OS permissions
     - Browser iframes
     - Windows UAC

6. **Security Monitoring**
   - Real-time attack detection (SQLi, exploit attempts)
   - Log auditing for hidden threats
   - Anomaly detection:
     - Unusual file transfers
     - Abnormal access patterns
