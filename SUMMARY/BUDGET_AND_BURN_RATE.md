# BUDGET SUMMARY — FIT TO $1.5M / 24 MONTHS

## Total Budget Envelope: $1,500,000

---

## PLATFORM COSTS (Non-Personnel)

These are the hard costs: cloud infrastructure, APIs, tools, licenses, audits, legal — everything that is NOT salaries.

### Cloud Infrastructure (24 Months)

| Component | Recommended | Mo. 1-6 | Mo. 7-12 | Mo. 13-18 | Mo. 19-24 | 24-Mo Total |
|-----------|------------|---------|----------|-----------|-----------|-------------|
| Backend API (Cloud Run) | Google Cloud Run | $50 | $150 | $300 | $400 | **$5,400** |
| **Vertex AI Platform** | **Pipelines + RAG + Agent Builder** | **$50** | **$150** | **$200** | **$250** | **$3,900** |
| LLM Models (via Vertex AI) | Gemini 2.5 Flash + Claude | $200 | $800 | $1,200 | $1,600 | **$22,800** |
| Database (PostgreSQL) | Supabase Pro then Cloud SQL | $75 | $150 | $200 | $250 | **$4,050** |
| Object Storage | Cloudflare R2 | $20 | $40 | $60 | $80 | **$1,200** |
| OCR/Doc Processing | Document AI + Textract | $100 | $300 | $500 | $600 | **$9,000** |
| Auth | Firebase Auth | $0 | $0 | $0 | $0 | **$0** |
| Observability | Grafana Cloud + Sentry | $0 | $50 | $80 | $100 | **$1,380** |
| CI/CD | GitHub Actions | $0 | $10 | $20 | $20 | **$300** |
| BIM Server | Hetzner Dedicated | $0 | $60 | $90 | $90 | **$1,440** |
| Message Queue | Upstash Redis | $0 | $10 | $20 | $30 | **$360** |
| Vector DB | pgvector (included) | $0 | $0 | $0 | $0 | **$0** |
| CDN/Frontend | Vercel Pro | $0 | $20 | $20 | $20 | **$360** |
| **CLOUD SUBTOTAL** | | **$495/mo** | **$1,740/mo** | **$2,690/mo** | **$3,440/mo** | **$50,190** |
| **After Startup Credits** | *Google for Startups AI Tier* | **~$0** | **~$0** | **$1,490/mo** | **$3,440/mo** | **~$29,580** |

### Software Licenses & Tools (24 Months)

| Item | Annual Cost | 24-Mo Total |
|------|-----------|-------------|
| CCDC document licensing | $3K/yr | **$6,000** |
| Compliance platform (Sprinto/Drata) | $8K/yr | **$16,000** |
| Security scanning (Snyk + SonarQube) | $5K/yr | **$10,000** |
| Dev tools & IDE licenses | $3K/yr | **$6,000** |
| Domain, DNS, email (Google Workspace) | $2K/yr | **$4,000** |
| **LICENSES SUBTOTAL** | | **$42,000** |

### SOC 2 Compliance (Non-Personnel Portion)

| Item | Cost |
|------|------|
| SOC 2 Type I Audit | $15,000 |
| SOC 2 Type II Audit (Year 2) | $20,000 |
| Penetration Testing (2 rounds) | $12,000 |
| Policy Development (legal review) | $8,000 |
| Security Training | $4,000 |
| Vulnerability Scanning Tools | $5,000 |
| **SOC 2 NON-PERSONNEL SUBTOTAL** | **$64,000** |

### Other Non-Personnel Costs (24 Months)

| Item | Cost |
|------|------|
| API/integration partnership fees (Procore, SAP, banking) | $10,000 |
| Data curation (IFC models, invoice datasets, schedules) | $20,000 |
| Travel (pilot site visits, investor meetings, conferences) | $10,000 |
| Legal (contracts, IP, partnership agreements) | $20,000 |
| UX/UI design (contract or freelance) | $20,000 |
| User training materials & onboarding | $8,000 |
| Insurance (E&O, cyber) | $12,000 |
| Accounting & bookkeeping | $15,000 |
| Office / coworking (Centech subsidized) | $18,000 |
| Miscellaneous / contingency | $22,000 |
| **OTHER SUBTOTAL** | **$155,000** |

---

## PLATFORM COST SUMMARY TABLE

| Category | 24-Month (List) | After Startup Credits | % of $1.5M |
|----------|-----------------|----------------------|------------|
| Cloud & AI Infrastructure | $50,190 | **$29,580** | 2.0% |
| Software Licenses & Tools | $42,000 | $42,000 | 2.8% |
| SOC 2 Compliance (non-personnel) | $64,000 | $64,000 | 4.3% |
| Other Non-Personnel (legal, travel, data, design, etc.) | $155,000 | $155,000 | 10.3% |
| **TOTAL PLATFORM COSTS** | $311,190 | **$290,580** | **19.4%** |
| | | | |
| **REMAINING FOR HIRING (PERSONNEL)** | | **$1,209,420** | **80.6%** |

*Google for Startups AI Tier ($250K Year 1 + $100K Year 2) covers all GCP services: Cloud Run, Vertex AI, Gemini models, Document AI, Firebase. This saves ~$20.6K in real cloud spend and adds $233K buffer for scaling.*

---

## SPREAD FOR HIRING

| | Amount |
|--|--------|
| Total Budget | $1,500,000 |
| Platform Costs (after startup credits) | ($290,580) |
| **Available for Personnel** | **$1,209,420** |

