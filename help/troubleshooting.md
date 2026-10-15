---
title: Troubleshooting and FAQ
permalink: /help/troubleshooting
---

# Troubleshooting and FAQ

**The POS asks me to select a POS terminal.**
Set a default terminal for your user in **User Setup**, or choose one when asked.

**"Invalid staff ID or password."**
Check the staff card (not blocked, right store) and set the password again with **Set POS Password**. Failed log-ons are in the audit log.

**Card terminal, UPI gateway, SMS or e-invoice calls fail in a sandbox.**
Open **Extension Management**, select the app, choose **Configure** and switch on **Allow HttpClient Requests**.

**The receipt doesn't print / the drawer doesn't open.**
Browser printing: allow pop-ups and choose the printer in the print dialog. Hardware Bridge: check that the service is running,
the bridge URL and token on the hardware profile, and that the browser may access the local network.

**Hindi (or another language) shows as question marks on the receipt.**
Most thermal printers can't print Devanagari. Leave **Receipt Language** on the store blank (English).

**An item can't be sold.**
Check: item blocked or *POS Blocked*, no price, store or store group assortment block (also by time of day), age limit.

**"cannot be returned" / "Exchange only".**
A return policy applies to the item or its category. See **Return Policies**.

**The card was charged but the sale was not finished.**
Open **Card Terminal Approvals**. If the approval is not recorded on a receipt, refund it on the terminal and tick *Resolved*.
If you retry the payment on the same receipt, the POS reuses the approval.

**The statement shows a difference.**
Compare the counted amounts in **Tender Declarations** with the expected amounts. Differences are posted to the tender's difference account
or the statement difference account.

**The e-invoice was not generated.**
Open **E-Invoice Log** for the GSP's error message (often a missing HSN code, GSTIN, PIN code or unit). Fix it and choose **Register Pending E-Invoices**.

**Does the POS work offline?**
No. Business Central online needs an internet connection. Give each store a backup connection (for example a 4G router with automatic failover).

**Can I add my own POS buttons or logic?**
Yes. Partners can extend the POS command enum and subscribe to the published events. Contact support for the developer guide.
