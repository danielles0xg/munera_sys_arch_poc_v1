# SYSTEM ARCHITECTURE

## Component Topology

```mermaid
graph TB
    Frontend["FRONTEND\nReact 19 + TypeScript\nOwner | GC | Lender | QS | Admin"]
    Gateway["API GATEWAY\nGoogle Cloud Run"]
    Backend["BACKEND API\nFastAPI\nAuth | RBAC | Multi-tenant | REST + WS"]
    VertexAI["VERTEX AI PLATFORM\nPipelines | RAG Engine | Context Caching\nAgent Builder | Model Evaluation"]
    Agents["AI AGENTS - LangGraph\nInvoice | Compliance | BIM | Schedule | Backoffice"]
    BIM["BIM SERVICE\nMCP4IFC | IfcOpenShell\nDigital Twin | Photo CV"]
    LLMs["LLM MODELS\nGemini 2.5 Flash + Pro\nClaude Sonnet via Model Garden"]
    DB["POSTGRESQL + pgvector\nProjects | Invoices | Contracts\nPayments | Holdbacks | Audit Logs"]
    Storage["CLOUDFLARE R2\nPDFs | IFC Files | Photos | Reports"]
    VectorDB["VECTOR DB - pgvector\nCCDC Docs | Legislation | Embeddings"]
    OCR["DOCUMENT AI + TEXTRACT\nOCR | Invoice Parser | Contract Parser"]
    Auth["FIREBASE AUTH"]
    Observability["GRAFANA + SENTRY\nOTel Traces | Logs | Metrics"]
    Redis["REDIS - Upstash\nMessage Queue + Cache"]

    Frontend --> Gateway
    Gateway --> Backend
    Gateway --> VertexAI
    Gateway --> BIM
    VertexAI --> Agents
    VertexAI --> LLMs
    Agents --> OCR
    Agents --> DB
    Agents --> VectorDB
    Backend --> DB
    Backend --> Storage
    Backend --> Auth
    Backend --> Observability
    BIM --> DB
    BIM --> Storage
    DB --> Redis
```

## Data Flow: Draw Request to Disbursement Report

```mermaid
graph LR
    A["GC/Borrower\nUploads Draw Request"] --> B["Document Ingestion\nOCR + Classification"]
    B --> C["Invoice Agent\nExtract + Validate + Fraud Check"]
    C --> D["BIM Agent\nProgress Verify + Photo CV"]
    D --> E["Compliance Agent\nHoldback + Prompt Pay + Liens"]
    E --> F["Backoffice Agent\nGenerate Report + Risk Score"]
    F --> G["QS/Lender Review\nApprove or Correct - HITL"]
    G --> H["Payment Released\n+ Audit Trail"]
```

---

## References

- [Google Cloud Run](https://cloud.google.com/run)
- [Vertex AI Platform](https://cloud.google.com/vertex-ai)
- [LangGraph](https://langchain-ai.github.io/langgraph/)
- [Supabase](https://supabase.com/)
- [Cloudflare R2](https://developers.cloudflare.com/r2/)
- [Google Document AI](https://cloud.google.com/document-ai)
- [Firebase Auth](https://firebase.google.com/products/auth)
- [Grafana Cloud](https://grafana.com/products/cloud/)
- [Sentry](https://sentry.io/)
- [Upstash Redis](https://upstash.com/)
