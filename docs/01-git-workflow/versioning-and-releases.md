# Versioning and releases

Use versions that help users understand compatibility and change. For public libraries and APIs, [Semantic Versioning](https://semver.org/spec/v2.0.0.html) is a useful default where a stable public API exists.

For `MAJOR.MINOR.PATCH`:

- **MAJOR:** an incompatible public API or behavior change.
- **MINOR:** backward-compatible functionality.
- **PATCH:** backward-compatible fixes.

Before version 1.0.0, compatibility expectations can be less stable, but breaking changes still need clear release notes.

## Release checklist

- [ ] CI and required tests pass on the release commit.
- [ ] Dependency and security alerts have been reviewed.
- [ ] Changelog/release notes describe features, fixes, breaking changes, and migration steps.
- [ ] Database migrations and configuration changes are documented.
- [ ] Artifact/package is built reproducibly and versioned consistently.
- [ ] Deployment, rollback, and post-release verification are ready.
- [ ] No secrets or private information are present in release artifacts.
- [ ] Tag and release notes point to the intended commit.

## Changelog guidance

Use an `Unreleased` section and group changes under `Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, and `Security` as needed. Keep entries user-facing; avoid dumping raw commit messages.

## Releases for different project types

- Application: a release may be a deployment rather than a public version number; still record what changed and how to roll back.
- Library/SDK: compatibility and deprecation promises matter; version carefully.
- Mobile app: include store review status, permissions/data disclosures, and rollout/rollback plan.
- Infrastructure: include plan output, approvals, state/backup considerations, and recovery procedure.
