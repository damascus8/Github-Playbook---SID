# Contributing to [Project name]

Thanks for considering a contribution.

## Before you start

- Read the README and relevant architecture/design docs.
- Check open issues and avoid duplicating work.
- For major behavior changes, open an issue or design discussion first.
- Never include secrets, real customer data, or confidential company information.

## Development setup

1. Install [runtime/tooling versions].
2. Configure local environment variables using `.env.example` or the documented method.
3. Run `[test command]` and `[lint/build command]` before changing code.

## Branch and commit conventions

Use branches such as `feat/short-description`, `fix/short-description`, `docs/short-description`, or `chore/short-description`.

Commit format: `[type](optional-scope): summary` — see the project's commit-message guide if included.

## Pull requests

- Explain the problem, solution, and trade-offs.
- Add tests for changed behavior and important failure modes.
- Update docs/changelog/config examples as needed.
- Confirm CI passes; explain any failure that is unrelated to your change.
- Request review from the owning person/team if CODEOWNERS is configured.

## Quality and security

Do not commit generated build output, local `.env` files, credentials, private keys, or sensitive datasets. Report potential vulnerabilities privately using `SECURITY.md`.
