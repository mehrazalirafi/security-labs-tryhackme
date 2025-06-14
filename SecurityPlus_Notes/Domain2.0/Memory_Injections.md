# 🛡️ Finding Malware in Memory

- **Malware runs in memory**  
  - It must be loaded into RAM to execute  
  - *Memory forensics* can help detect and analyze it  

- **Memory contains many active components**  
  - DLLs (Dynamic-Link Libraries)  
  - Threads, buffers, and memory management functions  

- **How malware hides:**  
  - **Own process:** Malware creates a separate memory process  
  - **Process injection:** Malware injects itself into a legitimate process, often for:
    - Avoiding detection
    - Gaining escalated privileges

---

# 🧬 DLL Injection

- **Dynamic-Link Library (DLL):**  
  - Windows library with code and data  
  - Shared across many applications

- **Injection Process:**  
  1. Attacker places malicious DLL on storage  
  2. Injects *path to DLL* into a target process  
  3. Target process loads DLL, thinking it’s legitimate  
  4. Malware executes within the context of the target

- **Why it’s used:**  
  - Popular memory injection method  
  - Easy to implement  
  - Grants malware the same rights as the host process
