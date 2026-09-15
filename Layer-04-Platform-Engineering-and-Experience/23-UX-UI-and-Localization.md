# UX, UI and Localization

## UX Objective
PIOS should reduce the effort required to make a local decision. The user should quickly understand:
- What was found.
- Why it matches.
- How far it is.
- How strong the evidence is.
- What important limitations exist.
- What action to take next.

## Search Result Card
Recommended hierarchy:
1. Place name.
2. Category/service.
3. Trust/evidence state.
4. Source rating summaries where permitted.
5. Distance/location.
6. Key matching attributes.
7. Short reason.
8. Primary actions.

## Avoid
- Dense dashboards for consumer search.
- One unexplained composite number.
- Hidden sponsored placement.
- Excessive badges.
- False precision.
- Long AI-generated paragraphs where a few facts suffice.

## Arabic
Arabic is first-class:
- Full RTL layout.
- Arabic typography.
- Correct bidirectional behavior for URLs, phone numbers, English brand names, and numbers.
- Arabic search normalization.
- Arabic synonyms and category aliases.
- Regional terminology.
- English numerals 1, 2, 3 when consistent with product design.
- Locale-aware dates and units.

## English
English receives equivalent functional coverage, not a secondary translation layer.

## Mixed Language
Queries such as “افضل dental clinic في الرياض” must be handled naturally through mixed-language tokenization, taxonomy aliases, and semantic retrieval.

## Localization Architecture
- No hardcoded user-visible strings.
- Translation keys.
- ICU-style pluralization where required.
- Locale-specific formatting.
- RTL-aware components.
- Localized metadata and SEO.
- Translation review workflow.

## Map UX
Map and list should cooperate. The map is a spatial aid, not the only discovery interface. Keyboard and screen-reader users must still be able to complete core search tasks.
