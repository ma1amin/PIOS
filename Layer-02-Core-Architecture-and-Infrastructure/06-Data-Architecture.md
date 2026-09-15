# Data Architecture

## Core Entities

### User
Identity, preferences, locale, privacy settings, contribution state.

### Organization
Business or institutional account entity.

### Place
Canonical PIOS identity. Stable `place_id` independent from any provider.

### PlaceLocation
Coordinates, address components, administrative hierarchy, geospatial representation.

### Category
Hierarchical taxonomy node.

### AttributeDefinition
Schema describing a reusable or category-specific attribute.

### PlaceAttribute
Value attached to a place with source/provenance and confidence.

### Source
Definition of an external, partner, business, public, or community data source.

### SourcePlace
Provider-specific representation of a canonical place.

### RatingSnapshot
Time-stamped rating/volume record from a source when permitted.

### ReviewReference
Reference and metadata for a review or feedback artifact where lawful and permitted.

### ReviewInsight
Derived sentiment, topic, aspect, or trend output linked to evidence.

### TrustAssessment
Versioned trust state and contributing signal metadata.

### CommunitySignal
Structured community validation, correction, report, or experience signal.

### SearchQuery
Privacy-aware search telemetry used for evaluation and improvement.

### Recommendation
Versioned result/reason record where retention is justified.

### FeedbackEvent
User interaction or explicit feedback.

### AuditEvent
Security/governance record for material operations.

## Identifier Rules
- PIOS IDs are generated internally.
- Provider IDs remain namespaced.
- IDs exposed publicly should not reveal sequential internal database counts.
- Merge operations preserve aliases and history.
- Split operations are supported when an incorrect merge is discovered.

## Geographic Model
Store:
- Latitude/longitude.
- PostGIS point/geography.
- Country.
- Administrative region.
- City.
- District/neighborhood.
- Postal information where available.
- Address lines.
- Source precision/confidence.

Distance calculations should use appropriate geodesic operations rather than naive Cartesian math.

## Provenance
Every externally derived field should be capable of carrying:
- Source.
- Source record.
- Acquisition timestamp.
- Transformation version.
- Confidence.
- Validation status.
- Original/raw reference where permitted.
- Last verified timestamp.

## Data Lifecycle
1. Acquire.
2. Store permitted raw/reference data.
3. Validate schema.
4. Normalize.
5. Resolve entity.
6. Enrich.
7. Compute derived intelligence.
8. Publish read model.
9. Monitor freshness.
10. Refresh or expire.
11. Archive/delete according to policy.

## Data Quality Dimensions
- Completeness.
- Accuracy.
- Consistency.
- Freshness.
- Uniqueness.
- Validity.
- Provenance coverage.

Quality metrics should be available per source and category to avoid hiding weak data behind aggregate platform metrics.
