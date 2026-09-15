# Decision Logs and Governance

## Architecture Decision Records
Use ADRs for material decisions.

### ADR Fields
- ID.
- Title.
- Status.
- Date.
- Decision owner.
- Context.
- Problem.
- Options considered.
- Decision.
- Rationale.
- Security impact.
- Privacy/data impact.
- Operational impact.
- Cost impact.
- Consequences.
- Rollback/exit strategy.
- Related documents.

## Governance Domains
- Data source governance.
- Canonical identity.
- Trust models.
- Ranking.
- AI models and tools.
- Security.
- Privacy.
- Retention.
- Community moderation.
- Business claiming.
- Monetization.
- Localization.
- Taxonomy.
- Country expansion.

## Change Classification
### Low
Local implementation with no material security/data/model behavior change.

### Medium
Cross-service change, new API behavior, material performance or operational change.

### High
Trust/ranking policy, sensitive data, authorization, destructive data, source rights, high-impact AI behavior, major infrastructure, or commercial-integrity change.

## High-Risk Requirements
High-risk changes require:
- Named owner.
- Independent review.
- Evaluation/test evidence.
- Security/privacy assessment.
- Migration/rollback.
- Audit record.
- Production approval.

## Governance Principle
PIOS must evolve deliberately. Important decisions should be explainable, reviewable, measurable, and recoverable. Governance exists to protect user trust and operational integrity without preventing normal engineering iteration.
