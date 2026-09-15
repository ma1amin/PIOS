# Recommendation Engine

## Purpose
The recommendation engine transforms ranked candidates into a concise decision set. Ranking answers “what order?” Recommendation answers “which options should the user seriously consider?”

## Default Output
Return approximately 3 to 5 strong options when enough evidence exists. Avoid overwhelming the user with long undifferentiated lists.

## Recommendation Labels
Examples:
- Best overall match.
- Best nearby option.
- Best value evidence.
- Best for a specified requirement.
- Strong alternative.
- Emerging option with limited evidence.

Labels must be supported by available features and evidence.

## Decision Logic
The engine considers:
- Rank score.
- Confidence.
- Candidate diversity.
- User hard constraints.
- Evidence sufficiency.
- Trust state.
- Recommendation redundancy.
- Availability/freshness where relevant.

## Weak Evidence
When evidence is sparse:
- State uncertainty.
- Avoid strong superlatives.
- Offer alternatives.
- Explain what evidence is missing.
- Permit the user to broaden geography or constraints.

## Personalization
Personalization should use explicit or privacy-respecting preference signals. It must not override hard user constraints or produce unexplained sensitive inferences.

## Sponsored Content
Sponsored results are a separate presentation surface. They may be relevant to the query, but must be visibly labeled and cannot be described as “best” based solely on payment.
