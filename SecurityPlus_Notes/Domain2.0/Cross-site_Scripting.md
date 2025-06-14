# Cross-Site Scripting (XSS) Summary

## What is XSS?
- **XSS (Cross-Site Scripting)** is a common web vulnerability.
- It was originally named "cross-site" due to browser flaws where one site could access data from another.
- **Not to be confused with CSS (Cascading Style Sheets).**

## Attack Characteristics
- One of the most widespread vulnerabilities in web apps.
- Exploits the **trust a user places in a website**.
- Most XSS attacks involve **JavaScript**.

## General Exploitation Flow
1. Attacker sends a **malicious link** with a script to a victim.
2. Victim clicks and visits a **legitimate website**.
3. The site loads, but the malicious script also runs.
4. This script may **steal cookies, session IDs, or other sensitive data** and send it to the attacker.

## Types of XSS

### Non-Persistent (Reflected) XSS
- Script is reflected off a web server (e.g., search input).
- Sent via email or link.
- Executes immediately in the user's browser.
- **Steals credentials/session IDs** without user's knowledge.

### Persistent (Stored) XSS
- Attacker posts the malicious script on a **public page** (e.g., comment or social media post).
- Payload is saved on the site and affects **every visitor**.
- Can **propagate** across users and spread.

### Real-World Case: Subaru (2017)
- Subaru's web app issued tokens that never expired.
- Tokens were valid for **any request**, even across accounts.
- XSS in frontend allowed an attacker to steal a token and gain **control of someone else's vehicle**.

## Mitigation and Protection

### For Users
- Avoid clicking **untrusted links** (especially in emails).
- Consider **disabling JavaScript** (limited protection).
- Always keep your **browser and apps updated**.

### For Developers
- **Validate user input** to prevent script injection.
- **Never allow arbitrary scripts** in input fields.
