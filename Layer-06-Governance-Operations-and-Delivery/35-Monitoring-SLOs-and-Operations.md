# Monitoring, SLOs and Operations

## Initial Engineering Targets
These are starting targets to validate operationally, not claims of achieved performance:
- Core API monthly availability target: 99.9%.
- Search API p95 target: <= 2.5 seconds under defined production load.
- Place profile p95 target: <= 1.5 seconds under defined production load.
- Critical ingestion pipeline success target: >= 99%.
- Critical audit-event delivery target: >= 99.9%.

Targets should be revised from real workload and business requirements.

## Monitoring Domains
- Edge/API.
- Application.
- Database.
- Search.
- Cache.
- Queue/event platform.
- Source integrations.
- AI providers.
- Trust/ranking services.
- Security.
- Cost.

## Alert Conditions
Examples:
- Sustained 5xx increase.
- Search latency breach.
- Database saturation.
- Search-index lag.
- Queue backlog.
- Source outage.
- Abnormal trust distribution change.
- Ranking distribution anomaly.
- Authentication failures.
- WAF/security events.
- Backup failure.
- Audit pipeline failure.

## Incident Severity
### SEV1
Major outage, confirmed serious security compromise, or widespread integrity failure.

### SEV2
Material degradation affecting a significant feature or user population.

### SEV3
Limited impact with workaround.

### SEV4
Minor operational issue.

## Incident Process
Detect → acknowledge → assign commander → contain → communicate → recover → verify → preserve evidence → postmortem.

## Postmortem
Include:
- Timeline.
- User/business impact.
- Root cause.
- Contributing factors.
- Detection gap.
- Response quality.
- Corrective actions.
- Owners and dates.
- Prevention/monitoring changes.

Focus on system improvement and accountable remediation.
