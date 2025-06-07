# Change Management Notes

## Change Management
- Involves making changes like software upgrades, firewall config, or switch port updates.
- Frequent risk in enterprise environments.
- Often overlooked—needs clear policies (frequency, process, rollback).
- Can be difficult due to corporate culture resistance.

## Change Approval Process
- Formal process to avoid confusion, downtime, and mistakes.
- Steps:
  - Complete request forms
  - Define change purpose
  - Identify change scope
  - Schedule date/time
  - Determine system impact
  - Analyze risk
  - Get approval
  - Confirm user acceptance

## Ownership
- Owners request the change but don’t execute it.
- They manage the process and verify the change.
- Example: shipping dept owns label upgrade, IT performs it.

## Stakeholders
- Anyone affected by the change (often non-obvious).
- E.g. shipping label software affects shipping, accounting, delivery, CEO visibility.

## Impact Analysis
- Risk values: high, medium, low.
- Risks: fix fails, breaks something else, OS fails, data corruption.
- Not changing can lead to vulnerabilities, downtime.

## Test Results
- Use sandbox environment to test upgrades safely.
- Validate the upgrade before production deployment.
- Confirm backout plan works.

## Backout Plan
- Always have a way to revert changes.
- Not always easy; some changes are hard to undo.
- Always maintain good backups.

## Maintenance Window
- Choose timing carefully.
- Avoid workday, prefer overnight or off-hours.
- Consider seasonal factors (e.g. holidays freeze changes).

## Standard Operating Procedure (SOP)
- Change management must be documented.
- Available on intranet with other SOPs.
- SOPs evolve with updated practices.
