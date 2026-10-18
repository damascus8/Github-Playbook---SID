# Maintenance and deprecation

## Ownership and support

Every production or widely reused project should state:

- who maintains it;
- which branches/versions are supported;
- where bug reports and security reports go;
- what maintenance level users can expect;
- how unsupported versions are identified.

Do not promise response times or support windows the maintainers cannot sustain.

## Deprecation process

1. Identify what is deprecated and why.
2. Provide a safe alternative and migration instructions.
3. Communicate the earliest removal version/date where feasible.
4. Add a warning or compatibility shim if practical.
5. Check usage and downstream dependencies before removal when data is available.
6. Record the change in release notes.

For public libraries, align this process with the documented versioning policy. For internal apps, coordinate with the teams and services that depend on the change.

## Routine review

At a cadence appropriate to project risk and activity, review:

- open security and dependency alerts;
- supported runtimes and major dependencies;
- failing/flaky CI jobs;
- issue and pull-request backlog;
- access permissions and deploy credentials;
- stale docs and dead links;
- backup, restore, monitoring, and rollback readiness for production systems.
