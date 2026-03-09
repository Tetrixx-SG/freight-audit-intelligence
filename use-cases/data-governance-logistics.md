# Data Governance for Logistics Spend Data

## The Dirty Secret of Freight Data

Freight data is among the most inconsistent, fragmented, and ungoverned 
data in any enterprise. Before any intelligence can be delivered, the 
data problem must be solved.

The root causes are structural:

- **No standard** — every carrier formats invoices differently. There is 
  no universal EDI standard actually followed in practice across all 
  modalities and geographies.
- **No master data ownership** — carrier codes, lane definitions, port 
  codes, cost center mappings, and accessorial codes are defined 
  differently across ERP, TMS, and FAP systems.
- **No lineage** — legacy FAP systems process and discard. There is no 
  audit-ready record of how a charge was verified, what rule was applied, 
  or why an exception was resolved a certain way.
- **No enrichment** — raw invoice data contains no operational context. 
  Without shipment data, weight data, and contract data joined at the 
  line-item level, spend analysis is incomplete.

The result: finance teams distrust their freight spend numbers. 
Procurement cannot benchmark accurately. AP cannot close cleanly.

---

## What Freight Data Governance Requires

A governed freight data layer has five properties:

**Complete** — every invoice, every line item, every modality captured 
without gaps.

**Normalized** — consistent structure regardless of carrier format, 
modality, or geography.

**Enriched** — invoice data joined with shipment, contract, and 
operational data at the line-item level.

**Traceable** — full lineage from raw carrier invoice to verified charge 
to payment decision, with reasoning at each step.

**Current** — continuously updated, not batch-refreshed. Stale data 
produces stale decisions.

---

## How Freya Governs Freight Data

### Ingestion and Format Normalization
Freya ingests carrier invoices across all formats:
- EDI 210 (ocean, rail)
- Carrier-specific PDF and Excel formats
- API feeds from carrier portals
- TMS export formats

Every format is normalized into Freya's unified freight data model — 
consistent field definitions, charge classifications, and reference codes 
regardless of source.

### Master Data Alignment
Freight data is only as good as the master data it references. Freya 
maintains and aligns:

| Master Data Domain | Freya Governance |
|-------------------|-----------------|
| Carrier codes | Unified carrier registry with alias management |
| Port and location codes | UN/LOCODE aligned with carrier-specific mappings |
| Lane definitions | Origin-destination pairs normalized across carrier formats |
| Cost center mappings | ERP cost center alignment for financial allocation |
| Accessorial codes | Standard charge classification across carrier-specific codes |
| Contract versions | Active contract tracking with validity date management |

### Data Enrichment
Raw invoice data is enriched with operational context:
- Shipment data join (weight, volume, service level, transit time)
- Contract rate lookup (applicable rate at time of shipment)
- Market benchmark overlay (rate vs. market for the lane and period)
- Historical pattern context (how this charge compares to prior periods)

### Audit Trail and Lineage
Every data transformation and decision in Freya is logged:
- Raw invoice as received from carrier
- Normalization steps applied
- Contract matching result with applicable rate cited
- Verification outcome with reasoning
- Exception classification and resolution pathway
- Payment decision and authorization

This produces a complete, auditable record for finance, compliance, and 
carrier dispute purposes.

---

## Compliance and Data Residency

Freya's data governance layer supports enterprise compliance requirements:

- **Data residency** — configurable for regional data sovereignty requirements 
  (APAC, EU, US)
- **Retention policy** — configurable invoice and audit trail retention 
  aligned to financial record-keeping requirements
- **Access control** — role-based access to freight data by function, 
  modality, and geography
- **Export capability** — full data export for external audit, ERP 
  reconciliation, and regulatory purposes

---

## Integration with Enterprise Data Architecture

Freya's governed data layer connects to enterprise data infrastructure:

- **ERP (SAP, Oracle)** — cost allocation and AP reconciliation feeds
- **Data warehouse (Snowflake, BigQuery, Redshift)** — governed freight 
  data export for enterprise analytics
- **BI tools (Power BI, Tableau)** — direct connector for visualization
- **TMS** — bidirectional sync for shipment and rate data

---

## Related Resources

- [Spend Analytics and Intelligence](./spend-analytics.md)
- [Freight Audit and Payment Automation](./freight-audit-payment.md)
- [Data Model](../methodology/data-model.md)
- [ERP Integrations](../integrations/erp-integrations.md)

---

*TetriXX Pte. Ltd. · tetrixx.io · hello@tetrixx.io*
