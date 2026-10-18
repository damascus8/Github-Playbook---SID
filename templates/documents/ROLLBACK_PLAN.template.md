# Rollback and recovery plan

- **Change / release:** [name/version]
- **Owner / approver:** [person/team]
- **Last validated:** [YYYY-MM-DD]

## Rollback trigger

[Observable conditions that warrant rollback, such as elevated errors, failed health checks, data integrity risk, or failed critical flows.]

## Preconditions and constraints

[Required access, backups, migration compatibility, stateful changes, and actions that are unsafe.]

## Steps

1. [Stop or pause rollout if applicable]
2. [Select last known-good artifact/configuration]
3. [Execute the rollback procedure]
4. [Handle database/schema changes safely; never assume code rollback reverses data migrations]
5. [Verify critical flows and monitoring]
6. [Communicate status and record the outcome]

## Success criteria

[Define healthy state and how to confirm it.]

## Recovery if rollback fails

[Escalation path and tested recovery option.]

## Follow-up

[Incident review owner, issue links, and corrective actions.]
