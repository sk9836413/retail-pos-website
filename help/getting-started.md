---
title: Getting started
permalink: /help/getting-started
---

# Getting started

## 1. Install

1. Install **Retail POS Pro** from AppSource into a **sandbox** first. Then install the add-on apps you need: Hospitality, India GST,
   Payment Terminals, E-Commerce. Each add-on needs Retail POS Pro.
2. Open **Extension Management**, select each app, choose **Configure** and switch on **Allow HttpClient Requests**.
   This is needed for card terminals, UPI QR, SMS / WhatsApp, e-invoicing and web stores. Sandboxes block outgoing calls until you do this.
3. Give users the permission sets: **RPOS ALL** (Retail POS Pro) plus **RPOS HOSP ALL**, **RPOS INDIA ALL**, **RPOS PAY ALL** or
   **RPOS COMM ALL** for the add-ons. Choose the **Retail Manager (POS)** role for back-office users.

## 2. Create the demo setup

1. Search for **Retail POS Setup**.
2. Choose **Create Default Setup & Demo Data**.
   This creates number series, tender types (cash, card, UPI, gift card, voucher, points, customer account), profiles, permission groups,
   POS menus, a demo store **S0001** with terminal **P0001**, staff, a loyalty club, infocodes and sample offers. Existing records are kept.

Demo staff:

| Staff ID / password | Role |
|---|---|
| 101 / 101 | Cashier |
| 500 / 500 | Supervisor (can approve) |
| 900 / 900 | Manager |

Change these passwords (**Staff → Set POS Password**) before going live.

## 3. Fill in the accounts

* **Tender Types**: set *Account Type* and *Account No.* for every tender (cash → cash G/L account, card → card clearing or bank account, …).
* **Retail POS Setup → Posting**: gift card liability, credit voucher liability, customer order deposit, rounding, statement difference
  and float accounts. Use a Gen. Prod. Posting Group and a **0% VAT** VAT Prod. Posting Group on these accounts.
* **Store card**: *Cash (Walk-in) Customer No.* (a customer with posting groups) and *Location Code*.

## 4. Make your first sale

1. Open **Retail POS** (or the **Open POS** tile on the role center). If you have more than one terminal, set a default terminal for your user in **User Setup**.
2. Log on with **101 / 101**.
3. Scan or type an item number and press Enter. Choose **Total**, then **Cash**, enter the amount, and the receipt prints.
4. In Business Central, open **POS Transactions** to see the sale.

## 5. Daily jobs

Open **Job Queue Entries**, create an entry for **codeunit 50116 RPOS Scheduled Jobs**, recurring every 15–60 minutes. It runs:
points expiry, member tier changes, web store sync, e-invoice retries and automatic statement posting (if switched on).

## 6. Go-live checklist

- [ ] Every store has a location, a cash customer and dimension values
- [ ] Every tender type has an account; card and UPI tenders tested end to end
- [ ] Staff created with their own passwords and permission groups
- [ ] Items have prices (sales price lists), barcodes (item references) and VAT / GST setup
- [ ] Receipt texts (header / footer) and the receipt layout checked on the real printer
- [ ] Hardware Bridge installed on POS PCs that use ESC/POS printers, drawers or scales
- [ ] A full day tested: sales, returns, tender declaration, Z report, statement posting, and the G/L checked by your accountant
- [ ] Backup internet connection in each store (for example a 4G router with automatic failover)
- [ ] Training mode used for staff training (training sales are never posted)
