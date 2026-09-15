# 🌍 PIOS - Place Intelligence Operating System

<div align="center">

![🚀](https://animated-fluent-emoji.vercel.app/animated/rocket-emoji.gif)
![🎯](https://animated-fluent-emoji.vercel.app/animated/target-emoji.gif)
![🤖](https://animated-fluent-emoji.vercel.app/animated/robot-emoji.gif)
![🔒](https://animated-fluent-emoji.vercel.app/animated/locked-emoji.gif)
![🌐](https://animated-fluent-emoji.vercel.app/animated/globe-meridians-emoji.gif)

**Arabic/English Trust-Driven Location Intelligence Platform**

[![License](https://img.shields.io/badge/license-Proprietary-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-Development-yellow.svg)](https://github.com/ma1amin/PIOS)
[![Architecture](https://img.shields.io/badge/architecture-Microservices-green.svg)](https://github.com/ma1amin/PIOS)

</div>

---

## 🎯 Core Mission

**PIOS** stands for **Place Intelligence Operating System** - a revolutionary location intelligence platform designed to help users identify the best place for their specific needs, location, and context.

> **"What is the best option for this user, in this context, and why?"**

Our platform combines canonical place data, permitted multi-source evidence, trust intelligence, community signals, contextual ranking, and explainable recommendations to deliver trustworthy place decisions.

---

## 🚀 Vision & Strategy

### 🌟 Vision
PIOS will become the trusted decision layer for physical places. Users can describe their needs naturally - like *"best pediatric dentist near north Riyadh with good appointment reliability"* - and receive evidence-backed options with clear explanations.

### 🎯 Target Users
- **👥 Consumers** - People seeking quality places based on evidence, distance, reliability, and suitability
- **🏢 Businesses** - Verified businesses needing accurate profiles and customer intelligence  
- **🏛️ Enterprises** - Organizations requiring location intelligence and trusted place APIs
- **👨‍💻 Developers** - Applications needing structured place intelligence through controlled APIs

### 🌍 Initial Market
Saudi Arabia is our launch market, with Riyadh and Jeddah as initial cities due to high place density and diverse categories.

### 💡 Differentiation
1. **Context-aware** local discovery
2. **Multi-source evidence** with provenance tracking
3. **Trust intelligence** independent from star ratings
4. **Community intelligence** structured around verifiable attributes
5. **Explainable ranking** with transparent reasoning
6. **Arabic-first-class** language support
7. **Canonical place identity** across all sources
8. **Organic-commercial separation** protecting decision integrity

---

## 🏗️ Architecture

### System Design
PIOS uses a **modular, API-first, event-aware architecture** designed for scalability and maintainability.

```
Client Applications
    ↓
API Gateway / Edge
    ↓
Identity & Authorization
    ↓
Query Orchestrator
    ↓
Context Understanding → Candidate Discovery → Search Retrieval
    ↓
Data Enrichment → Trust Evaluation → Ranking
    ↓
Recommendation → Explanation → Response Composition
```

### Core Services
- **🔍 Query Orchestrator** - Coordinates search requests
- **📍 Place Service** - Owns canonical place identity
- **📊 Source Service** - Manages source definitions and provenance
- **🔎 Search Service** - Indexes and retrieves candidates
- **🛡️ Trust Service** - Computes trust assessments
- **📈 Ranking Service** - Scores candidates using ranking models
- **💡 Recommendation Service** - Produces decision-ready sets
- **📝 Explanation Service** - Generates evidence-grounded reasons
- **👥 Community Service** - Manages contributions and validations
- **🏢 Business Service** - Handles claims and verification

### Architecture Principles
- **🎯 Canonical Identity** - PIOS owns `place_id`, providers keep their identifiers
- **🔄 Event-Driven** - Asynchronous processing for heavy operations
- **🛡️ Resilience** - Timeouts, retries, circuit breakers, and failure isolation
- **📊 Data Ownership** - Clear domain boundaries with API-based access
- **🔒 Security First** - Least privilege across all layers

---

## 💻 Technology Stack

### Frontend
- **⚛️ Next.js** - React framework with server-side rendering
- **📘 TypeScript** - Type-safe development
- **🎨 Tailwind CSS** - Utility-first styling
- **🗺️ MapLibre GL** - Provider-neutral mapping
- **🌐 i18n Library** - Arabic/English with RTL support
- **📦 TanStack Query** - Server state management

### Backend
- **🏗️ NestJS** - Modular TypeScript backend framework
- **📘 TypeScript** - End-to-end type safety
- **🌐 REST APIs** - Default external contract
- **📋 OpenAPI** - API specifications
- **🔌 WebSockets** - Real-time features where needed

### Data Layer
- **🐘 PostgreSQL + PostGIS** - Primary system of record with geospatial support
- **⚡ Redis** - Caching and rate limiting
- **🔍 OpenSearch** - Text search and faceting
- **📦 Object Storage** - Media and large file storage
- **🕸️ Graph Database** - Relationship queries (Neo4j when needed)

### AI/ML
- **🤖 AI Gateway** - Provider-agnostic model access
- **🧠 LLMs** - Language understanding and generation
- **📊 Embedding Models** - Semantic search
- **🎯 Rerankers** - Result refinement
- **🔤 Arabic/English NLP** - Specialized language models

### Infrastructure
- **📨 Kafka/Redpanda** - Event streaming
- **🔐 OAuth 2.0 / OpenID Connect** - Authentication
- **📊 OpenTelemetry** - Observability
- **🧪 Jest/Vitest** - Unit testing
- **🎭 Playwright** - E2E testing
- **🐳 Docker** - Containerization

---

## 🤖 AI Orchestration

### Master Orchestrator
The central AI coordinator that:
1. **🎯 Receives objectives** and classifies tasks
2. **🔍 Identifies affected domains** and requirements
3. **👥 Activates specialist agents** with bounded scopes
4. **⚖️ Reconciles conflicts** between agent recommendations
5. **🛡️ Applies guardrails** and project constraints
6. **✅ Requests approval** for high-impact changes
7. **📝 Records decisions** for auditability

### Specialist AI Roles
- **🏗️ Product Architect** - Product strategy and requirements
- **🧠 AI Systems Designer** - AI architecture and integration
- **🛡️ Security & Trust Guardian** - Security and trust modeling
- **🌐 Ecosystem Strategist** - Platform and partnerships
- **👨‍💻 Developer Lead** - Implementation guidance
- **🎨 UX & Localization Specialist** - User experience design
- **📊 Data Intelligence Lead** - Data architecture and quality
- **🧪 Evaluation Lead** - Testing and validation
- **⚙️ DevOps/SRE Lead** - Operations and reliability
- **📋 Governance Lead** - Policy and compliance

### Separation of Duties
No agent can silently approve its own high-impact changes. Security reviews trust model changes, evaluation validates data logic, and governance approves policy modifications.

---

## 🔒 Security, Privacy & Data Governance

### Security Architecture
- **🛡️ Defense in Depth** - Multiple security layers
- **🔐 Identity & Access** - OAuth 2.0/OIDC with MFA
- **👥 Role-Based Access** - Granular permissions across roles
- **🔍 Input Validation** - Schema validation and parameterized queries
- **🤖 AI Security** - Prompt injection protection and tool scoping
- **🔒 Supply Chain** - Dependency scanning and container security
- **🚨 Incident Response** - Detection, containment, and recovery

### Privacy Principles
- **📉 Data Minimization** - Collect only what's needed
- **🎯 Purpose Limitation** - Use data only for stated purposes
- **🔍 Transparency** - Clear data usage communication
- **👤 User Control** - Access, correction, and deletion rights
- **⏰ Retention Discipline** - Defined data lifecycle policies
- **🌍 Regional Compliance** - Saudi data protection law alignment

### Data Governance
- **📊 Classification** - Public, Internal, Confidential, Restricted
- **👥 Governance Roles** - Data owners, stewards, and custodians
- **📍 Location Privacy** - Precise location only when necessary
- **🔒 Secure Processing** - Encryption and access controls
- **📝 Provenance Tracking** - Complete data lineage
- **⚖️ Accountability** - Clear responsibility assignment

---

## 📚 Documentation Structure

This package is organized into **eight functional layers** plus control documents:

### 📋 Package-Level Documents
- **`README.md`** - This entry point with architecture overview
- **`MANIFEST.md`** - Complete file inventory and navigation map

### 🎯 Layer 01: Product & Strategy
Product vision, target users, requirements, and success criteria

### 🏗️ Layer 02: Core Architecture & Infrastructure  
System architecture, infrastructure, technology stack, and data architecture

### 🧠 Layer 03: Intelligence & Decision Engine
Trust, review intelligence, ranking, recommendations, and explanations

### 🔧 Layer 04: Platform Engineering & Experience
APIs, security, privacy, observability, UX, and accessibility

### 🤖 Layer 05: AI Orchestration & Development Operations
AI roles, agent specifications, skills, guardrails, and execution modes

### ⚙️ Layer 06: Governance, Operations & Delivery
Autonomous operations, testing, monitoring, and delivery roadmap

### 📈 Layer 07: Market, Growth & Expansion
Competitive positioning, SEO, and regional expansion strategy

### 🎮 Layer 08: AI Execution & Governance Control
Master prompts, agent activation, and decision governance

---

## 🎯 Non-Negotiable Principles

- **❌ Never fabricate** places, ratings, reviews, or attributes
- **🔍 Preserve provenance** and acquisition timestamps
- **⚖️ Keep organic ranking** independent from paid visibility
- **🏷️ Clearly label** sponsored content
- **🛡️ Treat external content** as untrusted data
- **📊 Separate trust scoring** from raw ratings
- **📝 Version and audit** high-impact decisions
- **🌐 Support Arabic/English** with RTL/LTR handling
- **🔐 Apply least privilege** across all layers
- **✅ Require human approval** for high-impact changes

---

## 📖 Recommended Reading Order

1. `README.md` (this file)
2. `MANIFEST.md`
3. Layer 01: Product & Strategy
4. Layer 02: Core Architecture & Infrastructure
5. Layer 03: Intelligence & Decision Engine
6. Layer 04: Platform Engineering & Experience
7. Layer 05: AI Orchestration & Development Operations
8. Layer 06: Governance, Operations & Delivery
9. Layer 07: Market, Growth & Expansion
10. Layer 08: AI Execution & Governance Control

**For AI coding environments:** Load Layer 05 and Layer 08 in addition to relevant product/technical layers.

---

## 💡 Additional Suggestions

### 🚀 Getting Started
- Start with Layer 01 to understand product vision
- Review Layer 02 for technical foundation
- Explore Layer 05 for AI development guidelines
- Check Layer 08 for execution prompts and guardrails

### 🔧 Development Workflow
- Follow the non-negotiable principles in all implementations
- Use the specialist AI roles for complex decisions
- Apply separation of duties for high-impact changes
- Maintain audit trails for all modifications

### 📊 Success Metrics
Focus on decision quality rather than traffic:
- Search success rate and user satisfaction
- Trust coverage and source freshness
- Explanation usefulness and organic result integrity
- Business profile correction turnaround

### 🌍 Expansion Strategy
Geographic expansion remains configuration-driven, preserving the production-capable architecture established from MVP.

---

<div align="center">

**Built with ❤️ for trusted place intelligence**

[![GitHub](https://img.shields.io/badge/Github-ma1amin%2FPIOS-blue?logo=github)](https://github.com/ma1amin/PIOS)

</div>
