# Explanation Engine

## Objective
Every important recommendation should be understandable. The explanation layer converts structured evidence into concise natural language without inventing reasons.

## Explanation Components
When applicable:
- Why the place matches the query.
- Which requirements it satisfies.
- Geographic context.
- Evidence/trust state.
- Relevant strengths.
- Material limitations.
- Comparison context.
- Freshness caveat.

## Evidence Contract
The engine receives structured facts from trusted services. It must not independently search unapproved sources or manufacture support.

Each explanation claim should map to:
- Place field.
- Source evidence.
- Ranking contribution.
- Trust signal.
- Review insight.
- Community signal.

## Depth Levels
### Compact
One short reason on a result card.

### Standard
A few evidence-backed factors on the place profile or recommendation panel.

### Detailed
A transparent breakdown for comparisons or users requesting more detail.

## Negative Evidence
Relevant limitations can be disclosed, for example:
- Longer distance.
- Limited recent evidence.
- Conflicting opening hours.
- Lower confidence in a specific attribute.

Avoid defamatory or accusatory language when anomaly detection is probabilistic.

## LLM Use
An LLM may verbalize structured explanation data. The structured evidence remains authoritative. Generated text should be validated against allowed facts before display.
