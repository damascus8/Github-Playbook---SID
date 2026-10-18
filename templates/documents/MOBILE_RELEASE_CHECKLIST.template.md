# Mobile app release checklist

- **App/version/build:** [name/version/build number]
- **Platforms:** Android / iOS / other
- **Release owner:** [person/team]

## Build and signing

- [ ] Production build variant selected.
- [ ] Version/build number updated.
- [ ] Signing credentials are stored securely and not committed.
- [ ] App permissions and exported components reviewed.
- [ ] Crash reporting / analytics do not capture secrets or unnecessary sensitive data.

## Privacy and store readiness

- [ ] Actual data collection and third-party SDK behavior reviewed.
- [ ] Store privacy/data-safety disclosures match the current app and SDKs.
- [ ] Permission prompts and rationale are accurate.
- [ ] Account/data deletion path is available if required by the app and current platform policy.
- [ ] Current store policies and review requirements checked.
- [ ] Store screenshots, description, icons, support URL, and privacy policy are current.

## Test and rollout

- [ ] Supported OS/device matrix tested.
- [ ] Login/logout, network failure, offline/restore, upgrade, and permission-denial paths checked.
- [ ] Backend compatibility and minimum supported API version verified.
- [ ] Staged rollout/monitoring plan agreed.
- [ ] Crash-free rate, critical flows, and rollback criteria identified.
- [ ] Release notes and support plan ready.
