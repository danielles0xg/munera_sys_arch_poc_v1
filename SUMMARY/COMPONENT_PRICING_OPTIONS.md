# COMPONENT PRICING — 5 OPTIONS EACH

## 1. Backend API Hosting (2-4 vCPU, 4-8GB RAM)

| Option | Provider | Monthly Cost | Pros | Cons |
|--------|----------|-------------|------|------|
| **Google Cloud Run** (Rec.) | GCP | **$50-$150** | Pay-per-request, auto-scale to 0, no idle cost | Cold starts |
| AWS ECS Fargate | AWS | $120-$300 | Proven, full AWS ecosystem | More expensive at low scale |
| Railway | Railway | $20-$100 | Fastest dev experience, easy deploy | Less enterprise features |
| Render | Render | $25-$85 | Simple, auto-deploy from Git | Fewer regions |
| Azure Container Apps | Azure | $100-$250 | Good if Azure ecosystem | Least community support |

## 2. Database — PostgreSQL + pgvector

| Option | Provider | Monthly Cost | Pros | Cons |
|--------|----------|-------------|------|------|
| **Supabase** (Rec. P0-P5) | Supabase | **$25-$75** (Pro) | pgvector, auth, storage, realtime included | Less control |
| Neon | Neon | $19-$69 | Serverless PG, scales to 0, branching | Newer, less proven |
| Google Cloud SQL | GCP | $50-$200 | Managed, reliable, HA | No extras included |
| AWS RDS PostgreSQL | AWS | $80-$300 | Battle-tested, Multi-AZ | Expensive for startup |
| Azure DB for PostgreSQL | Azure | $70-$250 | Flexible Server, good HA | Ecosystem lock-in |

## 3. Object Storage (PDFs, IFC files, photos — 1TB)

| Option | Provider | Monthly Cost | Pros | Cons |
|--------|----------|-------------|------|------|
| **Cloudflare R2** (Rec.) | Cloudflare | **$15-$25** | Zero egress fees, S3-compatible | Fewer features |
| Supabase Storage | Supabase | $25 (included in Pro) | Already in stack if using Supabase | Size limits |
| AWS S3 | AWS | $23-$50 | Industry standard, lifecycle policies | Egress fees add up |
| Google Cloud Storage | GCP | $20-$45 | Good with GCP ecosystem | Egress fees |
| Backblaze B2 | Backblaze | $5-$15 | Cheapest, S3-compatible | Fewer regions |

## 4. AI / LLM Orchestration Platform

| Option | Provider | Monthly Platform Cost | Pros | Cons |
|--------|----------|-----------------------|------|------|
| **Vertex AI** (Rec.) | Google Cloud | **$0 platform + pay-per-use** | Enterprise security (VPC-SC, CMEK, audit logs), RAG Engine, Pipelines ($0.03/run), Model Garden, Context Caching (90% savings), Agent Builder | GCP lock-in for orchestration |
| AWS Bedrock | AWS | $0 platform + pay-per-use | Multi-model (Claude, Titan, Llama), Knowledge Bases, Guardrails | Less Gemini integration |
| Azure AI Studio | Microsoft | $0 platform + pay-per-use | GPT-4o native, Prompt Flow, enterprise Azure integration | Weakest Gemini support |
| Direct APIs (Gemini + Claude) | Mixed | $0 | Simplest setup, free tiers, no vendor lock-in | No enterprise controls, no RAG Engine, no audit logs, manual orchestration |
| LangSmith + Direct APIs | LangChain | $39-$400/mo + API costs | Best LangGraph integration, tracing, evaluation | Additional vendor, no infra security |

### LLM Model Pricing (via Vertex AI)

| Model | Input/1M tokens | Output/1M tokens | Batch (50% off) | Context Cache |
|-------|-----------------|-------------------|------------------|---------------|
| **Gemini 2.5 Flash** (Rec. 90% of calls) | $0.30 | $2.50 | $0.15 / $1.25 | $0.0375 input (~87.5% savings) |
| **Gemini 2.5 Pro** (complex reasoning) | $1.25 | $10.00 | $0.625 / $5.00 | $0.125 input (90% savings) |
| Gemini 2.0 Flash | $0.15 | $0.60 | $0.075 / $0.30 | $0.025 input |
| Claude Sonnet 4.6 (via Model Garden) | $3.00 | $15.00 | N/A | N/A |
| Claude Haiku 4.5 (via Model Garden) | $1.00 | $5.00 | N/A | N/A |
| Claude Opus 4.6 (via Model Garden) | $5.00 | $25.00 | N/A | N/A |

