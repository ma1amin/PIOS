# Infrastructure and Deployment

## Cloud Strategy
Use a major cloud platform such as AWS or Azure with managed services wherever they reduce operational risk. The architecture must avoid unnecessary proprietary coupling in core domain logic.

## Runtime
- Linux containers.
- Kubernetes for production orchestration when scale/operations justify it.
- Managed container service may be used initially if service contracts remain portable.
- Container images are immutable.
- Images are stored in a private registry.
- Production containers run as non-root where technically feasible.

## Environments
Maintain isolated:
- Local
- Development
- Staging
- Production

Production credentials, databases, queues, buckets, and secrets must not be shared with development.

## Network Architecture
Typical production topology:
- Public CDN/edge.
- WAF.
- Load balancer/API gateway.
- Private application network.
- Private data network.
- Managed database without public exposure.
- Controlled outbound egress for source integrations.
- Bastionless administrative access where cloud-native secure access is available.

## Core Managed Components
- PostgreSQL with PostGIS.
- Redis.
- OpenSearch or equivalent.
- Object storage.
- Message broker or managed queue/event service.
- Secrets manager.
- Key management.
- Centralized logging.
- Metrics and tracing.
- Container registry.
- CI/CD runners.
- Backup service.

## Infrastructure as Code
Use Terraform or an equivalent declarative system. Infrastructure changes shall be peer reviewed and applied through controlled pipelines. Production drift should be detected.

## CI/CD Pipeline
Minimum pipeline:
1. Dependency installation from locked manifests.
2. Linting.
3. Type checks.
4. Unit tests.
5. Security and secret scanning.
6. Dependency vulnerability scanning.
7. Build.
8. Container scanning.
9. Integration/contract tests.
10. Staging deployment.
11. Smoke/E2E tests.
12. Approval for high-impact production releases.
13. Production deployment.
14. Post-deployment health checks.
15. Automated or operator-triggered rollback.

## Secrets
Secrets shall:
- Never be committed to repositories.
- Be stored in a managed secret store.
- Be scoped to service identity.
- Be rotated.
- Avoid long-lived static credentials where workload identity is available.
- Be redacted from logs.

## Backup and Recovery
Back up:
- Canonical relational data.
- Configuration.
- audit records.
- object storage according to lifecycle policy.
- search indexes only when restoration is more efficient than rebuilding.

Perform restore tests. A backup without verified restoration is not considered a complete recovery control.

## Deployment Safety
Use rolling, blue/green, or canary strategies according to risk. Database migrations require forward/backward compatibility during rollout where multiple application versions may coexist.

## Cost Controls
Tag resources by environment and service. Establish budgets, anomaly alerts, retention limits, right-sizing reviews, and separate scaling policies for search, workers, and AI workloads.
