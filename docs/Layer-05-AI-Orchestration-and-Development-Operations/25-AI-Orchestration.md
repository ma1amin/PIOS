# AI Orchestration

## Objective
PIOS uses specialized AI roles as bounded collaborators. Agents support analysis, implementation, evaluation, and operations. They do not become an uncontrolled authority over production data or policy.

## Master Orchestrator
The Master Orchestrator:
1. Receives the objective.
2. Classifies the task.
3. Identifies affected domains.
4. Activates required specialist agents.
5. Defines bounded outputs.
6. Reconciles conflicts.
7. Applies project guardrails.
8. Requests approval for high-impact changes.
9. Records material decisions.
10. Produces a final implementation or decision package.

## Core Roles
- Product Architect.
- AI Systems Designer.
- Security & Trust Guardian.
- Ecosystem Strategist.
- Developer Lead.
- UX & Localization Specialist.

## Additional Required Roles
- Data Intelligence Lead.
- Evaluation Lead.
- DevOps/SRE Lead.
- Governance Lead.

## Separation of Duties
Agents provide evidence and recommendations within scope. Examples:
- Data Intelligence proposes entity-resolution logic.
- Evaluation validates its accuracy.
- Security reviews manipulation risk.
- Developer implements approved contracts.
- Governance reviews high-impact policy/data changes.

No agent silently approves its own high-impact change.

## Agent Context
Each agent receives:
- Task objective.
- Relevant architecture excerpts.
- Allowed tools.
- Required data.
- Constraints.
- Expected output contract.

Avoid providing unrelated secrets, production data, or broad permissions.

## Standard Agent Output
Every specialist response should contain:
- Objective.
- Findings.
- Evidence.
- Proposed action.
- Risks.
- Confidence.
- Dependencies.
- Validation method.

## Human Approval
Required for:
- Production deployment with high impact.
- Destructive schema/data operations.
- Trust model changes.
- Ranking policy changes.
- Authentication/authorization changes.
- Privacy policy/retention changes.
- New sensitive data collection.
- High-risk source integrations.
