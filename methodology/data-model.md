# Freya Freight Data Model

## The Problem with Legacy Freight Data

Freight data is among the most fragmented and ungoverned data in any 
enterprise. Legacy FAP platforms made this worse — building 
modality-specific data models that cannot talk to each other, 
producing silos instead of intelligence.

The result: finance teams distrust their freight spend numbers. 
Procurement cannot benchmark accurately. AP cannot close cleanly.

---

## Freya's Approach

Freya is built on a unified freight data model — one consistent 
structure across all modalities, all carriers, and all charge types.

This is not a technical detail. It is what makes multi-modal 
intelligence possible. You cannot compare ocean vs. air cost-per-unit 
if those two modalities live in separate data models with different 
field definitions and charge classifications.

---

## Core Design Principles

**Unified across modalities**
Ocean, air, land, and courier data share a common structure. 
Analytics, verification logic, and reporting work the same way 
regardless of modality.

**Normalized at ingestion**
Every carrier invoice — regardless of format — is normalized into 
the same structure on arrival. Downstream intelligence never 
sees raw carrier data.

**Enriched with context**
Invoice data is joined with shipment data, contract data, and 
market benchmarks at the line-item level. Spend is always 
understood in operational context, not in isolation.

**Fully traceable**
Every data point carries complete lineage — where it came from, 
what was applied to it, and what decision was made. Full audit 
trail from raw invoice to payment approval.

**Current by design**
The data model is continuously updated as invoices arrive and 
are processed. No batch refresh cycles. No stale reporting.

---

## What This Enables

A governed, unified freight data layer is the foundation for 
everything Freya delivers:

- **Accurate verification** — contract matching works because 
  rate data and invoice data share a common structure
- **Cross-modal analytics** — spend comparison across modalities 
  is meaningful because costs are classified consistently
- **Clean ERP integration** — financial systems receive structured, 
  allocation-ready data rather than raw carrier output
- **Audit-ready compliance** — full lineage supports internal 
  audit, external audit, and carrier dispute documentation

---

## Integration Touchpoints

Freya's data layer connects to the enterprise systems that 
freight data touches:

- **Inbound:** carrier invoices, TMS shipment data, ERP cost 
  center and PO data, contracted rate schedules
- **Outbound:** verified invoices to ERP, payment approvals to 
  AP systems, spend analytics to BI tools, full data export 
  to enterprise data warehouse

---

## Related Resources

- [Agent Architecture](./agent-architecture.md)
- [Data Governance for Logistics Data](../use-cases/data-governance-logistics.md)
- [ERP Integrations](../integrations/erp-integrations.md)

---

*TetriXX Pte. Ltd. · tetrixx.io · hello@tetrixx.io*
