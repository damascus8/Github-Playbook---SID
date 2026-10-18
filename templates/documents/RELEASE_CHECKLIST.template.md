# Release checklist

- **Project/version:** [name/version]
- **Release owner:** [person/team]
- **Target date:** [YYYY-MM-DD]

## Before release

- [ ] Intended commit and version are confirmed.
- [ ] Required CI and tests pass.
- [ ] Security and dependency alerts are triaged.
- [ ] Changelog/release notes are accurate and user-facing.
- [ ] Configuration, migrations, and compatibility requirements are documented.
- [ ] Artifacts are reproducible and contain no secrets or unintended files.
- [ ] Deployment, monitoring, support, and rollback are ready.
- [ ] Approvals and signing credentials are available to authorized people only.

## Release

- [ ] Tag/package/store version matches the release notes.
- [ ] Publish/deploy steps completed.
- [ ] Critical smoke tests pass.
- [ ] Monitoring and user feedback checked.

## After release

- [ ] Release/commit/artifact references are recorded.
- [ ] Known issues and follow-up work are filed.
- [ ] Rollback trigger window is cleared or incident review started.
