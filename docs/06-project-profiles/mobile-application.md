# Profile: Mobile application

Use this profile for Android, iOS, or cross-platform apps. Store policies and legal obligations change, so verify current platform rules before submission.

## Documents to maintain

- [ ] README: supported OS/runtime, development setup, build variants, and test steps.
- [ ] Architecture, key screens, data flow, local storage, and network boundaries.
- [ ] Permissions inventory: what each permission is for and where it is requested.
- [ ] Data inventory: data collected, purpose, storage, sharing, retention, deletion, and third-party SDK use.
- [ ] Privacy disclosures aligned with the actual code and SDK behavior.
- [ ] Release checklist for signing, versioning, store metadata, assets, and staged rollout.
- [ ] Compatibility matrix for OS/device versions and important limitations.
- [ ] Crash/error reporting, support, backup, and account/data deletion behavior when applicable.
- [ ] Threat model for tokens, deep links, local storage, exported components, and backend APIs.

## Engineering checklist

- Store secrets on trusted servers, not in app source or packaged configuration.
- Use platform secure storage for credentials and sensitive local material.
- Minimize permissions and request them only when needed.
- Validate deep links, intents, URLs, and exported entry points.
- Avoid sensitive values in crash reports, analytics, and logs.
- Test poor connectivity, offline behavior, expired sessions, device rotation/backgrounding, and OS permission denial.
- Document how signing keys are stored and who can access them; never commit keystores or provisioning secrets.
- Verify current Google Play / Apple App Store requirements before each release.

## Templates

Use `MOBILE_RELEASE_CHECKLIST.template.md`, `PRIVACY_DATA_INVENTORY.template.md`, `ARCHITECTURE.template.md`, and `THREAT_MODEL.template.md`.
