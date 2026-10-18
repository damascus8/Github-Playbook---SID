# Commit message standard

Use a short imperative summary that explains the intent of the change. Be consistent, not ceremonial.

Recommended format:

```text
<type>(optional-scope): <imperative summary>

[optional body explaining why]

[optional footer: issue references or breaking change]
```

Common types:

- `feat`: user-visible capability
- `fix`: bug fix
- `docs`: documentation only
- `test`: tests only or test coverage
- `refactor`: code change without intended behavior change
- `perf`: performance improvement
- `build`: build/dependency tooling
- `ci`: CI workflow change
- `chore`: maintenance not covered above
- `revert`: reversal of an earlier change

Examples:

```text
feat(sms): retry temporary gateway failures
fix(api): reject duplicate request identifiers
docs: explain local development setup
test(auth): cover expired refresh tokens
```

Rules:

1. Prefer one logical change per commit.
2. Explain *why* in the body when the summary is not enough.
3. Link an issue when relevant, but do not fabricate issue IDs.
4. Never include passwords, API keys, private customer data, or internal incident details in commit messages.
5. Do not force-push rewritten commits to shared branches without coordination.

Conventional Commits is an optional stricter convention; it is helpful when automated changelog generation or semantic release is used. See [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).
