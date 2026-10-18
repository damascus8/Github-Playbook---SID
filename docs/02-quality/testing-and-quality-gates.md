# Testing and quality gates

A quality gate is a repeatable check that must pass before code is merged or released. Use gates that provide real signal; avoid adding checks just because they exist.

## Recommended levels

1. **Fast local checks:** formatter, linter, type checks where relevant.
2. **Unit tests:** small, deterministic tests for core behavior.
3. **Integration tests:** verify boundaries such as database, queues, files, or external services.
4. **Contract/end-to-end tests:** cover critical user and API flows where their cost is justified.
5. **Security/dependency checks:** dependency alerts and applicable static analysis.
6. **Release smoke tests:** verify the deployed build and a small set of critical paths.

Not every project needs every level. A small utility library and a payment processing service should not have identical test architectures.

## Minimum expectations

- Tests run from a clean checkout using documented commands.
- Tests are deterministic; flaky tests are tracked rather than ignored indefinitely.
- Critical business rules and failure conditions have coverage.
- Tests do not depend on production data or real production credentials.
- External systems are mocked, stubbed, sandboxed, or isolated as appropriate.
- Coverage percentage is a diagnostic, not a substitute for test quality.
- The pipeline fails clearly when a required check fails.

## Pull request gate

Start with build + unit tests + lint/format checks that can run reliably. Add integration/security jobs as appropriate. Make checks required only after validating them on normal and failure cases.

## When a test fails

1. Determine whether code, test, environment, or dependency behavior changed.
2. Reproduce locally or from logs without exposing secrets.
3. Fix the cause; do not repeatedly rerun until it happens to pass.
4. If an external outage caused a failure, document the reason and retry safely.
5. If a flaky test must be quarantined, create an issue with an owner and a revisit date.
