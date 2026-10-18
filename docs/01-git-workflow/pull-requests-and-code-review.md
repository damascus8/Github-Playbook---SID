# Pull requests and code review

## A useful pull request contains

- The problem and intended outcome.
- A small, reviewable change with context.
- Tests run and relevant results.
- Screenshots, API examples, migration notes, or logs when they help review.
- Security, privacy, compatibility, and operational impact when relevant.
- Rollback or migration notes for risky changes.

## Author checklist

- [ ] Scope is focused and unnecessary changes are removed.
- [ ] Tests cover the behavior changed, including important failure paths.
- [ ] Documentation, configuration examples, and changelog are updated as needed.
- [ ] No secrets, access tokens, private keys, customer data, or local environment files are included.
- [ ] New dependencies and permissions are justified.
- [ ] Database changes and backwards compatibility are considered.
- [ ] CI passes, or failures are explained and tracked.

## Reviewer checklist

Review in this order:

1. **Correctness:** Does this solve the intended problem? Are edge cases handled?
2. **Design:** Is the change understandable and proportionate? Is there a simpler option?
3. **Security/privacy:** Are input, access, secrets, logging, and data handling safe?
4. **Reliability:** What happens on timeout, retries, duplicate events, partial failure, or restart?
5. **Maintainability:** Are names, tests, docs, and error messages useful?
6. **Operations:** Can this be deployed, observed, and rolled back safely?

Ask questions when context is missing. Distinguish blocking defects from suggestions. Explain the risk behind a requested change rather than relying on authority alone.

## Approval rule

For a solo repository, use a self-review checklist and automated checks. For collaborative repositories, aim for at least one independent review. High-risk changes may need two-person review or specialist review depending on project risk and team size.

## Pull request size

A PR that changes one coherent thing is usually easier to test and revert. If a PR is large, explain why and separate mechanical formatting or generated files when feasible.
