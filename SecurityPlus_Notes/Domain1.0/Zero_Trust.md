# Zero Trust Architecture – Summary Notes

## Zero Trust

- Networks are often open internally after bypassing the firewall.
- **Zero trust** is a comprehensive security model:
  - Applies to every device, process, and person.
  - Assumes **nothing is trusted** by default.
- Requires verification for everything:
  - Techniques: MFA, encryption, access controls, firewalls, monitoring, analytics.

---

## Planes of Operation

- Networks are split into **functional planes**:
  - Applies across physical, virtual, and cloud infrastructure.

### Data Plane
- Handles **packets, frames, and traffic**.
- Tasks: forwarding, trunking, encrypting, NAT.

### Control Plane
- Makes decisions about **how data is handled**.
- Sets rules and policies:
  - Routing tables, NAT tables, session management.

---

## Extend the Physical Architecture

- Devices (e.g. firewalls) separate tasks physically:
  - **Control Plane**: manages and configures.
  - **Data Plane**: handles data forwarding.

---

## Controlling Trust

### Adaptive Identity
- Considers:
  - IP, location, device, relationship to organization.
- Increases authentication strictness if risk is high.

### Threat Scope Reduction
- Fewer trust boundaries reduce attack surface.

### Policy-Driven Access Control
- Decisions based on a **predefined ruleset** and contextual identity.

---

## Security Zones

- Broad zone groupings for access management.
- **Origin and destination** are key:
  - Trusted / Untrusted
  - VPNs, departments (HR, IT, etc.)
- Zones can **allow or block** traffic by default.
- Example: block `Untrusted → Trusted`, allow `Trusted → Internal`.

---

## Policy Enforcement Point (PEP)

- Evaluates access requests.
- Controls connections between subjects and resources.
- Enforces decisions made by policy systems.

---

## Applying Trust in the Planes

### Policy Decision Point (PDP)
- **Policy Engine**:
  - Evaluates rules and external data.
  - Grants, denies, or revokes access.
- **Policy Administrator**:
  - Talks to PEP.
  - Issues access tokens or credentials.

---

## Zero Trust Across Planes

- **Control Plane** manages PDP logic.
- **Data Plane** handles traffic through PEP.
- Workflow:
  1. Subject requests resource.
  2. PEP checks with PDP.
  3. Access is allowed or denied based on trust policies.

