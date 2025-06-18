# Video Summary: Indicators of Compromise (IOCs)

## What is an IOC?
- An IOC (Indicator of Compromise) is any evidence suggesting an intrusion.
- Examples include:
  - High network activity
  - Changed file hash values
  - Unexpected international traffic
  - DNS modifications
  - Unusual login times or file access patterns

## Account Lockout
- May indicate brute-force or impersonation attacks.
- Lockouts due to exceeded login attempts or admin disablement may be part of a social engineering scheme (e.g., attacker calls support pretending to be the user).

## Concurrent Session Usage
- Implies a user logged in from multiple places simultaneously.
- May indicate compromise unless explained by mobile devices or automation.

## Blocked Content
- Attackers may block update or antivirus websites to retain access.
- Unable to update security tools is a red flag.

## Impossible Travel
- Logins from geographically distant locations in a short time.
- Log analysis should catch this anomaly easily.

## Resource Consumption
- Sudden spikes in bandwidth or file transfers, especially off-hours.
- Often the first sign of attacker activity.

## Resource Inaccessibility
- Servers or resources unavailable could be due to attacks.
- Includes:
  - Server crashes
  - Network disruption
  - Encrypted files (ransomware)
  - Locked accounts (brute-force)

## Out-of-Cycle Logging
- Logs at unexpected times may indicate compromise.
- Unusual update or patch installations raise red flags.
- Firewall logs can capture suspicious traffic flows.

## Missing Logs
- Logs are crucial evidence.
- Attackers may delete logs to cover their tracks.
- Monitor for missing authentication, file access, proxy, and server logs.

## Published/Documented Breach
- Data may be published online without the organization knowing.
- May be part of a ransomware attack.
- Often released publicly or sent to researchers to trace its origin.
