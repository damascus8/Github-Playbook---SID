# Project documentation matrix

Use this matrix to decide which documents belong in a project. It is not a demand to create every file for every repository. A 100-line utility does not need the same paperwork as a mobile app that handles personal data.

**Legend:** `Required` = expected for the project type unless a recorded exception exists; `Recommended` = add when useful; `Conditional` = required only if the described feature/risk exists.

| Document | All non-trivial projects | API / backend | Web app | Mobile app | CLI | Library / SDK | Data / ML | Infra / IaC |
|---|---|---|---|---|---|---|---|---|
| README / setup / run / test | Required | Required | Required | Required | Required | Required | Required | Required |
| Contribution guide | Recommended | Recommended | Recommended | Recommended | Recommended | Recommended | Recommended | Recommended |
| License (when distributed) | Conditional | Conditional | Conditional | Conditional | Conditional | Required if open source | Conditional | Conditional |
| Security reporting policy | Required for public/shared projects | Required | Required | Required | Recommended | Required for public packages | Required if handling data | Required |
| Changelog / release notes | Recommended | Recommended | Recommended | Required for store releases | Recommended | Required | Recommended | Recommended |
| Architecture overview | Recommended | Required | Required | Required | Recommended | Recommended | Required | Required |
| ADRs for material decisions | Recommended | Recommended | Recommended | Recommended | Recommended | Recommended | Recommended | Recommended |
| API contract / OpenAPI | Conditional | Required if HTTP API | Conditional | Conditional | Conditional | Conditional | Conditional | Conditional |
| Data model / migration guide | Conditional | Required if persistent data | Conditional | Conditional | Conditional | Conditional | Required if data pipeline | Conditional |
| Threat model / data flow | Risk-based | Required for sensitive/high-risk paths | Required if sensitive/high-risk | Required if personal/sensitive data | Recommended | Recommended | Required for sensitive data/model use | Required for sensitive infrastructure |
| Privacy / data collection disclosure | Conditional | Conditional | Conditional | Required when collecting/sharing personal data | Conditional | Conditional | Required where personal data is processed | Conditional |
| Test plan | Recommended | Recommended | Recommended | Required for major releases | Recommended | Required for compatibility claims | Required | Required for deployment changes |
| Deployment / operations runbook | Conditional | Required if operated as a service | Required if hosted | Recommended | Conditional | Not usually | Required if pipeline operated | Required |
| Rollback / recovery plan | Risk-based | Required for production services | Required for production | Required for staged rollout | Conditional | Required for breaking package releases | Required for production pipeline/model | Required for stateful changes |
| API / command reference | Conditional | Required for public/consumed API | Recommended | Recommended | Required | Required | Recommended | Required for modules/interfaces |
| Model card / data card | Not usually | Not usually | Not usually | Not usually | Not usually | Not usually | Required for meaningful ML/data products | Not usually |
| Environment / permissions matrix | Recommended | Required for multiple environments | Required for multiple environments | Recommended | Recommended | Recommended | Required if data access differs | Required |

## Document rules by risk

Create more documentation when a project:

- handles personal, financial, health, authentication, or other sensitive data;
- exposes an internet-facing API or privileged automation;
- stores data that cannot be reconstructed easily;
- makes irreversible changes or has a complex release/rollback process;
- is a dependency for other teams or customers;
- includes machine-learning decisions that require evaluation, explainability, or monitoring.

## Start small

For a small hobby app, start with README, configuration example, test instructions, security contact/policy, and a deployment/rollback note if it is hosted. Add specialist documents when the profile and risks call for them.

See the matching profile for the full checklist: `docs/06-project-profiles/`.
