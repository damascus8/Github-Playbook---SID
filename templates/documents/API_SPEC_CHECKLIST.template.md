# API specification checklist

Use this to review an API specification or OpenAPI document. It is a checklist, not a substitute for a versioned machine-readable contract.

## Contract

- [ ] Base URL and API versioning approach are clear.
- [ ] Each endpoint defines method, path, purpose, and required permissions.
- [ ] Request path/query/header/body fields have types, constraints, and examples.
- [ ] Success and error response schemas are documented.
- [ ] Authentication and authorization requirements are specified.
- [ ] Pagination, filtering, sorting, idempotency, rate limits, and timeouts are documented where applicable.
- [ ] Date/time, currency, locale, null, and identifier formats are consistent.
- [ ] Deprecated endpoints include a migration path and removal policy.

## Security and reliability

- [ ] Sensitive fields are not returned unnecessarily.
- [ ] Input validation and size limits are defined.
- [ ] Errors do not leak stack traces, secrets, or internal infrastructure details.
- [ ] Retry behavior and idempotency are clear for operations with side effects.
- [ ] Backwards compatibility has been evaluated.
- [ ] Examples use fake values, never real tokens or personal data.

## Operations

- [ ] Logging/trace IDs and support diagnostics are described if users need them.
- [ ] Dependent services and failure behavior are understood.
- [ ] Contract tests or validation run in CI where practical.