This **$1.21M personnel envelope** covers 24 months of:
- Engineering salaries (backend, frontend, AI/ML, DevOps)
- Technical leadership
- Part-time security engineer (SOC 2 controls)
- QA/testing resources
- Contractors / freelancers for specialized work (BIM, CV)

*Personnel analysis will be done separately — this document establishes the fixed platform costs and the remaining budget available for the team.*

---

## PHASE-BY-PHASE COST TABLE (Fit to $1.5M)

Each phase total includes both platform costs and personnel. Personnel allocation is estimated here to show phase distribution — detailed hiring plan follows separately.

| Phase | Name | Months | Platform Cost | Personnel (est.) | Phase Total | Cumulative |
|-------|------|--------|--------------|------------------|-------------|------------|
| **P0** | Foundation | 1-2 | $6K | $79K | **$85K** | $85K |
| **P1** | Core Migration | 1-3 | $10K | $95K | **$105K** | $190K |
| **P2** | AI Invoice/Contract | 2-4 | $15K | $120K | **$135K** | $325K |
| **P3** | Lender/Backoffice | 3-5 | $12K | $108K | **$120K** | $445K |
| **P4** | Compliance/Clock | 3-5 | $18K | $97K | **$115K** | $560K |
| **P5** | Schedule Intel + BIM | 5-7 | $22K | $118K | **$140K** | $700K |
| **P6** | Integrations | 6-8 | $18K | $82K | **$100K** | $800K |
| **P7** | Pilot/Validation | 8-10 | $30K | $110K | **$140K** | $940K |
| **P8** | Production Ready | 10-12 | $25K | $100K | **$125K** | $1,065K |
| **Year 2** | Scale + Expand | 13-24 | $135K | $300K | **$435K** | $1,500K |
| | | | | | | |
| **TOTAL** | | **24 mo** | **$291K** | **$1,209K** | **$1,500K** | |

---

## MONTHLY BURN RATE PROJECTION

| Period | Monthly Burn | Cumulative |
|--------|-------------|------------|
| Months 1-3 | ~$63K/mo | $190K |
| Months 4-6 | ~$74K/mo | $412K |
| Months 7-9 | ~$80K/mo | $652K |
| Months 10-12 | ~$69K/mo | $860K-$940K |
| Months 13-18 | ~$47K/mo | $1,220K |
| Months 19-24 | ~$47K/mo | **$1,500K** |

**Average monthly burn: ~$62.5K/mo over 24 months**

---

## KEY TAKEAWAYS

### 1. Platform costs are only 19.4% of budget
Cloud + tools + compliance + operations = **$291K** out of $1.5M. The platform is cheap. **Talent is the investment.**

### 2. Cloud costs near-zero Year 1 with Google for Startups
Vertex AI + Cloud Run + Gemini + Document AI = **$50K over 24 months** at list price, but Google for Startups AI Tier ($350K in credits over 2 years) covers nearly all GCP spend. **Effective Year 1 cloud cost: ~$0. Year 2: ~$30K.**

### 3. $1.21M gives meaningful hiring runway
At an average blended cost of $8K-$12K/month per engineer (salary + benefits + tools), the personnel budget supports:
- **3-5 engineers for 12 months** (Year 1 sprint), then
- **2-3 engineers for 12 months** (Year 2 maintenance + scale)
- Plus technical leadership, contractors, and specialist engagements throughout

### 4. Year 2 is lean by design
Year 1 builds the platform ($1.07M). Year 2 operates, scales, and commercializes ($435K). The burn rate drops 35-40% in Year 2 because the heavy engineering is done.

### 5. Government co-funding further de-risks
- Google for Startups: **$350K-$372K** in GCP credits
- SR&ED + Quebec CRIC: **$545K-$560K** in tax credit recovery
- Scale AI: 40-50% co-investment on eligible R&D = **$340K-$680K**
- NRC IRAP + Mitacs: up to $110K for youth hires/interns
- **Effective out-of-pocket after all programs: ~$0-$200K**

---

## References

- [Google Cloud Run Pricing](https://cloud.google.com/run/pricing)
- [Vertex AI Pricing](https://cloud.google.com/vertex-ai/pricing)
- [Vertex AI Generative AI Pricing](https://cloud.google.com/vertex-ai/generative-ai/pricing)
- [Supabase Pricing](https://supabase.com/pricing)
- [Cloudflare R2 Pricing](https://developers.cloudflare.com/r2/pricing/)
- [Google Document AI Pricing](https://cloud.google.com/document-ai/pricing)
- [Firebase Pricing](https://firebase.google.com/pricing)
- [Grafana Cloud Pricing](https://grafana.com/pricing/)
- [Sentry Pricing](https://sentry.io/pricing/)
- [GitHub Pricing](https://github.com/pricing)
- [Hetzner Dedicated Servers](https://www.hetzner.com/dedicated-rootserver/)
- [Upstash Redis Pricing](https://upstash.com/pricing/redis)
- [Vercel Pricing](https://vercel.com/pricing)
- [Google for Startups AI Tier](https://cloud.google.com/startup/ai)
- [Sprinto Pricing](https://sprinto.com/pricing/)
- [Snyk Plans](https://snyk.io/plans/)
- [Google Workspace Pricing](https://workspace.google.com/pricing)
- [CCDC Contracts](https://www.ccdc.org/resources/contracts/)
- [Zensurance Technology Insurance](https://www.zensurance.com/technology-insurance)
