# Secrets and configuration

## Configuration is not the same as a secret

Normal configuration (feature flags, non-sensitive URLs, timeout settings) can often be documented. Passwords, private keys, access tokens, signing keys, production credentials, and sensitive personal information must not be committed.

## Recommended pattern

- Commit a `.env.example` containing variable names and safe fake values.
- Ignore `.env`, `.env.local`, and environment-specific secret files.
- Validate required variables at application startup and fail with a clear, non-sensitive message.
- Keep separate credentials for local, test, staging, and production environments.
- Inject credentials through repository/environment secrets or a managed secret store.
- Restrict who can read production secrets and who can approve deployments.

Example `.env.example`:

```dotenv
APP_ENV=local
LOG_LEVEL=INFO
DATABASE_URL=replace-me-locally
API_BASE_URL=http://localhost:8080
```

These values are examples only. Do not place real credentials in this file.

## If a secret reaches Git

Treat it as compromised even if the repository is private or the commit was quickly deleted. Revoke/rotate the credential first; then remove exposure, review access logs, and prevent recurrence. See the [security baseline](security-baseline.md).
