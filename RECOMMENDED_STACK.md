# RECOMMENDED STACK — STARTUP BUDGET

## Months 1-6 (MVP/Pilot)

| Component | Choice | Monthly Cost |
|-----------|--------|-------------|
| Frontend Hosting | Vercel (Pro) | $20 |
| Backend API | Google Cloud Run | $100 |
| **AI Platform** | **Vertex AI (Pipelines + RAG Engine + Agent Builder)** | **$50** |
| LLM Models | Gemini 2.5 Flash + Claude Haiku (via Vertex AI) | $350 |
| Database | Supabase (Pro) | $75 |
| Object Storage | Cloudflare R2 | $20 |
| Auth | Firebase Auth (free) | $0 |
| OCR | Google Document AI | $150 |
| Observability | Grafana Cloud (free tier) | $0 |
| CI/CD | GitHub Actions (free tier) | $0 |
| BIM Server | Hetzner (on-demand, P2+) | $60 |
| Message Queue | Upstash Redis | $10 |
| Vector DB | pgvector (in Supabase) | $0 |
| **TOTAL** | | **~$835/mo** |

*Note: With Google for Startups credits ($250K Year 1), Vertex AI + Gemini + Document AI + Cloud Run costs are effectively $0 for the first 12 months.*

## Months 7-12 (Scale/Production)

| Component | Choice | Monthly Cost |
|-----------|--------|-------------|
| Frontend Hosting | Vercel (Pro) | $20 |
| Backend API | Google Cloud Run (scaled) | $300 |
| **AI Platform** | **Vertex AI (Pipelines + RAG Engine + Context Cache + Agent Builder)** | **$150** |
| LLM Models | Gemini 2.5 Flash + Pro + Claude Sonnet (via Vertex AI) | $1,200 |
| Database | Cloud SQL (HA) or Supabase (Team) | $200 |
| Object Storage | Cloudflare R2 | $40 |
| Auth | Firebase Auth | $0 |
| OCR | Google Document AI | $400 |
| Observability | Grafana Cloud (Pro) | $50 |
| CI/CD | GitHub Actions | $20 |
| BIM Server | Hetzner Dedicated | $90 |
| Message Queue | Upstash Redis (Pro) | $30 |
| Vector DB | pgvector | $0 |
| **TOTAL** | | **~$2,500/mo** |

## 12-Month Cloud Cost Summary

| Period | Monthly | Duration | Subtotal | After Startup Credits |
|--------|---------|----------|----------|-----------------------|
| Months 1-3 (light) | $600 | 3 months | $1,800 | ~$0 (covered) |
| Months 4-6 (growing) | $835 | 3 months | $2,505 | ~$0 (covered) |
| Months 7-9 (production) | $1,800 | 3 months | $5,400 | ~$0 (covered) |
| Months 10-12 (full) | $2,500 | 3 months | $7,500 | ~$0 (covered) |
| **12-MONTH TOTAL** | | | **$17,205** | **~$0 with $250K credits** |

*Google for Startups AI Tier covers up to $250K in Year 1 GCP usage. Our $17K Year 1 GCP spend is well within the credit envelope, leaving $233K in unused credits as buffer.*

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
- [GitHub Pricing](https://github.com/pricing)
- [Hetzner Dedicated Servers](https://www.hetzner.com/dedicated-rootserver/)
- [Upstash Redis Pricing](https://upstash.com/pricing/redis)
- [Vercel Pricing](https://vercel.com/pricing)
- [Google for Startups AI Tier](https://cloud.google.com/startup/ai)
