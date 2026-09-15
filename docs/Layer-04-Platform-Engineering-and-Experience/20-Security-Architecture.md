# Security Architecture

## Security Objectives
Protect confidentiality, integrity, availability, user trust, place-data integrity, and decision-system integrity.

## Threat Model
Relevant threats include:
- Account takeover.
- Credential stuffing.
- API abuse.
- Automated scraping abuse.
- Injection.
- SSRF.
- Broken object-level authorization.
- Privilege escalation.
- Supply-chain compromise.
- Malicious business claims.
- Review manipulation.
- Community manipulation.
- Data poisoning.
- Prompt injection.
- Agent tool abuse.
- Unauthorized data extraction.
- Secrets leakage.
- Search/ranking manipulation.

## Identity
Use OIDC/OAuth standards. Prefer MFA for privileged accounts. Session/token design should use short lifetimes and secure refresh mechanisms.

## Authorization
Combine RBAC with resource-level checks. Roles may include:
- User.
- Contributor.
- Business member.
- Business administrator.
- Moderator.
- Data reviewer.
- Operations.
- Security administrator.
- Platform administrator.

Administrative role names alone are not sufficient. Every sensitive operation needs explicit authorization logic.

## Input Security
- Schema validation.
- Parameterized queries.
- Output encoding.
- File-type validation.
- Size limits.
- URL allowlists for server-side retrieval.
- Rate limits.
- Abuse detection.

## AI Security
External retrieved content is untrusted. It cannot override system policy. AI tools are allowlisted and scoped. Agents receive minimum required data and permissions.

Protect against:
- Prompt injection.
- Tool-call injection.
- Data exfiltration.
- Poisoned retrieved content.
- Model-generated SQL or commands executed without validation.

## SDLC
Required controls:
- Threat modeling.
- SAST.
- Dependency scanning.
- Secret scanning.
- Container scanning.
- DAST/API testing.
- Code review.
- Penetration testing before material public releases.
- AI red-team testing for agentic features.

## Incident Response
Maintain:
- Detection.
- Triage.
- Containment.
- Eradication.
- Recovery.
- Communication.
- Evidence preservation.
- Post-incident review.

Security-critical logs should feed a monitoring/SIEM process as operational maturity grows.
