# Incident: Snapshot Sprawl Leading to Datastore Saturation

## Incident Summary
Automated VM snapshot cleanup failed due to expired credentials,
resulting in uncontrolled snapshot growth and datastore saturation.

## Impact
- Multiple VMs experienced performance degradation
- Risk of service outage due to datastore exhaustion
- Manual remediation required over extended duration

## Timeline
| Time | Event |
|-----|------|
| T0 | Snapshot cleanup automation failed |
| T+2 months | Datastore usage reached critical levels |
| Detection | Manual investigation |
| Mitigation | Snapshot deletion and disk consolidation |

## Root Cause
Credential rotation was not reflected in the snapshot automation configuration,
causing silent failures.

## Contributing Factors
- Missing alert on automation failure
- No datastore growth alert tied to snapshots
- Long retention window without validation

## What Went Well
- Data integrity preserved
- Manual consolidation successful

## What Went Wrong
- Automation failure went unnoticed
- Alerting gaps
- Extended remediation time

## Action Items
- Add monitoring for snapshot job failures
- Alert on abnormal snapshot growth
- Periodic validation of automation credentials

## Lessons Learned
Automation requires monitoring. Silent failures are operationally dangerous.

## Escalation
This incident did not trigger formal escalation due to delayed detection.
Earlier escalation could have reduced remediation time.

