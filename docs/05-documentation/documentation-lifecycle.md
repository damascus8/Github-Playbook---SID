# Documentation lifecycle

Documentation is part of the code change, not a one-time ceremony.

## Ownership

Each important document should have a maintainer or owning team. The owner is responsible for keeping it understandable and reviewing it after material changes.

## Review triggers

Update the relevant docs when a change modifies:

- public APIs, commands, permissions, or user-visible behavior;
- supported languages, runtimes, dependency versions, or platforms;
- environment variables, secrets, configuration defaults, or data handling;
- schemas, migrations, retention, or data flows;
- deployment, monitoring, recovery, or rollback steps;
- support policy, release process, or deprecation timeline.

## Staleness check

At least before a release or major milestone, test the README from a clean environment, check links, confirm supported versions, and verify that runbooks match real operational procedures. Choose an interval that matches project activity and risk; do not invent a calendar ritual that nobody performs.

## Archive or remove docs

When a feature or platform is removed, move needed historical context to an archive or release note and remove misleading instructions. Mark obsolete docs clearly; avoid leaving multiple apparently authoritative guides.
