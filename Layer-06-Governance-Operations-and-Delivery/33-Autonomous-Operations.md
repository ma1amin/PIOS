# Autonomous Operations

## Allowed Autonomous Activities
Subject to scoped permissions, automation may:
- Refresh approved source data.
- Validate schemas.
- Normalize records.
- Generate duplicate candidates.
- Rebuild search projections.
- Recompute approved derived insights.
- Detect anomalies.
- Run tests.
- Generate pull requests.
- Generate operational reports.
- Recommend configuration changes.

## Approval Required
Automation may not independently perform:
- High-impact production deployments.
- Destructive schema changes.
- Bulk irreversible deletion.
- Trust model policy changes.
- Ranking policy changes.
- Privacy/retention changes.
- Authentication/authorization changes.
- New sensitive data collection.
- Permanent source-policy overrides.

## Monitoring
Autonomous operations monitor:
- Source degradation.
- Ingestion errors.
- Search index lag.
- Entity-resolution conflicts.
- Trust distribution drift.
- Ranking instability.
- Review/community anomalies.
- API latency.
- Error rates.
- Queue backlog.
- Infrastructure health.

## Change Safety
Every autonomous production mutation must have:
- Defined scope.
- Authorization.
- Idempotency where relevant.
- Audit event.
- Verification.
- Rollback or compensating action.

## Agent Generated Pull Requests
A generated PR must state:
- Why the change is needed.
- Files affected.
- Tests added/run.
- Security impact.
- Data impact.
- Migration impact.
- Rollback.
- Any unresolved uncertainty.

Human review remains required according to repository policy.
