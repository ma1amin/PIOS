# Data Normalization

## Objective
Normalization converts heterogeneous source representations into consistent PIOS structures while preserving original provenance.

## Normalization Domains

### Names
- Unicode normalization.
- Whitespace normalization.
- Arabic letter normalization only where search matching benefits and without destroying display form.
- Legal/business suffix handling.
- Transliteration aliases.
- Preserve original source spelling.

### Categories
Map provider categories to the PIOS taxonomy through versioned mapping tables. Unknown categories enter a review queue rather than being forced into an inaccurate mapping.

### Addresses
Parse into country, region, city, district, street, building, postal components where possible. Preserve original address text.

### Coordinates
Validate latitude/longitude ranges and detect obvious coordinate anomalies.

### Ratings
Never convert source ratings destructively. Store original scale and value. A normalized comparison value may be derived separately with the transformation method recorded.

### Time
Store timestamps in UTC internally. Preserve source timezone where required. Render dates/times according to user locale and place timezone.

### Language
Detect language where useful. Preserve original text. Do not translate content merely to simplify storage.

## Duplicate Detection
Candidate duplicates are generated using:
- Name similarity.
- Phone/domain matches.
- Geographic distance.
- Address similarity.
- Category compatibility.
- Provider crosswalks.

A confidence model determines automatic match eligibility. Borderline matches require review.

## Missing Data
Missing values remain null/unknown. The system must not infer factual business attributes from unrelated text unless the inference is explicitly stored as derived, confidence-scored intelligence and is safe to expose.

## Publication Gate
Normalized data is eligible for publication only after:
- Schema validation.
- Provenance attachment.
- Entity-resolution decision.
- Required policy checks.
- Quality status assignment.
