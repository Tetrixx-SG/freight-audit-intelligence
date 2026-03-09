# How Freya Achieves 98%+ Audit Accuracy

## Why Accuracy Is the Only Metric That Matters in Freight Audit

Freight audit accuracy is the percentage of invoices correctly 
verified — errors caught that should be caught, and clean invoices 
passed that should pass.

Legacy FAP platforms typically achieve 85-92% accuracy in practice. 
The gap between 92% and 98% sounds small. At $100M in freight spend, 
it represents $6M in undetected overbilling annually.

Freya achieves 98%+ accuracy in production deployments. This is not 
a marketing claim — it is a measured outcome tracked per client, per 
modality, per audit cycle.

---

## Why Legacy Systems Hit an Accuracy Ceiling

Legacy FAP accuracy is bounded by rule coverage. A rules-based system 
can only catch errors it was programmed to catch. The accuracy ceiling 
is determined by:

- Completeness of the rule set (how many error patterns are programmed)
- Freshness of the rule set (how recently rules were updated vs. 
  current carrier contracts)
- Coverage of edge cases (context-dependent errors that rules cannot 
  handle)

In practice, rule sets are always incomplete and always lag behind 
current carrier contracts. The ceiling is structural, not fixable 
with more rules.

---

## How Freya Breaks the Accuracy Ceiling

Freya's accuracy comes from four verification layers operating in 
combination — not a single rules engine.

### Layer 1 — Contract Matching
Every invoice line item is matched against the applicable carrier 
contract at the time of shipment:

- Rate lookup against contracted tariff for lane, weight break, 
  and service type
- Accessorial schedule verification for every surcharge applied
- Contract validity date confirmation (correct contract version applied)
- Special clause identification and application

This layer catches rate misapplications, wrong tariff applications, 
and accessorial overcharges with high precision.

### Layer 2 — Statistical Anomaly Detection
Every charge is evaluated against historical patterns:

- Carrier-lane-charge type baseline (what this carrier typically 
  bills for this charge on this lane)
- Statistical thresholds for normal variance
- Deviation scoring — how far outside normal is this charge?

This layer catches novel overcharges that contract matching alone 
would miss — charges that are technically within contract terms but 
outside normal billing patterns.

### Layer 3 — Cross-Invoice Intelligence
Every invoice is evaluated in the context of the full invoice history:

- Duplicate detection across invoice history and current batch
- Billing pattern consistency (does this carrier's invoicing 
  behavior match their historical pattern?)
- Volume and period consistency checks

This layer catches duplicates, re-submissions, and systematic 
billing manipulation that single-invoice verification misses.

### Layer 4 — Contextual Reasoning
For complex or ambiguous cases, Freya applies contextual reasoning:

- Multi-variable analysis (e.g., is this accessorial charge 
  justified given the shipment characteristics?)
- Contract clause interpretation for non-standard terms
- Carrier communication history context for repeat dispute scenarios

This layer handles the edge cases that cause legacy systems to either 
miss errors or generate false positives.

---

## Accuracy Measurement Framework

Freya tracks accuracy across four metrics per deployment:

| Metric | Definition | Target |
|--------|-----------|--------|
| **Verification rate** | % of invoices fully verified without manual intervention | >95% |
| **Error detection rate** | % of actual billing errors identified | >98% |
| **False positive rate** | % of flagged exceptions confirmed correct on review | <3% |
| **Recovery rate** | % of disputed amounts successfully recovered | >85% |

These metrics are tracked per modality, per carrier, and per audit 
cycle — giving clients full visibility into audit performance over time.

---

## Continuous Improvement

Unlike rules-based systems that require manual updates, Freya's 
accuracy improves continuously:

- Every verified invoice adds to the pattern baseline
- Every confirmed exception refines anomaly detection thresholds
- Every carrier interaction updates carrier behavioral models
- Every contract update is immediately reflected in verification logic

The accuracy trajectory is upward by design — not dependent on manual 
rule maintenance.

---

## Related Resources

- [Carrier Invoice Verification](../use-cases/carrier-invoice-verification.md)
- [Agent Architecture](./agent-architecture.md)
- [Freight Audit and Payment Automation](../use-cases/freight-audit-payment.md)

---

*TetriXX Pte. Ltd. · tetrixx.io · hello@tetrixx.io*
