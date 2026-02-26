# P6: INTEGRATIONS (Months 6-8)

## What Gets Built
Connect Munera to the tools their clients already use: Procore, SAP, QuickBooks, banking APIs.

## Components

| Component | Description | Why It's Needed |
|-----------|-------------|-----------------|
| **Procore API Connector** | Sync projects, budgets, change orders, RFIs from Procore | Most large GCs use Procore. Data must flow both ways. |
| **SAP Business One Connector** | Sync cost centers, POs, invoices from SAP | Mid-market GCs use SAP for accounting. |
| **QuickBooks Online Connector** | Sync invoices, payments, chart of accounts | Small-mid GCs and subs use QBO. |
| **Banking API (Plaid/Flinks)** | Bank account verification, payment status confirmation | Verify that payments actually cleared. |
| **Outlook/Email Integration** | Parse incoming emails for documents, auto-attach to projects | Documents arrive by email. Auto-ingest reduces manual upload. |
| **Webhook Framework** | Generic webhook system for any future integration | Extensibility without custom code per integration. |

---

## References

- [Procore API](https://developers.procore.com/)
- [SAP Business One SDK](https://developers.sap.com/topics/business-one.html)
- [QuickBooks Online API](https://developer.intuit.com/app/developer/qbo/docs/get-started)
- [Plaid API](https://plaid.com/docs/)
- [Flinks API](https://docs.flinks.com/)
- [Microsoft Graph API (Outlook)](https://learn.microsoft.com/en-us/graph/)
