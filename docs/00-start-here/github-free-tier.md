# Free-first GitHub feature guide

GitHub changes plan packaging over time. Treat this page as a planning guide, not a price guarantee; verify the linked official documentation before relying on a feature for a critical repository.

## Practical baseline

| Capability | Free-first recommendation | Important limitation |
|---|---|---|
| Git repository, issues, PRs, Markdown docs | Use GitHub Free | Availability and collaboration features can vary by account type and plan. |
| Dependabot alerts | Enable for supported dependency ecosystems | Alert visibility does not mean every remediation is automatic. Review and test upgrades. |
| Dependabot security updates | Enable where available | May create pull requests only for supported, resolvable vulnerable dependencies. |
| Dependabot version updates | Use `.github/dependabot.yml` | Add only ecosystems and directories used by the project. |
| GitHub Actions | Use small, targeted workflows | Standard hosted runners are free for public repositories; private repositories have plan quotas and overage rules. Dependabot-triggered Actions have special billing treatment; verify current limits. |
| Branch protection / rulesets | Use for public repos on Free | GitHub Free supports protected branches/rulesets for public repos; private-repo availability may require a paid plan. |
| Secret scanning | Enable for public repositories | GitHub's official feature matrix distinguishes public from private repositories; private coverage can require paid security products. |
| Code scanning / CodeQL | Consider for public repositories | Advanced security coverage for private repositories may require a paid plan/product. |
| External CI / scanners | Prefer reputable free/open-source options if GitHub plan limits do not fit | A third-party service may have its own usage limits and terms. |

## Official sources to verify

- [GitHub plans and features](https://github.com/pricing)
- [GitHub Actions billing and included quotas](https://docs.github.com/en/billing/concepts/product-billing/github-actions)
- [About GitHub Advanced Security](https://docs.github.com/en/get-started/learning-about-github/about-github-advanced-security)
- [Quickstart for securing a repository](https://docs.github.com/en/code-security/getting-started/quickstart-for-securing-your-repository)
- [Branch protection rules](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule)
- [Rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)

## Avoid accidental costs

- Check Actions usage under billing before adding frequent matrix builds or long-running jobs to a private repository.
- Prefer one CI workflow with clear jobs over many duplicate workflows.
- Do not enable a paid marketplace app without checking pricing, required permissions, and renewal terms.
- Do not assume a green alert page means the project is secure; alerts need triage and fixes.
- Keep third-party GitHub Actions to the minimum needed. For higher-assurance projects, pin actions to full commit SHAs and review updates.
