# EXECUTIVE SUMMARY — $1.5M / 24 MONTHS

## Cost Summary

| Category | 24-Month Total | % of Budget |
|----------|---------------|-------------|
| **Cloud & AI Infrastructure** | $29,580 | 2.0% |
| **Software Licenses & Tools** | $42,000 | 2.8% |
| **SOC 2 Compliance** | $64,000 | 4.3% |
| **Operations** (legal, insurance, office, travel, data) | $155,000 | 10.3% |
| **TOTAL PLATFORM** | **$290,580** | **19.4%** |
| **PERSONNEL** (engineering, technical leadership, QA, contractors) | **$1,209,420** | **80.6%** |
| **TOTAL** | **$1,500,000** | **100%** |

*Cloud infrastructure at list price is $50K, reduced to $30K via Google for Startups AI credits ($350K over 2 years).*

## Infrastructure

| Layer | Technology | Monthly Cost | Why |
|-------|-----------|-------------|-----|
| AI Platform | **Vertex AI** (Pipelines, RAG Engine, Agent Builder) | $50-$250 | Enterprise security (VPC-SC, CMEK), Context Caching (90% LLM savings), consolidated audit logging |
| LLM Models | **Gemini 2.5 Flash** (90%) + **Claude Sonnet** (10%) via Vertex AI | $200-$1,600 | Flash for extraction, Sonnet for compliance reasoning |
| Backend | **Cloud Run** (FastAPI, auto-scale to zero) | $50-$400 | Pay-per-request, Montreal region, no idle cost |
| Database | **Supabase** (PostgreSQL + pgvector + RLS) | $75-$250 | DB + vector + auth + storage in one, SOC 2 at Team tier |
| Storage | **Cloudflare R2** (zero egress) | $20-$80 | PDFs, IFC files, photos — 60-80% cheaper than S3 |
| OCR | **Google Document AI** | $100-$600 | Best FR/EN accuracy, $0.0015-$0.01/page, native Vertex integration |
| BIM | **Hetzner Dedicated** (IfcOpenShell + MCP4IFC) | $0-$68 | CPU-intensive processing at 1/4 the cost of cloud VMs |
| Observability | **Grafana Cloud + Sentry** (OTel) | $0-$100 | Free tier covers P0-P4, production-grade at $100/mo |

## Operations

| Item | Annual Cost | Notes |
|------|-----------|-------|
| Google Workspace (5-8 users) | $2,000 | Email, docs, calendar |
| CCDC contract licensing | $3,000 | Full suite: 2, 5A, 5B, 9A, 9B, 17, 30 |
| Compliance platform (Sprinto) | $8,000 | SOC 2 + ISO 27001 automation |
| Security scanning (Snyk + SonarQube) | $5,000 | SAST + SCA + dependency alerts |
| Insurance (E&O + Cyber) | $6,000 | Professional liability + cyber coverage |
| Coworking (Centech subsidized) | $9,000 | Free Year 1 via Centech, budget for growth |
| Accounting + bookkeeping | $7,500 | Monthly books + SR&ED prep |
| Legal (contracts, IP) | $10,000 | Partnership agreements, IP protection |
| Travel (pilot sites, investors) | $10,000 | Montreal-area pilot visits + conferences |

## Risk Matrix

| Risk | Impact | Likelihood | Mitigation |
|------|--------|-----------|------------|
| **AI accuracy below 90%** | High | Medium | HITL review catches errors; shadow deployment (P7) validates before go-live; Vertex AI evaluation tools benchmark continuously |
| **Quebec prompt payment deadline missed** | High | Low | P4 targets compliance engine by Month 5; deadline is Sept 2026 (7 months buffer); modular jurisdiction selector |
| **Google for Startups credits denied** | Medium | Low | Budget works at list price ($50K cloud); credits are upside not dependency; Centech accelerator strengthens application |
| **Key engineer departure** | High | Medium | Documentation-first culture; modular architecture limits bus factor; $1.2M personnel budget allows overlap hiring |
| **SOC 2 audit delays** | Medium | Medium | Compliance platform (Sprinto) from Month 1; parallel track to development; budget includes $10K remediation contingency |
| **Pilot partner unavailable** | Medium | Low | Target 3 pilot candidates simultaneously; Centech network for intros; demo-able product by P3 reduces partner friction |
| **LLM pricing increases** | Low | Medium | Multi-model strategy (Gemini + Claude); Context Caching locks in 90% savings on templates; can switch to Gemini 2.0 Flash at $0.10/MTok |
| **Scale AI co-investment rejected** | Medium | Medium | Budget is self-sufficient at $1.5M; Scale AI is de-risking upside ($340-680K); SR&ED credits ($545K) are independent fallback |
| **Scope creep across phases** | High | High | Each phase has explicit deliverables checklist; technical lead gate review between phases; contingency buffer (~15% per phase) |
| **Data residency / Law 25 non-compliance** | High | Low | GCP Montreal region (northamerica-northeast1); Supabase RLS for tenant isolation; Vertex AI VPC-SC for data boundary enforcement |

## Funding Stack (Potential Recovery)

| Program | Amount | Status |
|---------|--------|--------|
| Google for Startups AI Tier | $350K-$372K | Apply on seed close |
| SR&ED Federal + Quebec CRIC | $545K-$560K | File annually |
| Scale AI co-investment | $340K-$680K | Requires industry partner |
| NRC IRAP + Mitacs | $60K-$110K | Per hire/intern |
| **TOTAL POTENTIAL** | **$1.3M-$1.7M** | |
| **Effective out-of-pocket** | **~$0-$200K** | After all programs |

---

## References

- [Google Cloud Run Pricing](https://cloud.google.com/run/pricing)
- [Vertex AI Pricing](https://cloud.google.com/vertex-ai/pricing)
- [Vertex AI Generative AI Pricing](https://cloud.google.com/vertex-ai/generative-ai/pricing)
- [Supabase Pricing](https://supabase.com/pricing)
- [Cloudflare R2 Pricing](https://developers.cloudflare.com/r2/pricing/)
- [Google Document AI Pricing](https://cloud.google.com/document-ai/pricing)
- [Hetzner Dedicated Servers](https://www.hetzner.com/dedicated-rootserver/)
- [Grafana Cloud Pricing](https://grafana.com/pricing/)
- [Sentry Pricing](https://sentry.io/pricing/)
- [Google for Startups AI Tier](https://cloud.google.com/startup/ai)
- [SR&ED Tax Incentive Program](https://www.canada.ca/en/revenue-agency/services/scientific-research-experimental-development-tax-incentive-program.html)
- [Scale AI Projects](https://www.scaleai.ca/projects/)
- [NRC IRAP](https://nrc-cnrc.gc.ca/eng/irap/index.html)
- [Mitacs Programs](https://www.mitacs.ca/our-programs/)
