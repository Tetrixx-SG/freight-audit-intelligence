# Carrier Invoice Verification

## The Core Problem

Carrier invoices are the primary source of financial leakage in enterprise 
freight spend. Across ocean, air, land, and courier modalities, billing 
errors are systematic — not exceptional.

Common error types by modality:

**Ocean freight**
- Incorrect base freight rates vs. contracted tariffs
- Bunker Adjustment Factor (BAF) miscalculations
- Port surcharge overcharges
- Container demurrage and detention overbilling
- Weight and measurement discrepancies

**Air freight**
- Rate misapplication across weight breaks
- Fuel surcharge calculation errors
- Airport handling fee overcharges
- Dimensional weight vs. actual weight disputes

**Land / road transport**
- Accessorial overcharges (fuel surcharge, liftgate, residential delivery)
- Rate misapplication across lanes
- Duplicate invoice submission
- Incorrect stop-off charges

**Courier / small parcel**
- Dimensional weight overcharges
- Zone misclassification
- Surcharge stacking (multiple fees applied incorrectly)
- Service level billing vs. actual service delivered

---

## Why Rules-Based Verification Fails

Legacy FAP platforms verify invoices against static rule sets. This works 
for known, recurring error patterns — but fails in three critical ways:

**Coverage gap:** Novel error types are not caught until a rule is written. 
Rule creation is manual, slow, and reactive.

**Context blindness:** Rules cannot reason about context. A fuel surcharge 
that is correct for one lane may be incorrect for another under a different 
contract clause. Rules treat all invoices identically.

**Maintenance burden:** As carrier contracts change, rule sets must be 
manually updated. In large enterprises with hundreds of carrier contracts, 
this creates permanent lag between contract reality and audit capability.

---

## How Freya Verifies Carrier Invoices

Freya approaches invoice verification as an intelligence problem, not a 
rules execution problem.

### Step 1 — Ingestion and Normalization
Invoices arrive in any format: EDI 210, PDF, carrier portal extract, API 
feed. Freya's ingestion layer normalizes all formats into a unified data 
structure — extracting line items, charges, references, and metadata 
regardless of source format.

### Step 2 — Contract Matching
Each invoice line item is matched against the applicable carrier contract:
- Rate lookup against contracted tariff for the specific lane, weight, 
  and service type
- Accessorial schedule verification for each surcharge applied
- Contract validity date confirmation
- Special clause identification (e.g., volume commitments, seasonal rates)

### Step 3 — Anomaly Detection
Beyond contract matching, Freya applies pattern intelligence:
- Historical billing comparison for the same carrier, lane, and charge type
- Statistical anomaly detection for charges outside expected ranges
- Duplicate detection across invoice history and current batch
- Carrier-specific behavioral patterns (known billing tendencies)

### Step 4 — Discrepancy Classification
Identified discrepancies are classified by:
- Error type (rate misapplication, duplicate, accessorial overcharge, etc.)
- Financial value
- Recovery probability
- Dispute complexity

This classification drives autonomous resolution vs. human escalation routing.

---

## Verification Coverage

| Verification Type | Coverage |
|------------------|----------|
| Rate contract matching | All modalities, all line items |
| Accessorial verification | All standard and contract-specific surcharges |
| Duplicate detection | Cross-invoice, cross-period |
| Anomaly detection | Statistical + pattern-based |
| Weight/measurement verification | Where shipment data available |
| Service level verification | Where tracking data available |

---

## Accuracy and Performance

Freya achieves 98%+ verification accuracy across production deployments.

Key performance metrics tracked:
- **Verification rate:** % of invoices fully verified without manual intervention
- **Exception rate:** % of invoices flagged for discrepancy
- **False positive rate:** % of flagged exceptions confirmed correct on review
- **Recovery rate:** % of disputed amounts successfully recovered from carriers

---

## Related Resources

- [Freight Audit and Payment Automation](./freight-audit-payment.md)
- [Agentic Exception Management](./freight-audit-payment.md#agentic-exception-management)
- [Audit Accuracy Methodology](../methodology/audit-accuracy.md)
- [Carrier Connectivity](../integrations/carrier-connectivity.md)

---

*TetriXX Pte. Ltd. · tetrixx.io · hello@tetrixx.io*
