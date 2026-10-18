# Security baseline

This baseline is intended for ordinary software projects. High-risk systems need a threat-model-driven design and specialist review.

## Repository access

- Use least privilege: grant only the permissions people and automation need.
- Remove access promptly when it is no longer required.
- Keep personal access tokens short-lived and narrowly scoped when possible; prefer GitHub Apps or built-in workflow tokens for automation where appropriate.
- Restrict GitHub Actions token permissions at workflow or job level.
- Review new Actions, external services, and requested permissions before adoption.

## Protect the default branch

Where your plan supports it, require PRs, required checks, appropriate approvals, and restrict deletion/force-push. For private repos on GitHub Free, some branch-protection features may not be included; see the [free-tier guide](../00-start-here/github-free-tier.md).

## Dependencies

- Enable dependency graph and Dependabot alerts where available.
- Enable security updates and scheduled version updates where appropriate.
- Review release notes, compatibility, and lockfile changes before merging.
- Remove unused dependencies and avoid downloading packages from untrusted sources.
- Do not assume an alert-free project has no vulnerabilities.

## Secrets and sensitive data

- Never commit API keys, passwords, private keys, database dumps, customer records, or production exports.
- Use `.env.example` with fake values to document configuration; exclude real `.env` files.
- Inject secrets at runtime using repository/environment secrets or a dedicated secrets manager.
- Rotate a leaked secret immediately; deletion from the latest commit is not enough because Git history and logs may retain it.
- Avoid printing secrets in CI logs or error messages.

## Code and application security

- Validate and authorize inputs at trust boundaries.
- Use secure defaults and least privilege for service accounts.
- Protect authentication and authorization paths with tests.
- Use TLS for network traffic and approved encryption for sensitive stored data.
- Avoid logging tokens, session identifiers, passwords, or sensitive payloads.
- Apply safe timeout, retry, file upload, serialization, and error-handling practices.
- Keep supported runtimes and libraries current.

## Response when a secret is leaked

1. Revoke/rotate it immediately at the issuing service.
2. Identify the affected resources and potential misuse.
3. Remove it from current files and history if appropriate, but only after containment; history rewrites do not replace rotation.
4. Inspect logs and audit trails for misuse.
5. Notify affected parties when required by law, contract, or policy.
6. Add a prevention step and record the incident without copying the secret into the report.

## Feature limitations

GitHub's security feature availability depends on repository visibility and plan. Check the current official security feature matrix; do not promise free secret scanning or code scanning for every private repository.
