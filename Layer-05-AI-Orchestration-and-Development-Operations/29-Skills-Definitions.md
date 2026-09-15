# Skills Definitions

Skills are intentionally invoked capabilities coordinated by the Master Orchestrator. They are not assumed to run on every task.

## `place-search`
Parse place-discovery intent, constraints, geography, category, and required attributes. Produces a structured search plan.

## `entity-resolution`
Compare source records and determine match confidence using identity, geographic, contact, address, and category signals. Cannot auto-merge below approved confidence thresholds.

## `source-analysis`
Assess source coverage, permitted use, freshness, reliability, schema, and integration risk.

## `review-analysis`
Extract evidence-grounded topics, sentiment, aspect sentiment, and trends from permitted review material.

## `trust-analysis`
Evaluate trust signals, evidence coverage, anomalies, and confidence using the approved trust model.

## `ranking-analysis`
Evaluate candidate features and ranking behavior. Must preserve commercial separation and emit explainability metadata.

## `explanation-generation`
Convert structured evidence into localized user-facing reasons. Cannot invent support.

## `community-moderation`
Classify and route community contributions for spam, abuse, manipulation, PII, factual correction, and policy review.

## `localization`
Validate Arabic, English, RTL/LTR, mixed-language behavior, terminology, dates, numbers, and translation coverage.

## `security-review`
Perform threat, authorization, input, secrets, dependency, AI-tool, and abuse analysis.

## `data-governance`
Validate provenance, retention, classification, privacy, data ownership, and source governance.

## `architecture-review`
Evaluate boundaries, coupling, scalability, resilience, data ownership, and architectural consistency.

## `code-review`
Review correctness, maintainability, security, performance, tests, and adherence to project conventions.

## `test-generation`
Generate tests from acceptance criteria and known failure modes. Tests must not claim execution unless actually run.

## `observability-analysis`
Define logs, metrics, traces, alerts, dashboards, and correlation requirements.

## `incident-analysis`
Support triage, containment, impact analysis, recovery, evidence preservation, and post-incident actions.

## Invocation Rule
The orchestrator activates only skills relevant to the task. Security, privacy, provenance, and anti-fabrication constraints remain mandatory even when their specialist skill is not separately invoked.
