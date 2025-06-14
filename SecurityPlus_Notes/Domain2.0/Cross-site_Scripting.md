# Cross-Site Scripting (XSS) – Summary Notes

## 🔐 What is XSS?
- XSS = Cross-site scripting (not to be confused with CSS).
- Allows attackers to inject malicious scripts into trusted websites.
- Exploits browser security flaws, often via JavaScript.
- Takes advantage of the trust a user has in a website.

---

## 🚨 How XSS Works
1. Attacker sends a malicious link to the victim.
2. Victim clicks it and visits a legitimate site.
3. Malicious script runs in the victim’s browser.
4. Data like session cookies are stolen and sent to attacker.

---

## 🪞 Reflected (Non-Persistent) XSS
- Script runs only once—reflected off a vulnerable site (e.g., via a search box).
- Delivered via a URL (email, text, etc.).
- Runs in victim’s browser and steals session data.

---

## 🛒 Example of Reflected XSS
- XSS payload embedded in input fields (like credit card forms).
- Executes JavaScript like `document.cookie` when submitted.
- Victim’s session info displayed or stolen silently.

---

## 🧠 Stored (Persistent) XSS
- Malicious code is stored (e.g., in a social media post).
- Every viewer of the content gets affected.
- Can spread fast across users.

---

## 🏎️ Real-World Case: Subaru Hack (2017)
- Token never expired.
- XSS vulnerability allowed attacker to grab token and control vehicles.
- Vulnerability reported and patched.

---

## 🛡️ Protecting Against XSS
- Don’t click untrusted links.
- Consider disabling or limiting JavaScript.
- Keep browsers and software up-to-date.
- Always validate input—no raw scripts allowed!

---
