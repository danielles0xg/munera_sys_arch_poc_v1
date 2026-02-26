# P4: COMPLIANCE/CLOCK (Months 3-5)

## What Gets Built
Provincial holdback engine and prompt payment statutory clock. **This is the Sept 2026 Quebec deadline feature.**

## Components

| Component | Description | Why It's Needed |
|-----------|-------------|-----------------|
| **Provincial Holdback Engine** | Automatic calculation per jurisdiction: ON 10%/60-day, AB 10%/90-day, BC 10%, QC legal hypothec | 2-5% manual error rate → 0%. $200K-$500K lien liability eliminated. |
| **Prompt Payment Clock** | Statutory deadline tracker: invoice date → response deadline → payment deadline → interest accrual | Quebec Sept 2026 mandate. No tooling exists in Canada. |
| **Non-Payment Notice Generator** | Auto-generate statutory notices when deadlines are missed | Legal compliance requirement under prompt payment legislation. |
| **CCDC RAG Pipeline** | Ingest CCDC 2, 5A, 5B, 17, 30 (2025 editions) + provincial lien acts | Compliance Agent answers: "What are holdback conditions for this ON project under CCDC 2?" |
| **Jurisdiction Selector** | Pluggable module: select province → loads correct rules, rates, deadlines | Multi-provincial firms need one system, many rule sets. |

## Jurisdiction Rule Matrix

| Province | Holdback % | Lien Period | Prompt Payment | Special Rules |
|----------|-----------|-------------|----------------|---------------|
| **Quebec** | Legal hypothec (different mechanism) | 30 days | **Sept 2025 >$750K, Sept 2026 >$75K** | Civil Code based, not lien act |
| **Ontario** | 10% | 60 days | **Jan 2026 (in force)** | RFT milestone, mandatory adjudication |
| **British Columbia** | 10% | 45 days | **2026 (pending)** | 28-day owner pay, 7-day contractor-to-sub |
| **Alberta** | 10% | 90 days | In force | Prompt Payment and Construction Lien Act |
| **Manitoba** | 7.5% | 40 days | **April 2025 (in force)** | Builders' Liens Amendment Act |
| **Saskatchewan** | 10% | 60 days | Under review | Builders' Lien Act |

---

## References

- [CCDC Contracts](https://www.ccdc.org/resources/contracts/)
- [Quebec Prompt Payment Legislation](https://www.quebec.ca/en/government/policies-orientations/prompt-payment)
- [Ontario Construction Act (Prompt Payment)](https://www.ontario.ca/laws/statute/90c30)
- [Alberta Prompt Payment and Construction Lien Act](https://www.alberta.ca/prompt-payment-and-construction-lien-act)
- [Manitoba Builders' Liens Amendment Act](https://web2.gov.mb.ca/laws/statutes/ccsm/b091e.php)
