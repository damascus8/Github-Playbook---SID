# Profile: API or backend service

Use this profile for HTTP APIs, event-driven services, background workers, and backends that own business logic or persistent data.

## Documents to maintain

- [ ] README: local run, test, environment setup, health checks, and build.
- [ ] Architecture / component diagram and important dependencies.
- [ ] API contract (OpenAPI or an equivalent source of truth) if the service exposes HTTP endpoints.
- [ ] Authentication and authorization model, including service-to-service access.
- [ ] Data model, migrations, retention, and backup/restore approach if data is persisted.
- [ ] Error format, status codes, idempotency, pagination, timeout, retry, and rate-limit behavior where relevant.
- [ ] Threat model and data-flow diagram for sensitive or internet-facing paths.
- [ ] Runbook: dashboards/logs, alerts, common failures, escalation, and safe manual actions.
- [ ] Deployment and rollback / migration compatibility guide.
- [ ] SLO/SLA or availability targets if the service is production-critical.

## Engineering checklist

- Validate data at system boundaries and authorize every sensitive operation.
- Avoid logging secrets and full sensitive payloads.
- Make retry behavior bounded and idempotent where duplicate requests/events are possible.
- Set connect/read/request timeouts for network calls.
- Handle partial failures and graceful shutdown.
- Test authentication failures, permission boundaries, validation, and retry/timeout paths.
- Keep health/readiness checks meaningful; do not expose sensitive diagnostics publicly.
- Document schema migration sequencing for rolling deployments.

## Templates

Start with `templates/documents/ARCHITECTURE.template.md`, `API_SPEC_CHECKLIST.template.md`, `THREAT_MODEL.template.md`, `TEST_PLAN.template.md`, and `DEPLOYMENT_RUNBOOK.template.md`.
