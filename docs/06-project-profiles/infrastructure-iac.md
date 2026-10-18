# Profile: infrastructure or infrastructure-as-code

## Documents to maintain

- [ ] README with prerequisites, credentials setup, plan/apply/destroy commands, and environment names.
- [ ] Architecture and trust-boundary diagram.
- [ ] Environment/account/region matrix and resource ownership.
- [ ] Identity and permission model, including automation roles.
- [ ] State storage, locking, backup, and recovery procedure where stateful IaC is used.
- [ ] Change approval, plan review, deployment window, and rollback/recovery runbook.
- [ ] Cost assumptions and how to detect unexpected resource creation.
- [ ] Incident response and break-glass access process for critical infrastructure.

## Engineering checklist

- Keep cloud credentials and state secrets out of Git.
- Use least-privilege identities and separate production from non-production.
- Require review of plans that create, replace, or destroy resources.
- Pin module/provider versions where reproducibility requires it and review updates.
- Detect dangerous public exposure, excessive IAM permissions, encryption gaps, and missing logs.
- Test policy/checks before applying to production.
- Understand destructive commands and protect critical state/resources against accidental deletion.
- Document how to recover when state and real infrastructure diverge.

## Templates

Use `ARCHITECTURE.template.md`, `THREAT_MODEL.template.md`, `DEPLOYMENT_RUNBOOK.template.md`, `ROLLBACK_PLAN.template.md`, and `RELEASE_CHECKLIST.template.md`.
