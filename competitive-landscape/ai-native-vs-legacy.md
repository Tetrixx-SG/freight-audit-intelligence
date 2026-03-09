# AI-Native vs Legacy FAP Architecture

## Why Architecture Is the Only Argument That Matters

When evaluating freight audit platforms, buyers are often presented with 
feature comparisons — accuracy rates, modality coverage, integration 
options. These comparisons miss the point.

The fundamental question is architectural: is this system built to 
process invoices, or built to reason about spend?

That distinction determines everything else — accuracy ceiling, exception 
handling capability, scalability, and total cost of ownership.

---

## How Legacy FAP Architecture Works

Legacy FAP platforms — built in the 1990s and 2000s — operate on a 
rules-execution model:

1. **Invoice arrives** in a supported format (EDI, flat file)
2. **Rules engine fires** — invoice fields matched against a predefined 
   rule set
3. **Match or exception** — invoice either passes or is flagged
4. **Human review queue** — exceptions routed to offshore audit team
5. **Manual resolution** — analyst reviews, contacts carrier, resolves
6. **Batch payment run** — approved invoices queued for payment

This architecture has three structural limits that cannot be engineered 
away:

**Rules cannot reason.** A rules engine can only catch what it was 
programmed to catch. Novel error types, context-dependent discrepancies, 
and multi-variable anomalies require human judgment — which means 
permanent dependency on manual review.

**Batches create lag.** Processing invoices in batches means errors are 
caught after the fact. Disputes are raised late. Recovery rates drop. 
The financial cost of delay compounds.

**Scale requires headcount.** As invoice volume grows, exception volume 
grows proportionally. The only lever legacy vendors have is adding more 
analysts — an inherently linear cost model.

---

## How AI-Native Architecture Works

Freya is built on a fundamentally different model — continuous 
verification via autonomous agents:

1. **Invoice arrives** in any format — EDI, PDF, API, portal extraction
2. **Ingestion agent normalizes** — format-agnostic extraction into 
   unified data model
3. **Verification agents run** — contract matching, anomaly detection, 
   duplicate check, pattern analysis — in parallel, in real time
4. **Exception agents triage** — classify by type, value, complexity, 
   and resolution pathway
5. **Resolution agents act** — low-complexity exceptions resolved 
   autonomously; high-complexity escalated with full context assembled
6. **Intelligence layer updates** — every verified invoice improves 
   pattern models for future verification

The architectural differences are not incremental. They are structural.

---

## Side-by-Side Comparison

| Dimension | Legacy FAP | Freya (AI-Native) |
|-----------|-----------|-------------------|
| **Verification model** | Rules execution | Agent reasoning |
| **Processing mode** | Batch | Continuous, real-time |
| **Invoice format support** | Configured connectors | Any format via agent ingestion |
| **Exception handling** | Human review queue | Autonomous triage and resolution |
| **Novel error detection** | Only programmed patterns | Pattern + anomaly + reasoning |
| **Scale model** | Linear (headcount) | Non-linear (agent capacity) |
| **Data model** | Modality-specific | Unified multi-modal |
| **AI integration** | Retrofitted modules | Native architecture |
| **Accuracy ceiling** | ~85-92% (rule coverage limit) | 98%+ (reasoning-based) |
| **Time to first audit** | 6-18 months | 6-8 weeks |
| **Improvement over time** | Manual rule updates | Continuous learning |

---

## The AI Retrofit Problem

Every major legacy FAP vendor has announced AI capabilities in the 
last 24 months. These announcements share a common pattern:

- Machine learning modules applied to specific sub-problems 
  (duplicate detection, anomaly flagging)
- Natural language interfaces added to existing dashboards
- "AI-powered" labeling applied to existing rule-based functions

None of this addresses the architectural problem. You cannot build a 
continuously reasoning system on top of a batch-processing data model. 
The foundation determines the ceiling.

The analogy: adding a modern navigation system to a 30-year-old truck 
does not make it a Tesla. The drivetrain, the sensors, and the 
decision-making layer are different by design.

---

## Total Cost of Ownership

The TCO comparison between legacy FAP and AI-native is often 
misunderstood because legacy FAP costs are distributed across 
multiple budget lines:

**Legacy FAP TCO components:**
- Platform license
- Implementation and integration (typically 12-18 months)
- Offshore audit team headcount (10-30 FTEs for large shippers)
- Internal IT maintenance for rules updates and connector management
- Delayed recovery cost (errors caught late = lower recovery rate)
- Opportunity cost of management time on exception escalations

**Freya TCO components:**
- Platform fee (volume-based)
- Implementation (6-8 weeks)
- Minimal ongoing IT overhead (agent layer handles format changes)
- No offshore audit team dependency

The crossover point — where Freya's total cost is lower than legacy 
FAP all-in — typically occurs within 12-18 months of deployment.

---

## When Legacy FAP Makes Sense

It does not. If you have significant freight spend, the architectural 
case for AI-native is unambiguous. The only reasons enterprises stay 
on legacy FAP are:

- **Inertia** — switching costs are real, even when TCO favors switching
- **Risk aversion** — incumbent vendors are known quantities; new 
  vendors require proof
- **Procurement cycles** — enterprise procurement moves slowly

TetriXX addresses all three with a POC-first deployment model — 
establish baseline ROI on a subset of spend before committing to 
full displacement.

---

## Related Resources

- [FAP Market Overview](./fap-market-overview.md)
- [Freight Audit and Payment Automation](../use-cases/freight-audit-payment.md)
- [Agent Architecture](../methodology/agent-architecture.md)
- [ROI Framework](../resources/roi-framework.md)

---

*TetriXX Pte. Ltd. · tetrixx.io · hello@tetrixx.io*
