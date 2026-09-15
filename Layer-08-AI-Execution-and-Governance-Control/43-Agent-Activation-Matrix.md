# Agent Activation Matrix

| Trigger | Primary Agent | Supporting Agents | Approval |
|---|---|---|---|
| New product feature | Product Architect | Developer, UX, Security | Normal change process |
| Ranking model/config change | Data Intelligence / Evaluation | Security & Trust, Product | Required |
| Trust model/config change | Security & Trust Guardian | Data, Evaluation, Governance | Required |
| New external data source | Data Intelligence Lead | Governance, Security, Ecosystem | Required before production |
| New country | Ecosystem Strategist | Localization, Governance, Data, Security | Required |
| New category | Product Architect | Data, UX, Evaluation | Normal, elevated if sensitive |
| Arabic UX change | UX & Localization | Product, Accessibility/Developer | Normal |
| Database schema migration | Developer Lead | Data, DevOps, Security | Required for destructive/high-risk |
| Production incident | DevOps/SRE | Security, Developer, relevant domain owner | Incident authority |
| AI model/provider change | AI Systems Designer | Evaluation, Security, DevOps | Required for material behavior change |
| Privacy/retention change | Governance Lead | Security, Product, Data | Required |
| Authentication/authorization change | Security Guardian | Developer, Governance | Required |
| Monetization/sponsored placement | Ecosystem Strategist | Product, Governance, Trust | Required |
| SEO architecture | Ecosystem/Product | Developer, UX | Normal |
| Entity-resolution threshold change | Data Intelligence | Evaluation, Trust | Required |
| Community moderation policy | Governance/Product | Security, Community/Data | Required |

## Conflict Resolution
Priority:
1. Security and safety.
2. Legal/privacy obligations.
3. Trust/data integrity.
4. Explicit product/user requirements.
5. Commercial objectives.
6. Convenience/performance.

## Separation Rule
No specialist may silently approve its own high-impact change. The orchestrator must route material changes to an independent reviewer and preserve the decision record.
