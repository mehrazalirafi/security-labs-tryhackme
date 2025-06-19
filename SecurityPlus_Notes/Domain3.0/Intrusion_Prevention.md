# Intrusion Prevention System (IPS) and Monitoring Summary

## Intrusion Prevention System (IPS)
- **Function**: Monitors network traffic and blocks malicious content in real-time.
- **Intrusions**: Targets exploits against OS, applications (e.g., buffer overflows, cross-site scripting).
- **Detection vs Prevention**:
  - **IDS (Intrusion Detection System)**: Alerts only, no blocking.
  - **IPS**: Stops intrusions before they reach the network.

## Failure Modes
- **Fail-Open**: System failure allows data flow (less secure, more available).
- **Fail-Closed**: System failure blocks all data (more secure, may disrupt service).

## Device Connections
### Active Monitoring
- **Inline Connection**: Device sits directly in the traffic path.
- **Real-time Blocking**: Stops malicious packets before reaching endpoints.
- **Risk**: Can introduce a single point of failure.

### Passive Monitoring
- **Out-of-Band**: Traffic copy sent to monitoring device via port mirror (SPAN) or network tap.
- **Cannot Block Traffic**: Used primarily for detection and alerting.
- **Safer Setup**: Less risk of interrupting service.

## Active vs Passive Summary
| Feature             | Active Monitoring (IPS)     | Passive Monitoring (IDS-like IPS)     |
|---------------------|-----------------------------|----------------------------------------|
| Traffic Blocking     | Yes                         | No                                     |
| Risk of Downtime     | Higher                      | Lower                                  |
| Inline              | Yes                         | No                                     |
| Detection Accuracy  | Real-time                   | Near real-time                         |
| Common Use Case     | Preventing attacks          | Alerting and logging                   |

