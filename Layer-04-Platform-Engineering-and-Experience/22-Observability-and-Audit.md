# Observability and Audit

## Observability Pillars
- Structured logs.
- Metrics.
- Distributed traces.
- Events.

## Correlation
A user search should be traceable through:
query → retrieval → enrichment → trust → ranking → recommendation → explanation → response.

Correlation identifiers must not contain sensitive data.

## Logging
Logs should include:
- Timestamp.
- Service.
- Environment.
- Severity.
- Correlation ID.
- Safe actor/resource identifiers.
- Event/action.
- Outcome.
- Latency.
- Error code.

Never log secrets, tokens, full sensitive payloads, or precise user coordinates unless explicitly justified and protected.

## Metrics
Core metrics:
- API latency.
- Error rate.
- Search latency.
- Empty-result rate.
- Candidate count.
- Search success.
- Source freshness.
- Ingestion failures.
- Entity-resolution queue size.
- Trust coverage.
- Ranking distribution.
- Index lag.
- Queue depth.
- Cache performance.

## Audit Events
Audit:
- Authentication/security changes.
- Privileged authorization actions.
- Business claims.
- Place merges/splits.
- Source configuration.
- Trust model/config changes.
- Ranking model/config changes.
- Administrative overrides.
- Data deletion.
- Privacy requests.
- Security incidents.

## Audit Integrity
Audit records should be append-oriented and protected from ordinary application modification. Administrative access to audit data is itself audited.

## Alerting
Alerts must be actionable and tied to runbooks. Avoid alerting on every anomaly without severity or operational meaning.
