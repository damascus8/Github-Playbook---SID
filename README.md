# GitHub Standard Playbook

**A practical, free-first guide to making software repositories consistent, maintainable, and safer.**

This repository is a handbook and a collection of copy-ready templates. It is designed for a beginner who wants to apply sensible engineering standards to an existing repository without buying a tool or adopting an unnecessarily complicated process.

> **Important:** This Playbook documents standards and supplies templates. It does not automatically enforce rules on other repositories. Apply the selected files, change the project-specific placeholders, and configure GitHub repository settings as described in the guides.

## Start here

1. Read [the 30-minute quick start](docs/00-start-here/quick-start.md).
2. Follow [the beginner-friendly GitHub publishing steps](docs/00-start-here/publish-this-playbook.md) to create this one repository.
3. Understand [why this repository is not named `.github`](docs/00-start-here/github-repository-special-cases.md).
4. Follow the [repository setup checklist](docs/00-start-here/repo-setup-checklist.md).
5. Choose the documents your project needs using the [project documentation matrix](docs/05-documentation/project-documentation-matrix.md).
6. Copy the relevant files from [`templates/`](templates/) into your repository.
7. Configure repository settings using the [security baseline](docs/03-security/security-baseline.md) and [free-tier guide](docs/00-start-here/github-free-tier.md).
8. Review the checklist at the end of each guide and record any accepted exceptions.

## What is inside?

| Area | What you will learn or copy |
|---|---|
| Git workflow | Branch naming, commit messages, pull requests, code review, versioning |
| Repository hygiene | README, contribution guide, changelog, `.gitignore`, `.editorconfig`, CODEOWNERS |
| Security | Least privilege, dependency alerts, secret handling, vulnerability reporting |
| Automation | CI templates, Dependabot examples, quality gates and alert triage |
| Project documentation | Which documents belong in an API, web, mobile, CLI, library, data/ML, or infrastructure project |
| Engineering documents | PRD, architecture, ADR, API specification, threat model, test plan, runbook, rollback plan, postmortem |

## Recommended baseline

For most non-trivial repositories, aim for:

- A useful README with setup, configuration, testing, and deployment instructions.
- A predictable branch and pull-request workflow; do not develop directly on the default branch.
- Automated build and tests on every pull request where CI is practical.
- Dependency alerts and version-update automation where the ecosystem is supported.
- No secrets committed to Git; use environment variables or a secret manager.
- A clear license for distributed/open-source code, plus a security contact or reporting path.
- Documentation appropriate to the risk and complexity of the project, not documents written just to fill a folder.

See [the documentation matrix](docs/05-documentation/project-documentation-matrix.md) before deciding which documents are required.

## Principles

1. **Secure by default, practical by design.** Prefer protections that reduce real risk without adding ceremony.
2. **Automate repeatable checks.** People should spend review time on design and behavior, not avoidable formatting errors.
3. **Make every rule explainable.** Each standard should say what to do, why it matters, and how to verify it.
4. **Adapt by project type.** A library and a mobile app do not need identical documents.
5. **Keep the default free.** Paid features are clearly labelled as optional alternatives, never assumed prerequisites.
6. **Review exceptions explicitly.** If a rule does not fit, record why, who accepted the risk, and when to revisit it.

## Repository map

```text
.
├── .github/                      # Playbook repo's own issue templates and automation
├── .markdownlint.json            # Markdown lint rules used by this repository
├── docs/
│   ├── 00-start-here/            # First steps and account-plan notes
│   ├── 01-git-workflow/          # Branches, commits, reviews, releases
│   ├── 02-quality/               # Tests, quality gates, documentation style
│   ├── 03-security/              # Security and dependency practices
│   ├── 04-automation/            # CI and bot/alert operations
│   ├── 05-documentation/         # Document standards and project matrix
│   ├── 06-project-profiles/      # Requirements by app/project type
│   └── 07-maintenance/           # Maintenance and deprecation
├── templates/
│   ├── repository-files/         # README, SECURITY, CODEOWNERS, etc.
│   ├── github/                   # Issue and pull-request templates
│   ├── workflows/                # Optional CI workflow examples
│   ├── dependabot/                # Ecosystem-specific Dependabot examples
│   └── documents/                # ADR, threat model, runbook, test plan, etc.
└── LICENSE
```

## How to use the templates

- Copy only the files relevant to your project.
- Replace every `TODO`, `[placeholder]`, example owner, branch, runtime, and contact.
- Validate workflows against your actual build commands before enabling required checks.
- Use only the Dependabot ecosystem configuration that matches the package managers in your repository.
- Do not treat a sample as legal advice, a complete threat model, or a guarantee of security.

## Free-first promise

The guide prioritizes GitHub Free features and free/open-source tooling. Some security features are free only for public repositories; private-repository availability varies by plan. See [GitHub Free-tier notes](docs/00-start-here/github-free-tier.md) and verify the current official GitHub plan documentation before enabling a feature.

## Contributing

Suggestions and corrections are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). Keep the handbook beginner-friendly, vendor-aware, and explicit about paid-feature limits.

## License

The Playbook's documentation and templates are offered under the MIT License. Review the license before reusing the material in another context.
