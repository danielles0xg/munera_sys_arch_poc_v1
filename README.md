# MUNERA DILIGENCE — SYSTEM ARCHITECTURE & POC JUSTIFICATION
## Phased Roadmap with Component Pricing & Design Options
### February 26, 2026

---

Every cost, technology choice, and market figure in this document set is verified against real, current pricing:

- **Infrastructure costs** are sourced from live pricing pages as of February 2026 — see [Pricing Verification](./BUSINESS/PRICING_VERIFICATION.md) for every line item with direct links to [Cloud Run](https://cloud.google.com/run/pricing), [Vertex AI](https://cloud.google.com/vertex-ai/pricing), [Supabase](https://supabase.com/pricing), [Cloudflare R2](https://developers.cloudflare.com/r2/pricing/), [Document AI](https://cloud.google.com/document-ai/pricing), and [Hetzner](https://www.hetzner.com/dedicated-rootserver/)
- **Vendor comparisons** cover 12 components with 5 options each — see [Component Pricing Options](./BUSINESS/COMPONENT_PRICING_OPTIONS.md)
- **Government funding** estimates cite program rules directly from [SR&ED (CRA)](https://www.canada.ca/en/revenue-agency/services/scientific-research-experimental-development-tax-incentive-program.html), [Scale AI](https://www.scaleai.ca/projects/), [NRC IRAP](https://nrc-cnrc.gc.ca/eng/irap/index.html), [Mitacs](https://www.mitacs.ca/our-programs/), and [Google for Startups AI Tier](https://cloud.google.com/startup/ai)
- **Market sizing** references [Statistics Canada](https://www.statcan.gc.ca/), [GlobalData](https://www.globaldata.com/store/report/canada-construction-market-analysis/), and [Research and Markets](https://www.researchandmarkets.com/report/canada-construction-market)
- **Competitor benchmarks** are from [Crunchbase (Built Technologies)](https://www.crunchbase.com/organization/built-technologies-inc), [Rabbet](https://rabbet.com/), and [TIMVERO](https://timvero.com/construction-loan-software)
- **Regulatory deadlines** cite the [Quebec National Assembly (Bill 62)](https://www.assnat.qc.ca/en/travaux-parlementaires/projets-loi/projet-loi-62-43-1.html), [Miller Thomson analysis](https://www.millerthomson.com/en/insights/construction-and-infrastructure-law/how-the-new-regulation-respecting-prompt-payments-is-changing-construction-contracts-in-quebec/), and [provincial legislation](https://www.ontario.ca/laws/statute/90c30)

### The Investment

| | |
|---|---|
| **Total budget** | $1.5M over 24 months |
| **Platform costs** | $291K (19.4%) — infrastructure, licenses, compliance, operations |
| **People** | $1.21M (80.6%) — engineering, technical leadership, QA |
| **Cloud Year 1** | ~$0 effective cost via [Google for Startups AI credits](https://cloud.google.com/startup/ai) ($350K over 2 years) |
| **Government co-funding** | Up to $1.3M–$1.7M recoverable ([SR&ED](https://www.canada.ca/en/revenue-agency/services/scientific-research-experimental-development-tax-incentive-program.html) + [Scale AI](https://www.scaleai.ca/projects/) + [IRAP](https://nrc-cnrc.gc.ca/eng/irap/index.html) + [Mitacs](https://www.mitacs.ca/our-programs/)) |
| **Effective out-of-pocket** | ~$0–$200K after all programs |

---

## Document Index

### 1. Business & Costs

| # | Document | Description |
|---|----------|-------------|
| 1.1 | [Executive Summary](./BUSINESS/EXECUTIVE_SUMMARY.md) | $1.5M / 24-month cost summary, infrastructure overview, operations, risk matrix, funding stack |
| 1.2 | [Budget & Burn Rate](./BUSINESS/BUDGET_AND_BURN_RATE.md) | Full $1.5M breakdown — platform costs, hiring spread, phase cost table, monthly burn rate, key takeaways |
| 1.3 | [Phase Cost Breakdowns](./PHASES/PHASE_COST_BREAKDOWNS.md) | Cost tables for all 9 phases (P0–P8) consolidated |
| 1.4 | [Component Pricing Options](./BUSINESS/COMPONENT_PRICING_OPTIONS.md) | 12 components with 5 vendor options each — comparison tables |
| 1.5 | [Pricing Verification](./BUSINESS/PRICING_VERIFICATION.md) | Every cost verified with source links (February 2026) |
| 1.6 | [SOC 2 Compliance](./BUSINESS/SOC2_COMPLIANCE.md) | SOC 2 Type I/II plan, platform & audit firm options, pen test vendors, budget, timeline |
| 1.7 | [Funding & Government Programs](./BUSINESS/FUNDING_AND_GOVERNMENT_PROGRAMS.md) | SR&ED, Scale AI, NRC IRAP, Mitacs, Google for Startups — recovery estimates |
| 1.8 | [POC Justification](./PHASES/POC_JUSTIFICATION.md) | Why this POC is justified — the math, standalone value, risk management |

### 2. Tech Design

| # | Document | Description |
|---|----------|-------------|
| 2.1 | [System Architecture](./SYSTEM_DESIGN/SYSTEM_ARCHITECTURE.md) | Architecture diagrams, data flow, component topology |
| 2.2 | [Recommended Stack](./SYSTEM_DESIGN/RECOMMENDED_STACK.md) | Recommended technology stack for MVP (Mo 1–6) and production (Mo 7–12) |

### 3. Phases (Tech Design)

| # | Document | Months | Description |
|---|----------|--------|-------------|
| 3.0 | [Phase 0 — Foundation](./PHASES/PHASE_0_FOUNDATION.md) | 1–2 | Backend API, PostgreSQL, object storage, observability, CI/CD, IaC |
| 3.1 | [Phase 1 — Core Migration](./PHASES/PHASE_1_CORE_MIGRATION.md) | 1–3 | Auth, RBAC, multi-tenant DB, 30+ component migration, bilingual |
| 3.2 | [Phase 2 — AI Invoice & Contract](./PHASES/PHASE_2_AI_INVOICE_CONTRACT.md) | 2–4 | OCR pipeline, contract AI agent, invoice validation, RAG, fraud detection |
| 3.3 | [Phase 3 — Lender & Backoffice](./PHASES/PHASE_3_LENDER_BACKOFFICE.md) | 3–5 | CTC/EAC engine, draw risk scoring, HITL queue, report generator |
| 3.4 | [Phase 4 — Compliance & Clock](./PHASES/PHASE_4_COMPLIANCE_CLOCK.md) | 3–5 | Provincial holdback engine, prompt payment clock, CCDC RAG, jurisdiction selector |
| 3.5 | [Phase 5 — Schedule Intel & BIM](./PHASES/PHASE_5_SCHEDULE_BIM.md) | 5–7 | MCP4IFC, earned value, delay prediction, BIM progress overlay, photo CV |
| 3.6 | [Phase 6 — Integrations](./PHASES/PHASE_6_INTEGRATIONS.md) | 6–8 | Procore, SAP, QuickBooks, banking API, email, webhook framework |
| 3.7 | [Phase 7 — Pilot & Validation](./PHASES/PHASE_7_PILOT_VALIDATION.md) | 8–10 | Shadow deployment, pen test, load test, user training, feedback loop |
| 3.8 | [Phase 8 — Production Ready](./PHASES/PHASE_8_PRODUCTION_READY.md) | 10–12 | SOC 2 prep, US market, analytics dashboard, HA, payment gateway |
