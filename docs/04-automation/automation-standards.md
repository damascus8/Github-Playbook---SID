# Automation standards

Automate repeatable checks and routine maintenance, not judgment that needs context.

## Workflow design

- Use clear workflow and job names.
- Trigger checks on pull requests and the default branch where useful.
- Set the minimum `permissions` required; start with read-only permissions.
- Pin third-party Actions to full commit SHAs for higher-assurance repositories. If using version tags for beginner convenience, review updates and supply-chain risk.
- Keep secrets out of workflow files and logs.
- Set timeouts for jobs that could hang.
- Avoid writing to the repository unless the job truly needs it.
- Separate untrusted pull-request code from privileged workflows and secrets.
- Do not use `pull_request_target` to check out and execute untrusted pull-request code with privileged permissions.
- Make the failure actionable: show which command failed and where logs are available.

## CI job responsibilities

A starter CI pipeline generally performs:

1. Checkout source.
2. Set up the required runtime.
3. Install dependencies using the project's standard lockfile/command.
4. Run lint/format or static checks.
5. Run unit tests.
6. Build/package the project.
7. Upload diagnostics only when useful and safe.

Add integration tests, coverage thresholds, scanning, or deployment only when the project benefits and the cost/complexity is understood.

## Workflow templates

Examples in `templates/workflows/` are starters, not universal drop-in CI. Validate runtime versions, package-manager names, test commands, permissions, and required check names against the real repository.

## Cost controls

Public repositories can use standard GitHub-hosted Actions runners without charge under GitHub's published policy. Private repositories have plan-dependent included minutes and storage. Use focused jobs, avoid unnecessary schedules, and review billing. See the [free-tier guide](../00-start-here/github-free-tier.md).
