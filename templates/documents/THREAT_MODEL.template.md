# Threat model

- **System / feature:** [name]
- **Owner:** [person/team]
- **Date / version:** [YYYY-MM-DD]
- **Review trigger:** [major change, incident, release, etc.]

## Scope

[Components, APIs, data stores, trust boundaries, and what is out of scope.]

## Assets

| Asset | Sensitivity / importance | Where stored or processed |
|---|---|---|
| [asset] | [classification] | [locations] |

## Actors and trust boundaries

[Expected users, administrators, services, third-party providers, and potential attackers.]

## Data flows

[Describe or link a data-flow diagram. Show where sensitive data crosses boundaries.]

## Threats and mitigations

| Threat / abuse case | Likelihood | Impact | Existing control | Additional action / owner |
|---|---|---|---|---|
| [e.g. stolen token] | Low/Med/High | Low/Med/High | [control] | [action/owner/date] |

Consider authentication bypass, privilege escalation, injection, data exposure, secret leakage, dependency compromise, denial of service, unsafe deserialization, malicious uploads, and logging/monitoring gaps where relevant.

## Residual risks

[Risk intentionally accepted, why, who accepted it, and revisit date.]

## Validation

[Tests, security review, scanning, or other evidence used to validate mitigations.]
