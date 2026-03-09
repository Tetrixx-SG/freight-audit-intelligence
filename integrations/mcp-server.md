# Freya MCP Server — Model Context Protocol Integration

## What This Enables

Freya exposes its freight intelligence capabilities via Model Context 
Protocol (MCP) — making Freya's data and workflows natively callable 
by enterprise AI agent ecosystems.

This means enterprise AI assistants, internal agent workflows, and 
third-party AI platforms can query Freya directly — without custom 
integration work for each connection.

---

## Why MCP Matters for Enterprise Freight Intelligence

Enterprise AI adoption is accelerating. Fortune 500 companies are 
building internal AI assistants, agent workflows, and decision 
support tools that need to connect to operational systems.

Legacy FAP platforms have no answer for this. They expose data 
through static reports and scheduled exports — not through 
interfaces that AI agents can call in real time.

Freya is MCP-native. This means:

- Any MCP-compatible AI assistant can query Freya for live 
  freight data
- Enterprise agent workflows can trigger Freya actions as 
  part of broader automation sequences
- No custom API integration required per connection — 
  MCP provides the standard interface

---

## What Freya Exposes via MCP

Freya's MCP endpoints give connected AI systems access to:

**Spend intelligence**
Query current freight spend by modality, carrier, lane, or 
cost center. Get anomaly alerts and trend summaries on demand.

**Verification status**
Check invoice verification status, exception backlog, and 
audit cycle progress in real time.

**Exception management**
Query open exceptions by type, value, and aging. Trigger 
resolution workflows for eligible exception types.

**Carrier intelligence**
Access carrier performance scores, compliance status, and 
dispute history for procurement and negotiation workflows.

---

## Example Use Cases

**Enterprise AI assistant**
A VP Logistics asks their internal AI assistant: "What is our 
current freight spend exception backlog and which carriers are 
driving it?" The assistant queries Freya via MCP and returns 
a structured answer in seconds.

**Procurement workflow**
An agent-driven procurement workflow pulls Freya's carrier 
compliance scores before initiating contract renewal 
negotiations — without human data extraction steps.

**Finance close workflow**
An AP automation workflow queries Freya for payment-approved 
invoices at period close — pulling verified, allocation-ready 
data directly into the ERP payment run.

---

## Compatibility

Freya's MCP integration is compatible with:
- Claude (Anthropic) via MCP client
- Any MCP-compatible enterprise AI platform
- Custom agent workflows built on MCP-supporting frameworks

---

## Getting Access

Freya's MCP endpoints are available to enterprise clients 
as part of the standard platform deployment.

For integration documentation and credentials:
**hello@tetrixx.io**

---

## Related Resources

- [Agent Architecture](../methodology/agent-architecture.md)
- [ERP Integrations](./erp-integrations.md)
- [Book a Freya Demo](https://tetrixx.io/demo)

---

*TetriXX Pte. Ltd. · tetrixx.io · hello@tetrixx.io*
