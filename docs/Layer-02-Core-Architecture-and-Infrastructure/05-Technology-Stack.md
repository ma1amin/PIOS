# Technology Stack

## Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS
- Accessible component primitives
- TanStack Query or equivalent server-state library
- MapLibre GL or provider-neutral mapping abstraction
- i18n library supporting server rendering and RTL
- Schema validation shared with API contracts where practical

## Backend
- NestJS
- TypeScript
- REST APIs as the default external contract
- OpenAPI specifications
- Background workers
- WebSockets only for features that truly require real-time push

NestJS provides modular boundaries, dependency injection, validation integration, testing support, and a structured TypeScript backend suitable for a multi-domain platform.

## Data
### PostgreSQL + PostGIS
Primary system of record for canonical places, accounts, claims, taxonomy, attributes, governance records, and geographic operations.

### Redis
Caching, rate-limit counters, short-lived state, distributed coordination where required.

### OpenSearch
Text search, faceting, relevance retrieval, autocomplete, and searchable projections.

### Object Storage
Raw permitted source payloads where retention is allowed, exports, generated reports, and media metadata.

### Graph
Start with PostgreSQL relationship tables where graph depth remains manageable. Introduce Neo4j or another graph database when graph traversal requirements demonstrate measurable operational value.

## AI/ML
Use a provider-agnostic AI gateway. Models may include:
- Hosted LLMs.
- Self-hosted models.
- Embedding models.
- Rerankers.
- Classification models.
- Arabic/English NLP models.

Model providers are configuration, not domain architecture.

## Messaging
Use Kafka, Redpanda, or a managed event equivalent for high-volume durable event streams. An initial managed queue can be used for simpler workloads if event schemas and idempotency contracts are maintained.

## Languages
- TypeScript: primary product engineering language.
- Python: ML, NLP, experimentation, offline evaluation, and data-science workloads.

## Authentication
Use standards-based OAuth 2.0 / OpenID Connect. Prefer a mature managed or well-supported identity provider.

## Testing
- Jest/Vitest for unit tests.
- Supertest or equivalent for API integration.
- Playwright for browser E2E.
- Contract testing where services are independently deployed.
- Python pytest for ML/data workloads.

## Observability
- OpenTelemetry.
- Centralized structured logs.
- Metrics backend.
- Distributed tracing.
- Error monitoring.
- Security monitoring/SIEM integration as the platform matures.

## Selection Rule
A technology is adopted because it satisfies a documented requirement, not because it is fashionable. New infrastructure components require an architecture decision record describing operational cost, alternatives, failure modes, and exit strategy.
