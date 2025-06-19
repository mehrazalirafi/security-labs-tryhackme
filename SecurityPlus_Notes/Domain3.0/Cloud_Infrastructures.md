# Cloud Computing Security Concepts

## 1. Cloud Responsibility Matrix
- Cloud models like IaaS, PaaS, and SaaS distribute security responsibilities differently.
- Cloud providers offer a **responsibility matrix** showing who manages what (customer vs. provider).
- These matrices vary between providers and may be contract-specific.
- Example:
  - SaaS: Most components are **provider-managed**.
  - IaaS: Many components are **customer-managed**.
  - Accounts and data are **always customer-managed**.

## 2. Hybrid Cloud Considerations
- Involves multiple cloud providers (public/private), adding complexity.
- Risks include:
  - **Mismatched configurations** (authentication, firewall).
  - **Diverse logs** with incompatible formats.
  - **Data leakage** risks from inter-cloud communication over the public internet.

## 3. Third-Party Vendors in the Cloud
- Includes infrastructure tools and cloud appliances.
- Require:
  - Ongoing **vendor risk assessments**.
  - **Incident response planning** involving all stakeholders.
  - **Constant monitoring** for anomalies and updates.

## 4. Infrastructure as Code (IaC)
- Infrastructure is defined using **code**, just like application development.
- Enables:
  - Version control of infrastructure.
  - Automated, consistent deployments.
  - Easy modification and replication of environments.

## 5. Serverless Architecture
- Also known as **Function as a Service (FaaS)**.
- Developers create server-side logic, which runs in **stateless containers**.
- Functions are:
  - **Event-triggered**, **ephemeral**, and **cost-efficient**.
  - **Managed by third-parties**, so OS-level security is offloaded.

## 6. Microservices and APIs
- Contrast to monolithic apps that do everything in one package.
- **Microservices** isolate components like UI, logic, and data.
- Benefits:
  - **Scalable**: Only scale needed services.
  - **Resilient**: One failure doesn’t crash the app.
  - **Secure**: Service-specific security and compliance possible.
- **APIs** are the “glue” enabling inter-service communication.

---
