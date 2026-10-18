# 30-minute quick start

This is the shortest practical path for a typical small or medium software repository. The exact time depends on your codebase and access to repository settings.

## 1. Identify the repository

Write down:
- What the application/library does and who uses it.
- Language(s), framework(s), runtime, and package manager.
- How to install dependencies, run tests, and build a release.
- Whether the repository is public or private and whether it stores sensitive data.
- The default branch name and deployment process.

## 2. Add the minimum documentation

Copy and complete these templates from `templates/repository-files/`:
- `README.template.md` → `README.md`
- `CONTRIBUTING.template.md` → `CONTRIBUTING.md`
- `SECURITY.template.md` → `SECURITY.md`
- `CHANGELOG.template.md` → `CHANGELOG.md` (for versioned projects)

Choose a license deliberately. Do not add an open-source license unless you intend to grant those rights.

## 3. Add repository hygiene files

Review and adapt:
- `.gitignore` for your actual language/framework.
- `.editorconfig` for your formatting preferences.
- `.gitattributes` for line endings and binary files.
- `CODEOWNERS` if ownership paths and reviewers are meaningful for your project.

## 4. Configure safe collaboration

1. Use short-lived branches for changes.
2. Open pull requests instead of pushing directly to the default branch.
3. Enable a branch rule or ruleset if available on your plan; see [branch rules](../01-git-workflow/branching-strategy.md).
4. Add the pull-request template and one or two issue templates.
5. Use a review checklist and require CI to pass before merging when practical.

## 5. Turn on free-first security checks

1. Enable Dependabot alerts and security updates in repository settings where available.
2. Commit `.github/dependabot.yml` with only the ecosystems actually used.
3. Check the repository's Security tab for secret scanning and code-scanning availability; public and private repositories do not have identical free feature access.
4. Ensure local `.env` files, tokens, private keys, certificates, and production data are not committed.

## 6. Add CI

Copy exactly one starter workflow that matches the project's actual stack from `templates/workflows/`. Edit the runtime version and build/test commands, run it on a branch, and fix it before requiring the check for merges.

Do not copy every workflow. More jobs are not automatically better.

## 7. Choose project-specific documents

Use [the project documentation matrix](../05-documentation/project-documentation-matrix.md), then open the relevant project profile in `docs/06-project-profiles/`.

## 8. Verify

- [ ] A new contributor can follow the README without asking for missing setup steps.
- [ ] Tests can be run from a clean clone.
- [ ] Pull requests show a useful checklist.
- [ ] CI runs on a test pull request.
- [ ] Dependency alerts are enabled where available.
- [ ] No secret is present in the working tree or Git history.
- [ ] Required project documents have an owner and are not stale.
