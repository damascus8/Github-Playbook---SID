# Profile: data pipeline or machine-learning project

## Documents to maintain

- [ ] README with environment setup, reproducible run commands, expected outputs, and resource assumptions.
- [ ] Data card: source, permissions/consent basis where applicable, fields, quality, limitations, retention, and lineage.
- [ ] Feature definitions and transformations, including time windows and leakage risks.
- [ ] Model card when a model is trained or shipped: purpose, intended/non-intended use, evaluation, limitations, and responsible owner.
- [ ] Experiment configuration and reproducibility requirements (seeds, versions, inputs, and known nondeterminism).
- [ ] Evaluation plan, metrics, baseline comparisons, and acceptance criteria.
- [ ] Monitoring plan for drift, failures, data quality, and business impact where the model is operational.
- [ ] Rollback/fallback plan for a deployed model or pipeline.
- [ ] Privacy/security analysis if personal, sensitive, licensed, or confidential data is used.

## Engineering checklist

- Do not commit raw sensitive datasets, exported customer data, or model artifacts containing restricted information.
- Record data provenance and permissions; a public download is not automatically unrestricted for every use.
- Separate training, validation, and test data appropriately; guard against leakage.
- Make transformations testable and pipelines rerunnable where possible.
- Track schema changes and validate incoming data before processing.
- Evaluate performance across relevant subgroups and document known limitations where appropriate.
- Monitor behavior after deployment; offline metrics are not enough for production use.
- Record model/dataset versions needed to reproduce a result.

## Templates

Use `DATA_CARD.template.md`, `MODEL_CARD.template.md`, `TEST_PLAN.template.md`, `THREAT_MODEL.template.md`, and `DEPLOYMENT_RUNBOOK.template.md`.
