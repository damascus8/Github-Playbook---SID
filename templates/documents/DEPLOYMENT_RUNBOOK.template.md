# Deployment and operations runbook

- **Service / system:** [name]
- **Owner / escalation:** [team/contact]
- **Last tested:** [YYYY-MM-DD]

## Purpose and dependencies

[What the system does, downstream/upstream dependencies, dashboards, logs, and alerts.]

## Access and prerequisites

[Required role/access, tooling, environment, and approvals. Never put credentials in this document.]

## Deploy steps

1. [Pre-deployment checks]
2. [Build/artifact/version verification]
3. [Migration/configuration steps]
4. [Deployment command or system procedure]
5. [Smoke test and success criteria]

## Monitoring and health checks

- Dashboard: [link]
- Logs/traces: [link]
- Primary alert(s): [name and meaning]
- Healthy state: [observable signals]

## Common failures

| Symptom / alert | Diagnostic step | Safe remediation | Escalation |
|---|---|---|---|
| [symptom] | [check] | [action] | [team/contact] |

## Rollback / recovery

[Link to `ROLLBACK_PLAN.template.md` or describe safe rollback steps, constraints, and who approves.]

## Data and security considerations

[Backups, access, PII/secret handling, audit trails, and actions that must not be taken.]

## Post-deployment checks

- [ ] Health checks succeed.
- [ ] Key user flow succeeds.
- [ ] Error rate/latency/queue depth are normal where relevant.
- [ ] No unexpected resource or permission change occurred.
- [ ] Release version and outcome are recorded.
