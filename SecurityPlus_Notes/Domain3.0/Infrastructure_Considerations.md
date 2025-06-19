# Cloud Infrastructure Design Considerations

This document summarizes key infrastructure considerations for cloud-based environments, based on Professor Messer’s video lecture.

---

## Availability
- Ensures systems are up and transactions can be completed.
- Must be accessible **only to authorized individuals**.
- Redundancy and monitoring systems support uptime.
- Often measured in terms of **uptime percentage** (e.g., 99.999%).

## Resilience
- Focuses on recovery after failure or outage.
- Influenced by factors like root cause, hardware replacement, and software patch availability.
- Measured using **MTTR (Mean Time To Repair)**.

## Cost
- Total cost includes:
  - Initial setup
  - Ongoing maintenance
  - Replacement/repair
  - Tax and accounting considerations (e.g., capital vs. operating expenses)

## Responsiveness
- Speed of response to user requests.
- Critical for **interactive applications**.
- Depends on multiple layers of application architecture.
- Delays can occur due to any weak component.

## Scalability
- Ability to adjust capacity on demand (elasticity).
- Must consider **resource bottlenecks** and **security monitoring** when scaling.
- Supports demand spikes without overprovisioning.

## Ease of Deployment
- Applications consist of many components (e.g., web server, DB, firewall).
- Deployment may be **complex** (manual setup, change control) or **simple** (orchestrated/automated).
- Planning is critical to avoid deployment delays.

## Risk Transference
- Use of **cybersecurity insurance** to reduce financial risk.
- Covers downtime, ransomware losses, legal costs.
- Helps recover from **internal and external impacts**.

## Ease of Recovery
- Important to design systems with fast recovery paths.
- Example: OS reload (1 hour) vs. restoring from image (10 mins).
- Influences business continuity and cost-efficiency.

## Patch Availability
- Systems must be **regularly updated** with bug fixes and security patches.
- Microsoft and others provide **monthly updates**.
- Failure to patch increases **vulnerability risk**.

## Inability to Patch
- Some embedded systems (e.g., HVAC, time clocks) may not support patching.
- Additional controls like **network segmentation** and **firewalls** may be necessary.

## Power
- A **foundational requirement**.
- Needs detailed planning based on environment (data center vs. office).
- Backup options include **UPS** and **generators**.

## Compute
- The "engine" of the application.
- Cloud allows scalable compute options across multiple CPUs and regions.
- May use **multiple processors** or **single processor**, depending on need.

---
