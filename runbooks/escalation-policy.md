# Escalation Policy

## Purpose
This document defines when and how incidents are escalated to ensure
timely resolution while minimizing unnecessary disruption.

Escalation is based on **impact and risk**, not blame.

---

## Severity Levels

### SEV-1 (Critical)
**Definition**
- Complete service outage
- Data loss or corruption risk
- Security incident in progress

**Response**
- Immediate escalation
- Incident commander assigned
- Continuous communication until resolution

**Escalation Targets**
- Platform Lead
- Engineering Manager
- Security Team (if applicable)

---

### SEV-2 (High)
**Definition**
- Partial outage
- Performance degradation affecting users
- Capacity exhaustion risk

**Response**
- On-call engineer leads mitigation
- Escalate if unresolved within defined SLA

**Escalation Targets**
- Senior SRE
- Platform Owner

---

### SEV-3 (Moderate)
**Definition**
- Degraded non-critical functionality
- No immediate customer impact

**Response**
- Handle during business hours
- No immediate escalation required

---

## Escalation Triggers

Escalation occurs when:
- Incident exceeds defined response time
- Risk of customer impact increases
- Mitigation attempts fail
- On-call engineer requires additional authority or expertise

---

## Communication Expectations

- Status updates at regular intervals during SEV-1/SEV-2 incidents
- Clear ownership of incident coordination
- Post-incident summary shared with stakeholders

---

## Principles
- Escalate early when in doubt
- Avoid escalation delays due to optimism bias
- Escalation is a support mechanism, not a failure
