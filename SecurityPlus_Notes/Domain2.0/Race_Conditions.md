# Race Condition and TOCTOU Attack

## What is a Race Condition?
A race condition is a **programming flaw** that occurs when two or more processes access shared resources **simultaneously**, and the final outcome depends on the timing of their execution. If not properly managed, it can lead to unpredictable and dangerous behavior in applications.

- It is a **conundrum** where timing affects results.
- Common in **multi-threaded** or asynchronous systems.
- Especially problematic when the application does not anticipate concurrent actions.

---

## TOCTOU: Time-of-Check to Time-of-Use Attack

This is a specific type of race condition:
- You **check** the state of a system.
- You later **use** that state, assuming it hasn't changed.
- **But** something may have changed in between the check and the use.

### Example Process:
1. System checks access permissions or file status.
2. Before using the data (e.g., opening or writing a file), the attacker replaces or alters it.
3. Results in privilege escalation or unauthorized access.

---

## Visual Example: Banking Transaction Race Condition

### Initial State:
- Account A = $100  
- Account B = $100  

### User 1:  
1. Checks balance → A: $100, B: $100  
2. Adds $50 to B → B = $150  
3. Removes $50 from A → A = $50  

### User 2:  
1. Checks balance → A: $100, B: $100  
2. Adds $50 to B → B = $200  
3. Removes $50 from A → A = $50  

### Ending State (Incorrect):
- Account A = $50  
- Account B = $200  
> **Expected:** A = $0, B = $200  
> **Cause:** Both users operated simultaneously, and withdrawals weren’t updated in real-time.

---

## Real-World Race Condition Examples

### 1. **Mars Rover "Spirit" (2004)**  
- Race condition in **file system error handling** caused a reboot loop.
- The system rebooted on detecting a file error, but the reboot didn’t fix the underlying problem, triggering the same error repeatedly.

### 2. **Tesla Model 3 - Pwn2Own Vancouver 2023**  
- **TOCTOU attack** via Bluetooth on the infotainment system.
- Attackers escalated privileges to **root access**.
- Result: $100,000 prize and a free Tesla.

---

## Key Takeaways
- Always account for **simultaneous access** in applications.
- **Locks, semaphores, and atomic operations** help prevent race conditions.
- TOCTOU attacks are especially critical in **privileged operations** and **file handling**.