*Strategy: Gemini 2.5 Flash for 90% of calls (OCR, extraction, classification) with Context Caching on CCDC templates. Gemini 2.5 Pro or Claude Sonnet for 10% (complex compliance reasoning). All routed through Vertex AI for enterprise security + audit logging.*

### Vertex AI Platform Costs (Key Services)

| Service | Pricing | Our Use Case |
|---------|---------|-------------|
| Pipelines | $0.03/run + compute | Agent workflow orchestration |
| RAG Engine | Free ingestion + embedding costs | CCDC/legislation knowledge base |
| Grounding (your data) | $2.50/1,000 requests | Construction doc corpus |
| Context Caching | $1.00/M tokens/hr (Flash) | CCDC contract templates |
| Agent Builder | $0.01/vCPU-hr + $0.009/GB-hr | 5 AI agents runtime |
| Model Evaluation | Included | Accuracy benchmarking |
| Model Registry | Free | Version management |

### Google for Startups Cloud Program (AI Tier)

| Benefit | Amount |
|---------|--------|
| Year 1 credits | **$250,000** (100% of eligible usage) |
| Year 2 credits | **$100,000** (20% of eligible usage) |
| Model Garden partner credits | **$10,000** |
| Enhanced Support credits | **$12,000** |
| **Total potential** | **$372,000 over 2 years** |

*Eligibility: VC-funded startups (Seed to Series A) using Vertex AI/Gemini as foundation. SAFE agreements accepted. Munera qualifies via Centech + planned seed round.*

## 5. OCR / Document Processing (10K-50K pages/mo)

| Option | Provider | Monthly Cost | Per Page | Pros |
|--------|----------|-------------|----------|------|
| **Google Document AI** (Rec.) | GCP | **$65-$325** | $0.0015-$0.01 | Best accuracy, form parser |
| AWS Textract | AWS | $150-$750 | $0.015 | Tables + forms, AWS native |
| Azure Doc Intelligence | Azure | $100-$500 | $0.01 | Good multilingual (FR/EN) |
| Mindee | Mindee | $80-$400 | $0.008 | Developer-friendly API |
| Nanonets | Nanonets | $100-$500 | $0.01 | Custom model training |

## 6. Authentication (500-2000 MAU)

| Option | Provider | Monthly Cost | Pros | Cons |
|--------|----------|-------------|------|------|
| **Firebase Auth** (Rec. P0) | Google | **$0** (free to 50K MAU) | Free, battle-tested, Google ecosystem | Less customizable |
| Supabase Auth | Supabase | $0 (included) | Already in stack if using Supabase | Fewer providers |
| Clerk | Clerk | $20-$99 | Best DX, beautiful components | Adds cost |
| AWS Cognito | AWS | $0 (free to 50K MAU) | Free, AWS native | Terrible DX |
| Auth0 | Okta | $240-$960 | Enterprise SSO, compliance | Expensive |

## 7. Observability / Monitoring

| Option | Provider | Monthly Cost | Pros | Cons |
|--------|----------|-------------|------|------|
| **Grafana Cloud** (Rec.) | Grafana | **$0-$50** (free tier generous) | OTel native, Loki+Tempo+Mimir | Self-config needed |
| Sentry + Prometheus | Mixed | $29-$89 | Error tracking + metrics | Two tools to manage |
| AWS CloudWatch | AWS | $50-$150 | Integrated if on AWS | Expensive at scale |
| Datadog | Datadog | $200-$600 | Best-in-class, all-in-one | Very expensive |
| New Relic | New Relic | $0-$200 | 100GB/mo free, good APM | Gets expensive fast |

## 8. CI/CD Pipeline (~500 builds/month)

| Option | Provider | Monthly Cost | Pros | Cons |
|--------|----------|-------------|------|------|
| **GitHub Actions** (Rec.) | GitHub | **$0-$20** (2000 min free) | Integrated with GitHub, great ecosystem | Minutes-based billing |
| GitLab CI | GitLab | $0-$29 | Built-in, good pipeline viz | Slower runners |
| CircleCI | CircleCI | $15-$50 | Fast, good caching | Limited free tier |
| AWS CodePipeline | AWS | $1/pipeline + build costs | Deep AWS integration | Complex setup |
| Buildkite | Buildkite | $0-$50 | Bring-your-own-infra, fast | More ops overhead |

