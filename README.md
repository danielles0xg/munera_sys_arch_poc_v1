# MUNERA DILIGENCE — SYSTEM ARCHITECTURE & POC JUSTIFICATION
## Phased Roadmap with Component Pricing & Design Options
### February 26, 2026

---

## Document Index

### 1. Business & Costs

| # | Document | Description |
|---|----------|-------------|
| 1.1 | [Executive Summary](./EXECUTIVE_SUMMARY.md) | $1.5M / 24-month cost summary, infrastructure overview, operations, risk matrix, funding stack |
| 1.2 | [Budget & Burn Rate](./BUDGET_AND_BURN_RATE.md) | Full $1.5M breakdown — platform costs, hiring spread, phase cost table, monthly burn rate, key takeaways |
| 1.3 | [Phase Cost Breakdowns](./PHASE_COST_BREAKDOWNS.md) | Cost tables for all 9 phases (P0–P8) consolidated |
| 1.4 | [Component Pricing Options](./COMPONENT_PRICING_OPTIONS.md) | 12 components with 5 vendor options each — comparison tables |
| 1.5 | [Pricing Verification](./PRICING_VERIFICATION.md) | Every cost verified with source links (February 2026) |
| 1.6 | [SOC 2 Compliance](./SOC2_COMPLIANCE.md) | SOC 2 Type I/II plan, platform & audit firm options, pen test vendors, budget, timeline |
| 1.7 | [Funding & Government Programs](./FUNDING_AND_GOVERNMENT_PROGRAMS.md) | SR&ED, Scale AI, NRC IRAP, Mitacs, Google for Startups — recovery estimates |
| 1.8 | [POC Justification](./POC_JUSTIFICATION.md) | Why this POC is justified — the math, standalone value, risk management |

### 2. Tech Design

| # | Document | Description |
|---|----------|-------------|
| 2.1 | [System Architecture](./SYSTEM_ARCHITECTURE.md) | Architecture diagrams, data flow, component topology |
| 2.2 | [Recommended Stack](./RECOMMENDED_STACK.md) | Recommended technology stack for MVP (Mo 1–6) and production (Mo 7–12) |

### 3. Phases (Tech Design)

| # | Document | Months | Description |
|---|----------|--------|-------------|
| 3.0 | [Phase 0 — Foundation](./PHASE_0_FOUNDATION.md) | 1–2 | Backend API, PostgreSQL, object storage, observability, CI/CD, IaC |
| 3.1 | [Phase 1 — Core Migration](./PHASE_1_CORE_MIGRATION.md) | 1–3 | Auth, RBAC, multi-tenant DB, 30+ component migration, bilingual |
| 3.2 | [Phase 2 — AI Invoice & Contract](./PHASE_2_AI_INVOICE_CONTRACT.md) | 2–4 | OCR pipeline, contract AI agent, invoice validation, RAG, fraud detection |
| 3.3 | [Phase 3 — Lender & Backoffice](./PHASE_3_LENDER_BACKOFFICE.md) | 3–5 | CTC/EAC engine, draw risk scoring, HITL queue, report generator |
| 3.4 | [Phase 4 — Compliance & Clock](./PHASE_4_COMPLIANCE_CLOCK.md) | 3–5 | Provincial holdback engine, prompt payment clock, CCDC RAG, jurisdiction selector |
| 3.5 | [Phase 5 — Schedule Intel & BIM](./PHASE_5_SCHEDULE_BIM.md) | 5–7 | MCP4IFC, earned value, delay prediction, BIM progress overlay, photo CV |
| 3.6 | [Phase 6 — Integrations](./PHASE_6_INTEGRATIONS.md) | 6–8 | Procore, SAP, QuickBooks, banking API, email, webhook framework |
| 3.7 | [Phase 7 — Pilot & Validation](./PHASE_7_PILOT_VALIDATION.md) | 8–10 | Shadow deployment, pen test, load test, user training, feedback loop |
| 3.8 | [Phase 8 — Production Ready](./PHASE_8_PRODUCTION_READY.md) | 10–12 | SOC 2 prep, US market, analytics dashboard, HA, payment gateway |
