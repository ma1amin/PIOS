# Trust Engine

## Definition
PIOS trust represents confidence in the reliability of available evidence about a place or claim. It is not the same as customer satisfaction and must not be displayed as another star rating.

A place can have a high customer rating but weak evidence quality, or a moderate rating with strong evidence consistency.

## Signal Families
- Source reliability.
- Cross-source agreement.
- Data freshness.
- Entity-resolution confidence.
- Temporal consistency.
- Review distribution characteristics.
- Community corroboration.
- Verified business evidence.
- Anomaly indicators.
- Manipulation-risk indicators.
- Coverage/completeness.

## Conceptual Model
`Trust = f(source_reliability, cross_source_agreement, temporal_consistency, community_validation, freshness, entity_confidence, coverage, anomaly_penalty)`

The exact model and weights must be empirically validated, configurable, versioned, and monitored. Documentation must never present unvalidated weights as objective truth.

## Trust States
User-facing states can use:
- High confidence
- Moderate confidence
- Low confidence
- Insufficient evidence

The interface should explain the evidence behind a state in plain language.

## Anti-Manipulation Signals
Potential indicators include:
- Sudden review bursts.
- Highly repetitive text patterns.
- Coordinated account behavior.
- Unusual timing.
- Geographic inconsistencies.
- Extreme rating distribution changes.
- Identity conflicts.
- Abnormal contribution velocity.

These signals trigger risk scoring or investigation. They must not automatically produce public accusations of fraud.

## Versioning
Each assessment records:
- Trust model version.
- Input signal versions.
- Calculation time.
- Result.
- Key contributing factors.
- Confidence.
- Review/override history.

## Governance
Business users cannot directly alter trust. Administrative overrides require a documented reason, authorization, audit event, and expiration/review date when applicable.

## Calibration
Trust should be calibrated against known data-quality outcomes. Evaluation must examine false confidence, unnecessary skepticism, category differences, geographic bias, source bias, and manipulation resilience.
