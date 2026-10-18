# Repository setup checklist

Use this checklist when starting a repository or applying the Playbook to an existing one. Mark items `Done`, `Not applicable`, or `Exception accepted`; do not silently skip them.

## Identity and access

- [ ] Repository description states purpose and primary language.
- [ ] Visibility is intentional (public/private); no credentials or sensitive data are included.
- [ ] Default branch is named and protected as far as the current plan allows.
- [ ] Write/admin access follows least privilege; remove stale collaborators and tokens.
- [ ] A license is chosen intentionally if the code is distributed.

## Documentation and collaboration

- [ ] README includes purpose, prerequisites, setup, configuration, test, and deploy/run instructions.
- [ ] CONTRIBUTING explains branch, commit, test, and PR expectations.
- [ ] SECURITY explains private vulnerability reporting.
- [ ] Changelog/release notes exist where users need to understand releases.
- [ ] Issue and PR templates help collect useful context.
- [ ] CODEOWNERS is accurate if used.
- [ ] Required project-specific documentation is present.

## Quality and automation

- [ ] Formatting/linting rules are documented or configured.
- [ ] Automated tests exist for important behavior.
- [ ] CI builds/tests the project on pull requests.
- [ ] Workflow permissions are restricted to the minimum needed.
- [ ] Actions and third-party dependencies are updated and reviewed.

## Security and operations

- [ ] Dependency graph and Dependabot alerts are enabled where available.
- [ ] Dependabot version updates are configured for actual ecosystems.
- [ ] Secret scanning / code scanning availability is checked for this repository's plan and visibility.
- [ ] Secrets are injected at runtime from environment settings or a secrets manager.
- [ ] Errors, logs, backups, recovery, and rollback are considered where applicable.
- [ ] Supported versions and maintenance expectations are documented.

## Exception record

For every uncompleted baseline control, record:

| Field | Value |
|---|---|
| Control | `[rule or checklist item]` |
| Reason | `[why it does not fit]` |
| Risk / impact | `[what remains exposed or difficult]` |
| Accepted by | `[owner/reviewer]` |
| Revisit date | `[date or release]` |
