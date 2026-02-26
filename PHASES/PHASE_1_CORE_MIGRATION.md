# P1: CORE MIGRATION (Months 1-3)

## What Gets Built
Migrate 30+ React components from client-only prototype to real backend. Multi-tenant database with RBAC.

## Components

| Component | Description | Why It's Needed |
|-----------|-------------|-----------------|
| **Firebase Auth Integration** | Email/password + Google SSO + role mapping | Can't have multi-user without auth. Firebase is free to 50K MAU. |
| **RBAC Middleware** | Role-based access control: Owner, GC, Lender, Architect, Engineer, Sub, Reviewer, Admin | Each persona sees different data. Security boundary. |
| **Multi-Tenant DB Schema** | Tenant isolation via `organization_id` on all tables | Different QS firms / lender clients share platform but see only their data. |
| **Component Migration** | 30+ React components refactored to use API calls instead of localStorage | The entire frontend currently fakes persistence. This makes it real. |
| **Bilingual Support** | FR/EN i18n framework with DB-backed translations | Quebec requires French. Already in demo but needs server-side support. |

## Architecture Decisions

| Decision | Options | Chosen | Rationale |
|----------|---------|--------|-----------|
| Auth | Firebase, Clerk, Supabase Auth, Auth0 | **Firebase Auth** | Free, fast, Google ecosystem aligned, upgrade to Clerk or Auth0 at scale |
| Multi-tenancy | Schema per tenant, Row-level security, Shared with org_id | **Row-level security (RLS)** | Supabase/PG native RLS. No schema bloat. Secure by default. |
| State management | React Query, SWR, Redux | **React Query (TanStack)** | Server-state caching, auto-refetch, mutation lifecycle |

## Deliverables Checklist
- [ ] All 8 persona dashboards loading real data from API
- [ ] Role-based access: lender can't see what admin sees
- [ ] Multi-tenant: Firm A and Firm B data fully isolated
- [ ] Search/filter/sort on all list views
- [ ] Bilingual toggle working with server-backed strings

---

## References

- [Firebase Auth](https://firebase.google.com/products/auth)
- [Firebase Pricing](https://firebase.google.com/pricing)
- [Supabase Row Level Security](https://supabase.com/docs/guides/auth/row-level-security)
- [TanStack Query (React Query)](https://tanstack.com/query)
- [Clerk Auth](https://clerk.com/pricing)
