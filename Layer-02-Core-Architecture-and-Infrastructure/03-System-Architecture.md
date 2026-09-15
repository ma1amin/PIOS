# System Architecture

## Architecture Style
PIOS uses a modular, API-first, event-aware architecture. Early implementation may deploy several modules together to control operational complexity, but logical boundaries must remain explicit so that high-load domains can be separated later.

## Logical Flow

Client Applications  
→ API Gateway / Edge  
→ Identity and Authorization  
→ Query Orchestrator  
→ Context Understanding  
→ Candidate Discovery  
→ Search Retrieval  
→ Data Enrichment  
→ Trust Evaluation  
→ Ranking  
→ Recommendation  
→ Explanation  
→ Response Composition

Supporting platform:
- Canonical Place Service
- Taxonomy Service
- Source Registry
- Ingestion Workers
- Entity Resolution
- Review Intelligence
- Community Service
- Business Claim Service
- Moderation
- Audit Service
- Notification Service
- Analytics and Evaluation

## Service Boundaries

### Query Orchestrator
Coordinates a search request. It does not own canonical place records or modify trust models.

### Place Service
Owns canonical place identity and authoritative PIOS place fields.

### Source Service
Owns source definitions, external identifiers, acquisition metadata, and provenance.

### Search Service
Indexes searchable place projections and retrieves candidates.

### Trust Service
Computes and serves versioned trust assessments from defined signals.

### Ranking Service
Scores candidates using configured ranking models. It consumes trust as one feature and cannot rewrite trust.

### Recommendation Service
Chooses a compact decision-ready set from ranked candidates.

### Explanation Service
Produces evidence-grounded reasons from structured ranking and evidence metadata.

### Community Service
Owns contributions, validations, reports, reputation signals, and moderation state.

### Business Service
Owns claims, verification, business-managed fields, and business analytics permissions.

## Synchronous vs Asynchronous Processing

### Synchronous
Use for latency-sensitive user operations:
- Authentication.
- Search retrieval.
- Place profile retrieval.
- Ranking.
- Recommendation.
- User-visible explanation.
- Basic account operations.

### Asynchronous
Use for:
- Source ingestion.
- Data normalization.
- Entity-resolution jobs.
- Review analysis.
- Trust recalculation.
- Search indexing.
- anomaly detection.
- Notifications.
- analytics events.
- audit export.
- model evaluation.

## Event Design
Events should contain:
- Event ID.
- Event type.
- Schema version.
- Timestamp.
- Producer.
- Correlation ID.
- Entity identifier.
- Minimal payload or secure reference.
- Idempotency metadata where required.

Consumers must tolerate duplicate delivery when the messaging layer provides at-least-once semantics.

## Data Ownership
Each domain has a clear owner. Services should not directly mutate another domain’s private tables. Cross-domain access uses APIs, events, or approved read models.

## Canonical Identity
PIOS owns `place_id`. External providers retain their own source identifiers. A place may have many `source_place` records. Provider IDs must never become the platform’s primary identity.

## Resilience
External dependencies use:
- Timeouts.
- Retry policies with backoff.
- Circuit breakers where appropriate.
- Rate-limit awareness.
- Cached permitted data.
- Failure isolation.
- Explicit degraded-state metadata.

## Architecture Invariants
- Search cannot mutate source truth.
- Ranking cannot silently modify trust.
- Business users cannot edit independent evidence.
- Generic AI agents cannot receive unrestricted database credentials.
- Source provenance cannot be discarded during normalization.
- High-impact model/configuration changes are versioned and auditable.
