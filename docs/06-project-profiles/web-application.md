# Profile: Web application

## Documents to maintain

- [ ] README with local setup, build, tests, deployment, and configuration.
- [ ] Architecture and key page/service/data flows for non-trivial apps.
- [ ] Environment-variable reference with safe sample values.
- [ ] Authentication, authorization, session, and logout behavior.
- [ ] Privacy/data collection and retention notes where personal data is handled.
- [ ] Deployment, rollback, health checks, and incident notes if hosted.
- [ ] API contract if the frontend consumes a separately maintained API.

## Engineering checklist

- Validate input on the server; browser-side validation is not a security boundary.
- Enforce authorization server-side for every protected operation.
- Use framework-supported escaping and avoid unsafe HTML injection.
- Use secure cookie/session settings and HTTPS in production.
- Configure security headers, including a Content Security Policy appropriate to the app.
- Avoid exposing private keys or server credentials in browser bundles.
- Consider dependency, accessibility, browser compatibility, and performance checks.
- Test empty/error/loading states and permission boundaries, not only the happy path.

## Templates

Use `README.template.md`, `ARCHITECTURE.template.md`, `THREAT_MODEL.template.md`, `TEST_PLAN.template.md`, and `DEPLOYMENT_RUNBOOK.template.md` as applicable.
