# Technical Change Management Notes

## Change Execution
- Implement the change management plan.
- Upgrades are rarely simple—may involve many moving parts and events.
- Management determines *what* changes; technical team handles *how*.

## Application Control: Allow List / Deny List
- Applications may be dangerous (vulnerabilities, trojans, malware).
- Security policy controls execution using:
  - **Allow list**: Only listed apps can run (very restrictive).
  - **Deny list**: All apps can run except those listed (common for antivirus/malware).

## Restricted Activities
- Scope defines which components are affected.
- Change approval is limited—only allows specified actions.
- Scope may expand mid-process; documentation and policies must account for this.
- Change management process dictates next steps.

## Downtime Management
- Services may become unavailable during change.
- Prefer non-production hours for disruptive changes.
- Prevent downtime with secondary system failover.
- Automate and monitor the process to minimize events.
- Communicate clearly—send emails and update calendars.

## Restarts
- Commonly required to implement changes.
- Restart OS, services, or apps depending on context.
- Validate system recovery post-power loss.
- Services may need restarting; applications may need relaunching.

## Legacy Applications
- May be unsupported or undocumented.
- Often critical—document behavior and support it.
- Can be quirky—develop custom procedures.
- Over time, become the expert by maintaining it.

## Dependencies
- Some tasks depend on others (e.g., service/library prerequisites).
- Changing one component might require others to restart or update.
- Can span systems (e.g., upgrade firewall before the firewall manager).

## Documentation
- Must be updated as part of change management.
- Update:
  - **Diagrams**: Network config, addressing.
  - **Policies/Procedures**: New systems may need new rules.

## Version Control
- Tracks config/file changes over time.
- Allows reverting to earlier versions.
- Examples:
  - Router configurations
  - Windows OS patches
  - Registry entries
- May not be built-in—external tools might be required.

---

*Created from Professor Messer’s lecture slides and transcript.*
