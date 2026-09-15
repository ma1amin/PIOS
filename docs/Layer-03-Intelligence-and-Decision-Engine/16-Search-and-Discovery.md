# Search and Discovery

## Supported Query Types
- Place name.
- Category.
- Service.
- Natural-language need.
- Geographic request.
- Near-me request.
- Attribute combination.
- Comparison.
- Conversational refinement.

## Intent Extraction
The query understanding layer identifies:
- Category.
- Service.
- Country/city/district.
- Radius.
- User location when permitted.
- Required attributes.
- Preferred attributes.
- Price/value intent.
- Quality intent.
- Distance intent.
- Temporal constraints.
- Language.

## Pipeline
1. Normalize query.
2. Detect language and mixed-language terms.
3. Extract intent and constraints.
4. Resolve location.
5. Resolve taxonomy.
6. Retrieve candidates.
7. Apply hard eligibility filters.
8. Enrich required features.
9. Retrieve trust.
10. Rank.
11. Select recommendations.
12. Generate evidence-backed explanations.
13. Render localized response.

## Search Retrieval
Use a hybrid strategy where justified:
- Lexical search.
- Typo tolerance.
- Arabic normalization.
- Transliteration aliases.
- Synonyms.
- Category mappings.
- Semantic retrieval.
- Geospatial filtering.

Semantic search must not replace deterministic filters for explicit requirements.

## Empty Results
Controlled expansion:
1. Exact requested area and constraints.
2. Nearby district or wider radius.
3. City-level expansion.
4. Related category/service alternatives.

The UI must tell the user when constraints were broadened.

## Conversational Refinement
Follow-up queries retain prior constraints unless the user changes them. Example:
“Best dentist in north Riyadh”
then
“only those open after 8”
should preserve dentist and north Riyadh while adding the new temporal constraint.
