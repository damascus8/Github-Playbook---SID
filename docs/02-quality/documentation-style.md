# Documentation style standard

Write documentation for the person who has not seen the project before.

## General rules

- Use clear headings and short sections.
- Explain what the reader needs, why it matters, and what success looks like.
- Include prerequisites before commands.
- Put commands in fenced code blocks and name the shell or language when needed.
- Mark placeholders clearly, for example `<OWNER>` and `<REPOSITORY>`; never present placeholders as real values.
- State tested runtime and dependency versions where reproducibility depends on them.
- Include expected output or a verification step for non-obvious instructions.
- Keep screenshots current and provide text instructions too.
- Add a source link for GitHub feature limits, standards, or security claims likely to change.
- Avoid committing secrets, customer information, internal URLs, or production identifiers in examples.

## README order for most software

1. Name and one-sentence purpose
2. Status / supported platform / compatibility
3. Features and non-goals
4. Prerequisites
5. Quick start
6. Configuration and environment variables
7. How to test
8. How to build, run, and deploy
9. Architecture or data flow (if non-trivial)
10. Security and privacy notes
11. Known limitations / troubleshooting
12. Contributing and support
13. License

Adapt this order for libraries, CLIs, and mobile apps as appropriate.

## Documentation ownership

Give operationally important docs an owner or owning team. Review them when commands, APIs, permissions, data flows, deployment steps, or supported versions change.
