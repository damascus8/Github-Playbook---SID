# Dependency management and Dependabot

## Two different jobs

- **Dependabot alerts** notify you when GitHub detects a known vulnerability in a supported dependency.
- **Dependabot security updates** may open pull requests to update vulnerable dependencies.
- **Dependabot version updates** create scheduled pull requests for newer versions based on `.github/dependabot.yml`.

Alerts and update pull requests are not the same thing. An update must still be reviewed, tested, and released.

## Setup steps

1. In repository Settings, open the security / code security area (the label can change as GitHub updates the UI).
2. Enable the dependency graph and Dependabot alerts where available.
3. Enable Dependabot security updates where available.
4. Copy one ecosystem example from `templates/dependabot/` to `.github/dependabot.yml`.
5. Check that `directory` matches where the package manifest/lockfile actually lives.
6. Commit the file and confirm that Dependabot reports the expected package manager.
7. Review the first pull requests before allowing any automatic merge behavior.

## Rules for a safe setup

- Add only ecosystems actually present in the repository.
- Prefer weekly updates as a reasonable starting point; larger teams may need a different cadence.
- Group compatible minor/patch updates to reduce pull-request noise, but keep security updates visible and do not obscure major changes.
- Keep lockfiles committed when the package manager uses them.
- Do not auto-merge major upgrades or production-critical dependencies without passing checks and a clear rollback plan.
- Review permissions of GitHub Actions dependencies too.

## Alert triage priority

1. Exploitable vulnerability in a production path or internet-facing component.
2. Critical/high severity dependency with a feasible attack path.
3. Runtime/build tool vulnerability with meaningful impact.
4. Low-risk development-only issue or non-exploitable path.

This ordering is a starting point, not a substitute for assessing exploitability, exposure, available fixes, and the project's threat model. Record accepted risks with an owner and revisit date.

## Official documentation

- [About Dependabot alerts](https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts)
- [Configuring Dependabot version updates](https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file)
- [About Dependabot security updates](https://docs.github.com/en/code-security/dependabot/dependabot-security-updates/about-dependabot-security-updates)
