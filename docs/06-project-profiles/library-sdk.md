# Profile: library or SDK

Libraries need stronger compatibility and release discipline because other projects depend on them.

## Documents to maintain

- [ ] README with installation, minimum supported runtime, quick start, examples, and support policy.
- [ ] Public API reference and realistic usage examples.
- [ ] Compatibility matrix for runtime/platform versions.
- [ ] Versioning and deprecation policy.
- [ ] Changelog with migration notes and breaking changes.
- [ ] Contribution and release process, including tests across supported versions.
- [ ] License and notices for code and bundled assets.

## Engineering checklist

- Treat public APIs as contracts; document intended stability.
- Avoid breaking changes in patch/minor versions if following SemVer.
- Test the supported runtime matrix or clearly state its limits.
- Include examples that can be run in CI when practical.
- Keep dependencies minimal and review transitive licensing/security implications.
- Plan deprecation warnings and a removal timeline before removing widely used APIs.
- Do not publish credentials or generated local build output in packages.

## Templates

Use `README.template.md`, `CHANGELOG.template.md`, `TEST_PLAN.template.md`, and `RELEASE_CHECKLIST.template.md`.
