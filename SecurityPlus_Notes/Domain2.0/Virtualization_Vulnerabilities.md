# Virtualization Security Summary

## Virtualization Characteristics
- **VMs differ from non-virtual machines**
  - Can appear anywhere; more dynamic and transient.
- **Resources vary between VMs**
  - VMs may have different allocations of CPU, memory, and storage.
- VMs **resemble physical machines**, but their **complexity increases risk**.

## Common Virtualization Vulnerabilities
- **Local privilege escalation**
- **Command injection**
- **Information disclosure**

## VM Escape
- A VM is designed to be **isolated**.
- **VM escape** occurs when a user breaks out of the VM to access the host or other VMs.
- A successful escape gives the attacker **full control** of the virtual environment.

### Case Study: March 2017 Pwn2Own
- Contestants exploited:
  - **JavaScript bug in Microsoft Edge**
  - **Windows 10 kernel vulnerability**
  - **VMware hardware simulation bug**
- Result: attacker escaped sandbox → guest OS → host system.
- **Patches released** shortly after discovery.

## Resource Reuse Issues
- The **hypervisor** manages memory, CPU, storage for all VMs.
- Sometimes **overcommitted RAM** is shared dynamically.
  - e.g., 3 VMs each allocated 2 GB on a 4 GB RAM host.
- This can lead to **data leakage** if memory is not properly isolated.
- Fixes: update memory management and apply **security patches**.