## 9. BIM Processing Server (IfcOpenShell — 8-16 vCPU, 32GB RAM)

| Option | Provider | Monthly Cost | Pros | Cons |
|--------|----------|-------------|------|------|
| **Hetzner Dedicated** (Rec.) | Hetzner | **$46-$68** (EUR) | Best price/perf, EU data centers | No managed services |
| OVH Dedicated | OVH | $60-$120 | Canadian data center (Montreal) | Support quality varies |
| AWS EC2 (c6i.2xlarge) | AWS | $200-$350 | Reliable, spot instances available | Expensive |
| Google Compute Engine | GCP | $180-$320 | Sustained-use discounts | Expensive |
| Azure VM (F8s v2) | Azure | $200-$350 | Good if Azure ecosystem | Expensive |

## 10. Message Queue / Event Bus

| Option | Provider | Monthly Cost | Pros | Cons |
|--------|----------|-------------|------|------|
| **Redis (Upstash)** (Rec.) | Upstash | **$0-$10** | Serverless, 500K cmd/mo free, queue+cache | Limited throughput |
| AWS SQS/SNS | AWS | $5-$20 | Reliable, scalable | AWS lock-in |
| Google Pub/Sub | GCP | $5-$20 | Good with GCP | GCP lock-in |
| RabbitMQ (self-hosted) | Self | $0 + server cost | Full control, AMQP | Ops overhead |
| NATS | Self/Cloud | $0-$15 | Ultra-fast, lightweight | Less tooling |

## 11. Vector Database (RAG pipeline)

| Option | Provider | Monthly Cost | Pros | Cons |
|--------|----------|-------------|------|------|
| **pgvector** (Rec.) | In PostgreSQL | **$0** (included) | No extra infra, good enough for 1M vectors | Slower than dedicated |
| Qdrant Cloud | Qdrant | $25-$100 | Fast, good filtering | Extra service |
| Pinecone | Pinecone | $70-$230 | Managed, easy API | Expensive, vendor lock |
| Weaviate Cloud | Weaviate | $25-$95 | Hybrid search, good docs | Newer |
| ChromaDB (self-hosted) | Self | $0 + server | Free, good for dev | Not production-grade |

## 12. CDN / Frontend Hosting

| Option | Provider | Monthly Cost | Pros | Cons |
|--------|----------|-------------|------|------|
| **Vercel** (Rec.) | Vercel | **$0-$20** | Best React/Next.js DX, global CDN | Vendor-specific |
| Cloudflare Pages | Cloudflare | $0-$20 | Fast, unlimited bandwidth | Fewer build features |
| Netlify | Netlify | $0-$19 | Good DX, form handling | Bandwidth limits |
| AWS CloudFront + S3 | AWS | $15-$50 | Full control | Complex setup |
| Azure Static Web Apps | Azure | $0-$9 | Free tier generous | Fewer features |

---

## References

- [Google Cloud Run Pricing](https://cloud.google.com/run/pricing)
- [Supabase Pricing](https://supabase.com/pricing)
- [Neon Pricing](https://neon.tech/pricing)
- [Cloudflare R2 Pricing](https://developers.cloudflare.com/r2/pricing/)
- [Vertex AI Pricing](https://cloud.google.com/vertex-ai/pricing)
- [Vertex AI Generative AI Pricing](https://cloud.google.com/vertex-ai/generative-ai/pricing)
- [Claude API Pricing](https://docs.anthropic.com/en/docs/about-claude/models)
- [Google for Startups AI Tier](https://cloud.google.com/startup/ai)
- [Google Document AI Pricing](https://cloud.google.com/document-ai/pricing)
- [AWS Textract Pricing](https://aws.amazon.com/textract/pricing/)
- [Firebase Pricing](https://firebase.google.com/pricing)
- [Clerk Pricing](https://clerk.com/pricing)
- [Grafana Cloud Pricing](https://grafana.com/pricing/)
- [Sentry Pricing](https://sentry.io/pricing/)
- [GitHub Pricing](https://github.com/pricing)
- [Hetzner Dedicated Servers](https://www.hetzner.com/dedicated-rootserver/)
- [Upstash Redis Pricing](https://upstash.com/pricing/redis)
- [Pinecone Pricing](https://www.pinecone.io/pricing/)
- [Vercel Pricing](https://vercel.com/pricing)
