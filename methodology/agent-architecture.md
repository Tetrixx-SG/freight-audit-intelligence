# Freya Agent Architecture — Connected Brains Framework

## Why Multi-Agent Architecture Matters for Freight Intelligence

Freight audit is not a single problem. It is a collection of distinct 
reasoning tasks that must operate in parallel, at scale, across 
heterogeneous data:

- Format normalization (different for every carrier)
- Contract matching (different for every modality)
- Anomaly detection (requires statistical and pattern reasoning)
- Exception triage (requires classification and routing logic)
- Exception resolution (requires carrier context and negotiation logic)
- Intelligence delivery (requires synthesis and summarization)

A single model or rules engine cannot handle this well. A coordinated 
system of specialized agents can.

This is the architectural principle behind Freya — what we call the 
Connected Brains framework.

---

## The Connected Brains Framework

Freya operates across four intelligence pillars that work in 
coordination:

### Pillar 1 — Directives
Strategic rules and audit policies that govern how Freya operates.

- Client-specific audit policies (which error types to prioritize, 
  which carriers to scrutinize more closely, dispute thresholds)
- Modality-specific verification standards
- Exception escalation rules (what gets resolved autonomously vs. 
  escalated to human review)
- Payment approval policies

Directives are the governance layer — they ensure Freya operates 
within the boundaries the client defines.

### Pillar 2 — Role Context
Domain knowledge about carriers, contracts, and modality specifics.

- Active carrier contracts with rate schedules and accessorial terms
- Carrier behavioral profiles (known billing tendencies, dispute 
  history, response patterns)
- Modality-specific knowledge (ocean surcharge structures, air weight 
  break conventions, parcel zone definitions)
- Market rate benchmarks for lane and modality benchmarking

Role Context is what makes Freya's verification intelligent rather 
than mechanical — it knows what correct looks like for each carrier 
and modality.

### Pillar 3 — Current State
Live operational data — invoices, discrepancies, resolution queues.

- Invoice ingestion queue (invoices awaiting verification)
- Active discrepancy register (identified errors pending resolution)
- Dispute tracker (open disputes with carriers, status, and aging)
- Payment approval queue (verified invoices awaiting payment)
- Exception escalation queue (items requiring human judgment)

Current State is the operational heartbeat — the live data layer 
that agents act on continuously.

### Pillar 4 — Deep Knowledge
Historical patterns, carrier benchmarks, market rate intelligence.

- Invoice history and verified charge baselines by carrier and lane
- Anomaly detection models trained on client-specific billing patterns
- Carrier dispute outcome history (what arguments win, with which 
  carriers, on which charge types)
- Market rate intelligence for benchmarking contracted rates against 
  actuals

Deep Knowledge is what makes Freya improve over time — every verified 
invoice, every resolved exception, and every carrier interaction 
enriches the models.

---

## Agent Specialization

Within the Connected Brains framework, Freya deploys specialized 
agents for each task domain:

| Agent Type | Function |
|-----------|----------|
| **Ingestion Agent** | Invoice format normalization across all carrier types |
| **Verification Agent** | Contract matching and discrepancy identification |
| **Anomaly Agent** | Statistical and pattern-based anomaly detection |
| **Triage Agent** | Exception classification and routing |
| **Resolution Agent** | Autonomous exception resolution for low-complexity cases |
| **Intelligence Agent** | Spend analytics synthesis and insight delivery |
| **Communication Agent** | Carrier dispute communication and follow-up |

Each agent is specialized for its task and operates on the relevant 
subset of the Connected Brains data layer.

---

## Orchestration

Agent coordination is managed by an orchestration layer that:

- Routes invoices through the verification pipeline in the correct 
  sequence
- Manages agent handoffs when a task requires multiple agent types
- Tracks state across multi-step resolution workflows
- Escalates to human review when agent confidence falls below threshold
- Logs all agent decisions with reasoning for audit trail purposes

---

## Model Agnosticism

Freya's agent architecture is designed to be model-agnostic. The 
orchestration layer and agent interfaces are decoupled fr
