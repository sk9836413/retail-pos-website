---
title: Reports and Power BI
permalink: /help/reports
---

# Reports and Power BI

## In Business Central

| Report / page | Shows |
|---|---|
| **POS Sales Analysis (Excel)** | Sales grouped by store, date, item, item category, staff, tender or hour, exported to Excel |
| **Z Report History (Excel)** | Every Z report with totals per tender |
| **POS Sales by Item / Staff / Store & Date / Tender** | Analysis queries you can open in Excel |
| **Offer Performance** | Sales and discount per offer |
| **Staff Performance** | Sales, transactions, average basket, discounts, voids, hours, sales per hour and commission |
| **Sales Budgets** | Budget vs. actual per store and day |
| **POS Transactions**, **Sales Entries**, **Payment Entries** | Every receipt and line |
| **POS Audit Log** | Voids, price overrides, discounts, drawer openings, approvals |

India GST reports are described in [India GST](india-gst).

## Power BI

Retail POS Pro publishes read-only data feeds for Power BI, Excel and Fabric under `knack/retailPosAnalytics/v1.0`:
`posSalesLines`, `posReceipts`, `posPayments`, `posDiscounts`, `posStores`, `posStaff`.

In Power BI Desktop: **Get Data → Dynamics 365 Business Central**, sign in, then choose your environment and company,
**Advanced APIs → knack/retailPosAnalytics/v1.0**. The PowerBI guide in the download package has the data model, a date table and
ready-made DAX measures (sales, net sales, average basket, returns %, growth vs. last year, sales per cover, GST collected).
