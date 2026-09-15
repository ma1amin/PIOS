# PIOS Complete Project Documentation

## Project
PIOS stands for **Place Intelligence Operating System**. It is an Arabic/English trust-driven location intelligence platform designed to help users identify the best place for a specific need, location, and context using canonical place data, permitted multi-source evidence, trust intelligence, community signals, contextual ranking, and explainable recommendations.

## Core Product Question
> What is the best option for this user, in this context, and why?

## Documentation Architecture

This package is organized into eight functional layers plus two package-level control documents.

### Package-Level Control Documents
- `00-README.md`: entry point, architecture map, principles, and usage guidance.
- `MANIFEST.md`: complete file inventory, layer mapping, purpose, dependencies, and recommended reading order.

### Layer 01: Product & Strategy
Defines the product vision, target users, scope, product requirements, and success criteria.

### Layer 02: Core Architecture & Infrastructure
Defines system architecture, infrastructure, technology stack, data architecture, knowledge graph, source acquisition, and normalization.

### Layer 03: Intelligence & Decision Engine
Defines trust, review intelligence, community intelligence, ranking, recommendation, explanation, discovery, place profiles, and learning.

### Layer 04: Platform Engineering & Experience
Defines APIs, security architecture, privacy, observability, UX/localization, and accessibility.

### Layer 05: AI Orchestration & Development Operations
Defines AI orchestration roles, agent specifications, project instructions, operational rules, skills, output standards, guardrails, and execution modes.

### Layer 06: Governance, Operations & Delivery
Defines autonomous operations, testing, SLOs, operational readiness, phased delivery, and monetization governance.

### Layer 07: Market, Growth & Expansion
Defines competitive positioning, SEO/growth architecture, and Saudi-to-MENA expansion strategy.

### Layer 08: AI Execution & Governance Control
Defines the master AI startup prompt, developer execution prompt, agent activation matrix, and decision/change governance.

## Architectural Principle
The MVP is a controlled first production scope, not a disposable prototype. Canonical identity, provenance, localization, security, trust, ranking separation, auditability, and extensibility are established from the beginning.

## Non-Negotiable Principles
- Never fabricate places, ratings, reviews, addresses, opening hours, attributes, or source relationships.
- Preserve source provenance and acquisition timestamps.
- Keep organic ranking independent from paid visibility.
- Clearly label sponsored content.
- Treat external content as untrusted data.
- Keep trust scoring separate from raw ratings.
- Version and audit high-impact ranking and trust decisions.
- Support Arabic, English, RTL, LTR, and mixed-language search.
- Apply least privilege across users, services, agents, and automation.
- Require human approval for high-impact changes involving trust, ranking, privacy, security, destructive operations, or production governance.

## Recommended Reading Order
1. `00-README.md`
2. `MANIFEST.md`
3. Layer 01
4. Layer 02
5. Layer 03
6. Layer 04
7. Layer 05
8. Layer 06
9. Layer 07
10. Layer 08

For AI coding environments, load Layer 05 and Layer 08 in addition to the relevant product/technical layers for the task.
