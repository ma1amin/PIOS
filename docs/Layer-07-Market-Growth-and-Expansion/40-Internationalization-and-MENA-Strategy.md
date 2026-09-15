# Internationalization and MENA Strategy

## Initial Market
Saudi Arabia is the initial market. Country expansion is a governed capability, not a simple translation exercise.

## Country Configuration
Each country module should define:
- Administrative geography.
- Address conventions.
- Currency.
- phone formats.
- locale.
- language variants.
- category terminology.
- source availability.
- regulatory constraints.
- privacy requirements.
- business identifiers where applicable.
- map/geocoding strategy.

## Arabic Search
Support:
- Arabic script normalization for matching.
- spelling variants.
- transliteration.
- English brand/service terms embedded in Arabic.
- regional vocabulary.
- Arabic/English synonyms.

Preserve original display names even when normalized aliases are used for retrieval.

## Taxonomy
Maintain a global conceptual taxonomy with localized labels and country-specific extensions. Do not fork the entire category system for each country.

## Expansion Gate
Before entering a new country assess:
- Source licensing.
- data coverage.
- entity-resolution quality.
- local privacy/legal requirements.
- hosting/transfer constraints.
- taxonomy gaps.
- language quality.
- commercial demand.
- operational support.

## Regional Architecture
Core services remain common. Country differences should be expressed through configuration, localized taxonomy, policy modules, source adapters, and regional deployment controls where required.
