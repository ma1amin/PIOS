# Testing and Quality

## Test Layers
- Unit.
- Integration.
- Contract.
- End-to-end.
- Security.
- Performance.
- Accessibility.
- Localization.
- AI evaluation.
- Data-quality tests.

## Entity Resolution Tests
Measure:
- Precision.
- Recall.
- False merges.
- Missed merges.
- Category-specific behavior.
- Arabic/English name variants.
- Geographic edge cases.

False merges are especially damaging because they combine evidence from different real places.

## Search Tests
Cover:
- Arabic.
- English.
- Mixed language.
- Misspellings.
- Transliteration.
- Category aliases.
- Geographic constraints.
- Empty results.
- conversational refinement.

## Ranking Tests
Cover:
- Hard constraint satisfaction.
- Distance behavior.
- Trust contribution.
- Diversity.
- Sponsored separation.
- Regression queries.
- Manipulation scenarios.

## Security Tests
Include:
- BOLA/IDOR.
- Injection.
- SSRF.
- authentication.
- privilege escalation.
- rate-limit abuse.
- secret leakage.
- prompt injection.
- malicious retrieved content.
- agent tool misuse.

## AI Evaluation
Maintain versioned benchmark sets for:
- Factual grounding.
- Relevance.
- Explanation faithfulness.
- Arabic/English quality.
- Refusal/fallback behavior.
- Hallucination rate.
- structured output validity.

## Release Gate
Block release for:
- Unresolved critical security issue.
- Failed core regression.
- Data corruption risk.
- Broken authorization.
- Unacceptable trust/ranking regression.
- Failed migration safety checks.

## Test Evidence
Reports distinguish tests designed from tests actually executed. Never state a test passed without execution evidence.
