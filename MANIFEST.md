# PIOS Documentation Manifest

## Purpose
This manifest is the authoritative inventory and navigation map for the PIOS documentation package. It identifies the layer, purpose, dependencies, and recommended reading order for every file.

## Package-Level Documents

| File | Purpose |
|---|---|
| `00-README.md` | Human and AI entry point. Explains PIOS, the eight-layer architecture, mandatory principles, and reading order. |
| `MANIFEST.md` | Authoritative package inventory and dependency map. |

## Layer Map

### Layer 01 Product and Strategy

**Dependencies:** Package-level documents only.

| File | Purpose |
|---|---|
| `01-Product-Vision-and-Strategy.md` | Defines PIOS vision, target users, category strategy, differentiation, success measures, and long-term direction. |
| `02-Product-Requirements-Specification.md` | Defines functional and non-functional requirements, acceptance philosophy, user/business/admin capabilities, and platform quality constraints. |

### Layer 02 Core Architecture and Infrastructure

**Dependencies:** Layer 01.

| File | Purpose |
|---|---|
| `03-System-Architecture.md` | Defines logical service boundaries, orchestration flow, event patterns, canonical identity, data ownership, and resilience rules. |
| `04-Infrastructure-and-Deployment.md` | Defines cloud runtime, environments, networking, managed services, CI/CD, IaC, secrets, backups, recovery, and deployment safety. |
| `05-Technology-Stack.md` | Defines the primary frontend, backend, data, AI, messaging, observability, testing, and language choices. |
| `06-Data-Architecture.md` | Defines core entities, identifier rules, geography, provenance, lifecycle, and data-quality dimensions. |
| `07-Knowledge-Graph.md` | Defines graph concepts, entity relationships, entity resolution, merge/split rules, and graph storage strategy. |
| `08-Data-Acquisition-and-Source-Strategy.md` | Defines source classes, source registry, lawful acquisition, source freshness, conflict handling, and acquisition-agent boundaries. |
| `09-Data-Normalization.md` | Defines normalization rules for names, categories, addresses, ratings, language, time, duplicates, missing values, and publication gates. |

### Layer 03 Intelligence and Decision Engine

**Dependencies:** Layers 01 and 02.

| File | Purpose |
|---|---|
| `10-Trust-Engine.md` | Defines trust as evidence confidence, signal families, manipulation indicators, trust states, versioning, governance, and calibration. |
| `11-Review-Intelligence.md` | Defines sentiment, aspect analysis, trend extraction, language handling, evidence tracing, temporal analysis, and safety constraints. |
| `12-Community-Intelligence-Network.md` | Defines community contribution types, contributor quality, validation states, moderation, disputes, incentives, and auditability. |
| `13-Ranking-Engine.md` | Defines ranking features, scoring structure, distance behavior, hard versus soft constraints, diversity, sponsorship separation, and change management. |
| `14-Recommendation-Engine.md` | Defines how ranked results are reduced into decision-ready recommendations with evidence-backed labels and uncertainty handling. |
| `15-Explanation-Engine.md` | Defines how structured evidence is converted into transparent recommendation reasons without unsupported claims. |
| `16-Search-and-Discovery.md` | Defines supported queries, intent extraction, hybrid retrieval, empty-result expansion, and conversational refinement. |
| `17-Place-Profile.md` | Defines canonical place profile content, source ratings, trust, freshness, claiming, community, and historical change handling. |
| `18-Feedback-and-Learning.md` | Defines feedback events, offline evaluation, experiments, versioning, and privacy-aware learning loops. |

### Layer 04 Platform Engineering and Experience

**Dependencies:** Layers 01 to 03.

| File | Purpose |
|---|---|
| `19-API-and-Service-Contracts.md` | Defines API design principles, representative endpoints, search contracts, error models, and internal contract rules. |
| `20-Security-Architecture.md` | Defines threat model, identity, authorization, input controls, AI security, secure SDLC, and incident response. |
| `21-Privacy-and-Data-Governance.md` | Defines privacy principles, location handling, data classification, governance roles, retention, Saudi compliance mapping, and cross-border controls. |
| `22-Observability-and-Audit.md` | Defines logs, metrics, traces, audit events, integrity, correlation, and alerting expectations. |
| `23-UX-UI-and-Localization.md` | Defines decision-focused UX, search-card hierarchy, Arabic/English parity, mixed-language handling, localization architecture, and map UX. |
| `24-Accessibility-and-Design-System.md` | Defines WCAG 2.2 AA target, accessible interaction requirements, design tokens, component standards, and testing. |

### Layer 05 AI Orchestration and Development Operations

**Dependencies:** Layers 01 to 04, especially architecture, security, privacy, and data governance.

