# Ranking Engine

## Objective
Ranking orders eligible candidates according to user intent and context while preserving organic integrity.

## Feature Families
- Text/semantic relevance.
- Category match.
- Service/attribute match.
- Geographic fit.
- Trust contribution.
- Quality evidence.
- Freshness.
- User constraints.
- Context-specific suitability.
- Risk penalties.
- Diversity controls.

## Conceptual Score
`FinalScore = Relevance + ContextFit + TrustContribution + GeographicFit + FreshnessContribution + QualitySignals - RiskPenalties`

This formula expresses feature families, not fixed production weights.

## Distance
Distance is contextual. For “closest pharmacy,” geographic fit may dominate. For “best cardiac specialist in Riyadh,” quality, specialization, and trust may justify longer travel.

## Hard Filters vs Soft Features
Hard constraints such as required service, open-now status when reliable, or explicit maximum radius should filter candidates before ranking. Preferences such as “prefer nearby” should influence scoring.

## Diversity
The result set should avoid unnecessary duplication:
- Multiple branches of one chain should not dominate unless strongly relevant.
- Results may diversify by neighborhood, price segment, or category subtype when this improves decision value.

## Commercial Separation
Sponsored placement must:
- Be clearly labeled.
- Use a separate commercial eligibility and placement mechanism.
- Never silently increase organic trust.
- Never rewrite organic rank features.
- Be auditable.

## Explainability
The ranking service should emit structured contribution metadata sufficient for the explanation layer, such as:
- Strong service match.
- High evidence confidence.
- Close distance.
- Recent positive trend.
- Limited evidence.

## Change Management
Ranking changes require:
1. Versioned configuration/model.
2. Offline benchmark.
3. Regression analysis.
4. Security/manipulation review where relevant.
5. Controlled online experiment when appropriate.
6. Monitoring.
7. Rollback capability.
