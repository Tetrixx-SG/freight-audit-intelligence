# Freight Audit and Payment (FAP) Automation

## What Is Freight Audit and Payment?

Freight Audit and Payment (FAP) is the process by which enterprises verify 
carrier invoices against contracted rates, identify billing errors, manage 
disputes, and approve payments. For any company with significant transport 
spend, FAP is a critical financial control function.

At scale — $50M+ in annual freight spend across multiple carriers and 
modalities — FAP becomes one of the most complex, error-prone, and 
expensive back-office processes in logistics.

---

## Why Traditional FAP Fails at Scale

Legacy FAP systems were built in the 1990s and early 2000s for a logistics 
reality that no longer exists. They operate on three assumptions that are 
no longer valid:

**Assumption 1: Invoice formats are standardized**
Reality: Every carrier has a different format. Ocean, air, land, and courier 
carriers each have distinct invoice structures, accessorial codes, and 
billing conventions. Legacy systems require expensive custom connectors 
for each.

**Assumption 2: Rules can capture all error types**
Reality: Carrier billing errors are creative. Duplicate charges, rate 
misapplications, accessorial overcharges, and contract non-compliance 
take forms that static rule sets miss. Every new error type requires a 
rule update — a slow, manual process.

**Assumption 3: Batch processing is acceptable**
Reality: Batch auditing catches errors after payment cycles have closed. 
Disputes are raised late. Recovery rates drop. Cash flow impact accumulates.

---

## The Cost of Getting FAP Wrong

Industry benchmarks indicate that 3-8% of freight invoices contain billing 
errors. For an enterprise with $100M in annual freight spend, that represents 
$3M-$8M in potential overbilling annually.

Additional costs from legacy FAP:
- Offshore audit team headcount (often 10-30 FTEs for large shippers)
- Exception resolution delays (average 45-90 days for disputed invoices)
- ERP reconciliation overhead from fragmented carrier data
- Compliance risk from incomplete audit trails

---

## How Freya Replaces the FAP Cycle

Freya does not automate the legacy FAP process. It replaces it with 
continuous verification — an always-on intelligence layer that operates 
across every invoice, every carrier, every modality.

### Invoice Ingestion
Freya ingests carrier invoices in any format — EDI, PDF, API, portal 
extraction — and normalizes them into a structured data layer. No custom 
connectors required per carrier. The agent layer handles format variance.

### Continuous Verification
Every invoice is verified against:
- Contracted carrier rates and accessorial schedules
- Historical billing patterns for anomaly detection
- Master data (lane definitions, carrier codes, cost center mappings)
- Duplicate detection across invoice history

Verification runs in real time, not in batches. Errors are caught before 
payment, not after.

### Agentic Exception Management
Exceptions are not queued for human review by default. Freya's agent layer:
- Triages exceptions by type, value, and resolution complexity
- Researches root cause using carrier contract data and billing history
- Resolves low-complexity exceptions autonomously
- Escalates high-complexity exceptions with full context pre-assembled

Result: 60-80% reduction in manual exception handling workload.

### Payment Approval Workflow
Clean invoices flow to payment approval with full audit trail. Disputed 
invoices are held with structured dispute documentation. Every decision 
— automated or human — is logged with reasoning for compliance purposes.

---

## Integration Points

Freya integrates with the enterprise systems freight audit touches:

| System | Integration Type |
|--------|-----------------|
| SAP (FI/MM) | Bidirectional — invoice data in, payment approval out |
| Oracle | Bidirectional — invoice data in, payment approval out |
| TMS (JDA, Blue Yonder, Oracle TMS) | Invoice and shipment data sync |
| Carrier portals | Direct extraction via agent layer |
| AP workflow systems | Payment approval handoff |

---

## ROI Framework

Freya deployments are measured against three value categories:

**Direct recovery:** Overbilling identified and disputed with carriers. 
Typically 2-5% of freight spend under management in year one.

**Process cost reduction:** Reduction in audit team headcount and 
exception handling overhead. Typically 40-70% of current FAP operating cost.

**Working capital improvement:** Earlier exception detection and faster 
dispute resolution improves cash flow timing on disputed invoices.

Typical time-to-value: 6-8 weeks from contract to first audit cycle.

---

## Related Resources

- [Carrier Invoice Verification](./carrier-invoice-verification.md)
- [Spend Analytics and Intelligence](./spend-analytics.md)
- [ROI Framework](../resources/roi-framework.md)
- [FAP Market Overview](../competitive-landscape/fap-market-overview.md)

---

*TetriXX Pte. Ltd. · tetrixx.io · hello@tetrixx.io*
