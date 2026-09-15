# Place Knowledge Graph

## Purpose
The knowledge graph represents relationships that are difficult to express through flat place records alone. It supports entity resolution, contextual discovery, service relationships, category reasoning, similarity, and explainable evidence paths.

## Node Types
- Place
- Location
- Category
- Service
- Organization
- Attribute
- SourceRecord
- TrustAssessment
- CommunityTopic where justified

## Core Relationships
- `LOCATED_IN`
- `PART_OF`
- `INSTANCE_OF`
- `OFFERS`
- `BELONGS_TO`
- `HAS_ATTRIBUTE`
- `HAS_SOURCE_RECORD`
- `HAS_TRUST_ASSESSMENT`
- `RELATED_TO`
- `SIMILAR_TO` when derived and versioned

## Entity Resolution
Resolution uses multiple signals:
- Exact provider identifiers.
- Normalized name.
- Geographic proximity.
- Phone number.
- Website/domain.
- Address similarity.
- Organization relationship.
- Category compatibility.
- Business registration identifiers when lawfully available.
- Human-reviewed mappings.

No single weak signal should auto-merge records.

## Confidence States
- Confirmed
- High-confidence match
- Probable match requiring review
- Unresolved
- Conflict

Low-confidence candidates remain separate until stronger evidence or human review is available.

## Merge Requirements
A merge must:
- Select or create a canonical `place_id`.
- Preserve all source identifiers.
- Preserve provenance.
- Record merge reason and algorithm/version.
- Record actor or automated process.
- Support reversal.

## Split Requirements
When two real places were incorrectly merged, the system must support a governed split without losing historical evidence.

## Graph Storage Strategy
Do not introduce a graph database solely for architectural appearance. Begin with relational edges if they satisfy query requirements. Adopt a dedicated graph engine after benchmarked use cases demonstrate that traversal complexity, performance, or graph algorithms justify the operational cost.
