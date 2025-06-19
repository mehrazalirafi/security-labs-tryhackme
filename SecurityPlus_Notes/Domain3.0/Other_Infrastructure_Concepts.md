# Summary: Cloud Infrastructure and Security

This video explores key aspects of modern IT infrastructure, especially cloud vs. on-premises environments, security considerations, and architecture types.

## Cloud vs. On-Premises Security
- **Cloud-based security** is cost-effective, centralized, and managed by third-party providers. No need for physical data centers or hardware maintenance.
- **On-premises infrastructure** provides full control and customization but requires local staffing, resources, and incurs higher costs. 
- Attackers target data regardless of its location; thus, both environments need strong security.

## On-Premises Security Pros and Cons
- **Pros**: Full control, better customization, local team can maintain uptime.
- **Cons**: High costs, staff challenges, and slower implementation of changes.

## Centralized vs. Decentralized Management
- Most infrastructures are **decentralized** (spread across locations, OSs, and cloud providers).
- A **centralized approach** improves visibility, log management, and system maintenance but introduces single points of failure and scaling issues.

## Virtualization
- Enables multiple **operating systems** to run on a single hardware using a **hypervisor**.
- Each application has its own **guest OS**, leading to increased resource use and complexity.

## Containerization
- Containers run applications with only necessary dependencies using the **host OS**.
- They are lightweight, isolated, and use systems like **Docker** for management, increasing efficiency.

## Virtualized vs. Containerized
- **Virtualized apps**: Each runs on its own OS, more overhead.
- **Containerized apps**: Share the same host OS, use less resources, more scalable.

## Internet of Things (IoT)
- Includes sensors, smart devices, wearables, and facility automation tools.
- **Security risk**: Weak default settings; manufacturers often lack security expertise.

## SCADA / ICS Systems
- Used in industrial environments (e.g., power, manufacturing).
- Highly secure and segmented; real-time control is centralized to prevent external access.

## RTOS (Real-Time Operating Systems)
- Deterministic systems used in vehicles, military, and manufacturing.
- Sensitive to security; need to always be available and are often self-contained.

## Embedded Systems
- Designed for a **single purpose** (e.g., traffic lights, smartwatches).
- Optimized for efficiency and cost, limited security and OS access.

## High Availability (HA)
- Ensures services remain available even during failures.
- Implemented using redundancy and active-active setups, but **increases cost** with each layer of backup or contingency.
