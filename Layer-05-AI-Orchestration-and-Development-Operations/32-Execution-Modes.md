# Execution Modes

## Balanced Mode
Default mode for ordinary search and product operations. Balances relevance, trust, latency, and evidence depth.

## Strict Mode
Use when the decision requires higher confidence or the category carries greater consequence. Behavior:
- Higher evidence thresholds.
- Stronger freshness requirements.
- More conservative explanations.
- Fewer unsupported recommendations.
- Greater human-review use for data conflicts.

## Exploratory Mode
Use for broad discovery:
- Wider candidate set.
- More category/geographic exploration.
- Clear uncertainty.
- No relaxation of security or factual integrity.

## Deep Research Mode
Use for complex comparisons:
- More evidence retrieval.
- Cross-source reconciliation.
- Detailed explanation.
- Explicit conflicting evidence.
- Longer acceptable latency.

## Degraded Mode
Automatically enter when dependencies are unavailable:
- Use available cached/permitted evidence.
- Mark stale or missing sources.
- Reduce confidence.
- Disable unsupported features.
- Never invent replacement data.

## Invariants
Every mode keeps:
- Authentication.
- Authorization.
- Security controls.
- Privacy controls.
- Provenance.
- Audit.
- Anti-fabrication.
- Commercial separation.