| File | Purpose |
|---|---|
| `25-AI-Orchestration.md` | Defines master orchestration, specialized AI roles, separation of duties, agent context, output contract, and approval gates. |
| `26-AI-Agent-Specifications.md` | Defines responsibilities, authority, and restrictions for all specialized AI and operational roles. |
| `27-Project-Instructions.md` | Defines mandatory project principles, implementation workflow, AI rules, priority order, change discipline, and completion criteria. |
| `28-Operational-Rules.md` | Defines runtime and operational invariants for provenance, security, privacy, ranking, trust, agents, source failures, and human escalation. |
| `29-Skills-Definitions.md` | Defines intentionally invoked skills such as search, trust, entity resolution, security review, data governance, code review, and incident analysis. |
| `30-Output-Standards.md` | Defines quality and content standards for engineering, product, AI, code, documentation, and evidence claims. |
| `31-Guardrails.md` | Defines prohibited fabrication, agent security boundaries, trust/ranking integrity, privacy, approval requirements, and safe failure behavior. |
| `32-Execution-Modes.md` | Defines balanced, strict, exploratory, deep research, and degraded execution modes plus non-negotiable invariants. |

### Layer 06 Governance Operations and Delivery

**Dependencies:** Layers 01 to 05.

| File | Purpose |
|---|---|
| `33-Autonomous-Operations.md` | Defines what automation may perform autonomously, what requires approval, monitoring responsibilities, and safe change requirements. |
| `34-Testing-and-Quality.md` | Defines unit through AI evaluation layers, search/ranking/entity-resolution/security tests, and release gates. |
| `35-Monitoring-SLOs-and-Operations.md` | Defines initial SLO targets, alerting domains, severity model, incident process, and postmortem requirements. |
| `36-MVP-and-Delivery-Roadmap.md` | Defines phased delivery from foundation through expansion while preserving production-capable architecture. |
| `37-Business-and-Monetization-Model.md` | Defines consumer, business, API, and enterprise monetization while protecting trust and organic ranking integrity. |

### Layer 07 Market Growth and Expansion

**Dependencies:** Layers 01, 03, 04, and 06.

| File | Purpose |
|---|---|
| `38-Competitive-Positioning.md` | Defines PIOS positioning relative to review/reputation platforms and its differentiation around place decision intelligence. |
| `39-SEO-and-Growth-Architecture.md` | Defines local search intent, programmatic SEO constraints, technical SEO, trust-safe publishing, and growth loops. |
| `40-Internationalization-and-MENA-Strategy.md` | Defines country configuration, Arabic search, taxonomy localization, expansion gates, and regional architecture. |

### Layer 08 AI Execution and Governance Control

**Dependencies:** Layers 01 to 06, with Layer 05 as the main operational dependency.

| File | Purpose |
|---|---|
| `41-Master-Startup-Prompt.md` | Provides the master operating prompt for Manus, Claude, Codex, opencode, or similar AI environments. |
| `42-Developer-Execution-Prompt.md` | Provides the execution contract for AI-assisted software implementation, testing, migration, security, and reporting. |
| `43-Agent-Activation-Matrix.md` | Defines when each specialist agent activates, which agents support it, and which changes require approval. |
| `44-Decision-Logs-and-Governance.md` | Defines ADR structure, governance domains, change classification, high-risk controls, and decision recoverability. |

## Recommended Reading Order

1. `00-README.md`
2. `MANIFEST.md`
3. Layer 01: Product & Strategy
4. Layer 02: Core Architecture & Infrastructure
5. Layer 03: Intelligence & Decision Engine
6. Layer 04: Platform Engineering & Experience
7. Layer 05: AI Orchestration & Development Operations
8. Layer 06: Governance, Operations & Delivery
9. Layer 07: Market, Growth & Expansion
10. Layer 08: AI Execution & Governance Control

## AI Environment Loading Guidance

For Manus, Claude, Codex, opencode, or another AI development environment:
- Always load `00-README.md`, `MANIFEST.md`, `27-Project-Instructions.md`, `28-Operational-Rules.md`, `31-Guardrails.md`, and `41-Master-Startup-Prompt.md` when establishing project-wide context.
- Load only the technical/product layers relevant to the active task to reduce context noise.
- Load `42-Developer-Execution-Prompt.md` for coding tasks.
- Use `43-Agent-Activation-Matrix.md` to select specialists.
- Use `44-Decision-Logs-and-Governance.md` for architectural, high-risk, policy, ranking, trust, privacy, security, or production changes.

## Integrity Rules

- The manifest does not replace any domain specification.
- A layer name is organizational; security, privacy, provenance, and trust constraints apply across all layers.
- High-impact changes must follow governance and approval rules even when implemented through AI automation.
- No file in this package is intended as empty scaffolding or future-only documentation.
