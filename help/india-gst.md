---
title: India GST
permalink: /help/india-gst
---

# India GST, e-invoice and e-way bill

Requires the **Retail POS Pro - India GST** app.

## GST on the POS

1. **Retail POS Setup**: switch on **India GST Enabled**. Fill in the CGST, SGST/UTGST, IGST and cess payable accounts, and a
   **VAT Prod. Posting Group with 0%** used on the statement sales documents, so the GST is posted only to the GST accounts.
2. **GST Groups**: GST % and compensation cess % (for example 5, 12, 18, 28 + cess).
3. **Items**: GST group and HSN/SAC code.
4. **Stores**: GSTIN and 2-digit GST state code (for example 27 Maharashtra).
5. **Customers**: GSTIN. A customer from another state gets IGST instead of CGST + SGST (place of supply).

Prices on the POS include GST. Receipts print as **TAX INVOICE** (or **CREDIT NOTE** for returns) with the store GSTIN, customer GSTIN,
place of supply and an HSN-wise GST summary. Statement posting books the GST to the payable accounts.

## E-invoice (IRN)

E-invoicing is for B2B sales (customer with GSTIN) if your turnover requires it.

1. Get API access from a GST Suvidha Provider (GSP). ClearTax is built in; other GSPs that accept the NIC JSON work through *Generic GSP*.
2. **GST E-Invoice Setup**: *Enabled*, provider, environment (sandbox / production), owner ID / user name, and **Set API Token / Secret**.
   For a generic GSP also fill in the URLs and the response paths.
3. Switch on **Generate IRN when the sale is finished**.

When a B2B sale finishes, the IRN is generated and the **IRN, Ack No., Ack Date and signed QR code** print on the receipt.
If the GSP can't be reached, the receipt prints without it and the job queue retries (**Register Pending E-Invoices**).
**E-Invoice Log** shows every request. On the transaction card: **Cancel E-Invoice** (within 24 hours) and **Generate E-Way Bill**
(distance, transport mode, vehicle number or transporter GSTIN).

A receipt that mixes sold and returned items can't be e-invoiced; issue the return separately.

## Returns and reports

| Report | Use |
|---|---|
| **GSTR-1 Export (JSON)** | JSON for the GST offline tool / portal: B2B, B2C large, B2C small, credit notes, HSN summary (B2B and B2C), documents issued |
| **GSTR-3B Summary (Excel)** | Table 3.1 (taxable outward supplies, nil rated / exempt) and 3.2 (inter-state supplies to unregistered persons) |
| **GST Sales Register (Excel)** | Every POS invoice with taxable value, CGST, SGST, IGST and cess |
| **GST B2B Invoices**, **GST HSN Summary** | On-screen lists for checking |

Filter by GSTIN when a company has several registrations. Check the figures with your tax adviser before filing.
