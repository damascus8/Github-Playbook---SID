# Profile: CLI tool

## Documents to maintain

- [ ] README with install, upgrade, supported OS/shell/runtime, and examples.
- [ ] Full command and option reference, including defaults and environment variables.
- [ ] Exit-code table and error-message conventions.
- [ ] Configuration precedence, file permissions, and secret handling guidance.
- [ ] Compatibility/deprecation policy if scripts depend on the CLI.
- [ ] Release/install/distribution instructions and checksum/signature approach where appropriate.

## Engineering checklist

- Use stable exit codes and send diagnostics to stderr when appropriate.
- Provide `--help`; consider `--version`, dry-run, and non-interactive modes.
- Never print secrets from environment variables or config files.
- Quote/escape arguments safely; do not build shell commands from untrusted strings.
- Be explicit before destructive operations; provide dry-run where practical.
- Test supported shells, paths with spaces, non-ASCII input, and permission errors.
- Document whether commands are safe to rerun and how partial failures are handled.

## Templates

Use `README.template.md`, `TEST_PLAN.template.md`, `RELEASE_CHECKLIST.template.md`, and `ARCHITECTURE.template.md` where useful.
