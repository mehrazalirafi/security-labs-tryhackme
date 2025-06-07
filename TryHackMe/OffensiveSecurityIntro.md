# TryHackMe: Intro to Offensive Security – Summary

##  What is Offensive Security?
- **Definition**: Offensive Security simulates real hacker behavior to test and improve security.
- **Goal**: Identify vulnerabilities before malicious actors can exploit them.
- **Mindset**: "To outsmart a hacker, you need to think like one."

## Lab Environment
- TryHackMe provides a **safe, virtual environment** for legal hacking practice.
- You used a **simulated bank website ("FakeBank")** hosted on a virtual machine.

## Your First Hack – Key Steps
1. **Open a Terminal** in the VM.
2. **Run Gobuster** to find hidden directories:
   ```bash
   gobuster -u http://fakebank.thm -w wordlist.txt dir
   ```
   - `-u` sets the URL
   - `-w` sets the wordlist
   - `dir` mode checks for directories

3. **Interpreting Results**:
   - Status `200`: Page exists (`/bank-transfer` found)
   - Status `301`: Redirect (e.g., `/images`)

4. **Access Hidden Page**:
   - Navigate to `/bank-transfer`
   - Transfer money as an "ethical hacker" to simulate exploiting the vulnerability.

## Career Pathways Mentioned
- **Penetration Tester**: Finds exploitable vulnerabilities.
- **Red Teamer**: Simulates real attacks for defense testing.
- **Security Engineer**: Maintains and improves defenses.
