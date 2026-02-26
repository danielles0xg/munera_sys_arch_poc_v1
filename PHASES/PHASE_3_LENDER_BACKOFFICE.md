# P3: LENDER/BACKOFFICE (Months 3-5)

## What Gets Built
The lender-facing module: CTC engine, draw risk scoring, HITL review queue, automated report generation. This is the module that directly serves the investor's workflow.

## Components

| Component | Description | Why It's Needed |
|-----------|-------------|-----------------|
| **CTC/EAC Engine** | Cost-to-Complete and Estimate-at-Completion calculations per project | Core lender analytics. Predicts if project will finish within budget. |
| **Draw Risk Scoring** | AI-powered risk score (0-100) per draw request | Flags high-risk draws before approval. 400% better detection (Built Technologies benchmark). |
| **HITL Review Queue** | Workflow: AI generates report → QS reviews → Approve/Correct/Reject → Digital signature | The "human in the loop" that maintains professional liability coverage. |
| **Report Generator** | Auto-generate Rapport de Deboursement PDF from structured data | Currently 2-4 hours manual. Target: 10-20 minutes with AI pre-fill. |
| **Interest Reserve Monitor** | Track interest reserve burn rate vs. project timeline | Warns lender when interest reserve may be exhausted before project completion. |
| **12+ Report Templates** | Disbursement, progress, budget evolution, holdback status, compliance, portfolio summary | Replaces manual Excel compilation with one-click generation. |

## Architecture Decisions

| Decision | Options | Chosen | Rationale |
|----------|---------|--------|-----------|
| Report generation | jsPDF, Puppeteer/Chrome, WeasyPrint, LaTeX | **WeasyPrint (Python)** | HTML/CSS → PDF, template engine, bilingual, server-side |
| HITL workflow | Custom, Temporal, Inngest | **Custom + Redis queue** | Simple for V1, migrate to Temporal at scale |
| Risk model | Rule-based, ML classifier, LLM scoring | **Hybrid: rules + LLM** | Rules for deterministic checks, LLM for pattern recognition |

---

## References

- [WeasyPrint](https://weasyprint.org/)
- [Upstash Redis](https://upstash.com/)
- [Temporal.io](https://temporal.io/)
- [Built Technologies](https://getbuilt.com/) — industry benchmark for draw risk scoring
