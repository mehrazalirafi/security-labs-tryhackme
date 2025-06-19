# Network Segmentation and SDN Overview

## 1. Physical Isolation
- **Physically separate devices** (e.g., Switch A and B with an air gap).
- Prevents attacker pivoting between systems.
- Example: Web servers in one rack, databases in another.
- No data mixing: each customer/device is on its own switch.
- Downsides: Poor scalability—requires more hardware.

## 2. Physical Segmentation
- **Separate infrastructure units** per customer.
- Devices (like switches) are isolated for each user.
- Ensures clear separation but still hardware-intensive.

## 3. Logical Segmentation with VLANs
- **Virtual Local Area Networks (VLANs)** provide separation within the same physical switch.
- Segments customers/devices logically.
- Communication between VLANs requires a **Layer 3 device** (e.g., router).
- More scalable and cost-efficient than full physical separation.

## 4. Software Defined Networking (SDN)
- Breaks networking device operations into **three planes**:
  - **Data Plane** (Infrastructure Layer): Handles packet forwarding, NAT, encryption.
  - **Control Plane**: Manages routing/session tables and dynamic protocols.
  - **Management Plane** (Application Layer): Used for device configuration (via SSH, API).

## 5. SDN Architecture Benefits
- Allows **logical function separation** and centralized control.
- Provides programmability and agility in cloud environments.
- Extendable and modular: built for cloud-native infrastructure.

## 6. SDN Flow and Security
- Data flows through structured layers:
  - **Management**: SSH, SNMP, APIs
  - **Control**: Routing decisions
  - **Data**: Actual traffic forwarding
- Example: Cloud setup with dynamic firewalls, load balancer, web servers, and database.
- Firewalls can be **provisioned dynamically** to segment traffic between zones.

---
