# Disaster Recovery Metrics & Objectives

## Core Recovery Metrics
| Metric | Acronym | Definition | Key Considerations | Example |
|--------|---------|------------|---------------------|---------|
| **Recovery Time Objective** | RTO | Time to restore service functionality | - Includes all critical components<br>- Defines operational readiness | Database + web server restoration time |
| **Recovery Point Objective** | RPO | Acceptable data loss timeframe | - Measures data currency, not just availability<br>- Defines "usable" state | 12 months of restored data required |

## Reliability Engineering Metrics
| Metric | Acronym | Formula | Purpose | Optimization Strategies |
|--------|---------|---------|---------|--------------------------|
| **Mean Time To Repair** | MTTR | (Total repair time) / (Number of repairs) | Measures outage resolution efficiency | - Onsite spares<br>- Faster vendor SLAs<br>- Diagnostic tooling |
| **Mean Time Between Failures** | MTBF | (Total uptime) / (Number of failures) | Predicts system reliability | - Manufacturer specifications<br>- Historical performance analysis |

---

**Key Relationships:**
```mermaid
graph LR
A[Failure] --> B(MTTR = Downtime Duration)
B --> C[RTO Determines MTTR Target]
D[Uptime] --> E(MTBF = Reliability Period)
E --> F[Informs RPO Planning]
