# P0: FOUNDATION (Months 1-2)

## What Gets Built
The technical backbone that everything else depends on. No AI, no BIM yet — just the plumbing.

## Components

| Component | Description | Why It's Needed |
|-----------|-------------|-----------------|
| **Backend API** | Python/FastAPI server with REST + WebSocket endpoints | Currently zero backend — all client-side. Can't have multi-user, auth, or data persistence without this. |
| **PostgreSQL Database** | Multi-tenant schema: projects, invoices, contracts, payments, users, audit_logs | Replaces browser localStorage. Enables real queries, relationships, RBAC. |
| **Object Storage** | S3-compatible bucket for PDFs, photos, IFC files | Documents need persistent, secure, scalable storage. |
| **Observability** | OpenTelemetry SDK + Grafana (traces, logs, metrics) | Can't debug, optimize, or prove reliability without telemetry from day 1. |
| **CI/CD Pipeline** | GitHub Actions: lint → test → build → deploy (staging + prod) | Automated, repeatable deployments. No manual SSH. |
| **Docker + Infrastructure-as-Code** | Dockerfiles + Terraform/Pulumi for all infra | Reproducible environments. One-command deploy. |

## Architecture Decisions

| Decision | Options Considered | Chosen | Rationale |
|----------|-------------------|--------|-----------|
| Language | Python, TypeScript (Node), Go | **Python/FastAPI** | AI/ML ecosystem (LangGraph, IfcOpenShell), team expertise, async support |
| DB | PostgreSQL, MongoDB, CockroachDB | **PostgreSQL + pgvector** | Relational + vector in one DB, ACID, ecosystem |
| Hosting | Cloud Run, ECS, Railway, K8s | **Google Cloud Run** (P0-P5), then evaluate | Pay-per-request, auto-scale to 0, cheapest at low volume |
| IaC | Terraform, Pulumi, CDK | **Terraform** | Industry standard, multi-cloud, largest community |

## Deliverables Checklist
- [ ] FastAPI server running on Cloud Run with health checks
- [ ] PostgreSQL schema deployed (migrations via Alembic)
- [ ] File upload endpoint → Cloudflare R2
- [ ] OpenTelemetry instrumented on all API routes
- [ ] CI/CD: push to main → auto-deploy to staging
- [ ] API documentation (OpenAPI/Swagger) generated

---

## References

- [FastAPI](https://fastapi.tiangolo.com/)
- [Google Cloud Run](https://cloud.google.com/run)
- [PostgreSQL + pgvector](https://github.com/pgvector/pgvector)
- [Cloudflare R2](https://developers.cloudflare.com/r2/)
- [OpenTelemetry](https://opentelemetry.io/)
- [Grafana Cloud](https://grafana.com/products/cloud/)
- [GitHub Actions](https://github.com/features/actions)
- [Terraform](https://www.terraform.io/)
- [Alembic Migrations](https://alembic.sqlalchemy.org/)
