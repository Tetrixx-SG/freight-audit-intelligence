# Carrier Invoice Connectivity

## How Invoice Data Reaches Freya

Freya receives carrier invoice data from the enterprise — 
not from carriers directly. This reflects how freight billing 
actually works: invoices arrive at the enterprise from carriers 
through existing channels, and Freya processes them from there.

This means no carrier negotiation is required to get started. 
Freya works with what the enterprise already receives.

---

## Supported Ingestion Methods

Freya accepts carrier invoice data in any format the enterprise 
currently receives:

- Email attachments (PDF, Excel, flat files)
- ERP and TMS exports
- EDI feeds already flowing into enterprise systems
- Portal export files from carrier billing platforms
- Direct file transfer from enterprise document management systems

All formats are normalized into Freya's unified data model 
at ingestion — downstream verification and analytics work 
consistently regardless of source format.

---

## Direct Carrier Integration

Where carriers support it and the enterprise prefers it, 
Freya can connect directly to carrier billing systems — 
bypassing the manual forwarding step entirely.

This is configured case-by-case based on carrier capability 
and enterprise preference. It is not a requirement to get 
started.

---

## Modality Coverage

**Ocean freight**
Full coverage of ocean carrier invoice structures — base 
freight, bunker, port surcharges, origin and destination 
charges, demurrage and detention.

**Air freight**
International and domestic air freight carriers. Weight 
break rate verification, fuel surcharge calculation, and 
airport handling charges.

**Land / road transport**
Full truckload (FTL), less-than-truckload (LTL), and 
intermodal. Lane-based rate verification and accessorial 
charge coverage.

**Courier / small parcel**
Major global and regional courier carriers. Dimensional 
weight verification, zone classification, and surcharge 
stack coverage.

---

## Carrier Intelligence Layer

Freya builds a carrier intelligence layer as invoices 
are processed:

- Invoice accuracy scoring per carrier
- Billing pattern baselines for anomaly detection
- Dispute history and resolution outcome tracking
- Contract compliance monitoring over time

---

## Related Resources

- [ERP and System Integrations](./erp-integrations.md)
- [MCP Server Documentation](./mcp-server.md)
- [Carrier Invoice Verification](../use-cases/carrier-invoice-verification.md)

---

*TetriXX Pte. Ltd. · tetrixx.io · hello@tetrixx.io*
