# Branching strategy

## Default strategy: short-lived feature branches

Use the repository's default branch (often `main`) as the stable integration branch. Create a branch for each focused change, open a pull request, run checks, review, and merge.

Suggested names:

- `feat/add-sms-retry`
- `fix/duplicate-notification`
- `docs/update-setup-guide`
- `test/add-api-contract-tests`
- `refactor/split-message-service`
- `chore/update-dependencies`

Keep branches small and short-lived. Avoid long-running `develop`, `release`, or `integration` branches unless the team has a real release or coordination need.

## Branch rule baseline

Where the current GitHub plan supports it, protect the default branch with:

- Pull requests required for changes.
- At least one approval for collaborative projects; for solo projects, use self-review and passing CI where possible.
- Required CI status checks after the workflow names stabilize.
- Conversation resolution before merge.
- Restrict force pushes and deletion.
- Require linear history only if the team understands its merge/rebase workflow.

Do not require a status check before it has run successfully at least once and the exact check name is known. Do not add requirements that leave nobody able to merge or recover a broken rule.

## Merge method

Choose one method and explain it in CONTRIBUTING:

- **Squash merge:** usually simplest for small teams; one commit per PR.
- **Rebase and merge:** preserves individual commits but requires a clean history.
- **Merge commit:** preserves branch topology; useful when that history matters.

Avoid mixing methods without a reason. Never rewrite shared history casually.

## Emergency fix

Document who may approve an emergency bypass, how the fix is validated, and how a follow-up review is recorded. A bypass must be exceptional, traceable, and followed by remediation.

## Learn more

- [GitHub protected branches](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule)
- [GitHub rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)
