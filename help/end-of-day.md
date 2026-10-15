---
title: End of day
permalink: /help/end-of-day
---

# End of day

## On the POS

1. **Remove Tender**: take out the cash above the next day's float (it goes to the store safe if the store uses one).
2. **Tender Declaration**: count the cash per note and coin. With *Blind Tender Declaration*, the cashier doesn't see the expected amount.
3. **X Report** (optional): shows the totals without closing the period.
4. **Z Report**: closes the period for the terminal and prints the totals per tender, discounts, returns and voids.
   If a table check is partly paid, finish it first.

## Store safe (optional)

If the store has a *Safe G/L Account*, open **Store Safe** to record **Bank Deposit**, **Cash from Bank** and **Count Safe** (with difference posting).

## Statements (back office)

1. Open **POS Statements** and choose **New Statement** for the store and date (or let the job queue do it).
2. Choose **Calculate Statement**. It lists the expected amount per tender, the counted amount and the difference.
3. Check differences above the *Max. Statement Difference* of the store.
4. Choose **Post Statement**. This creates and posts:
   * a **sales invoice** (and a credit memo for returns) for the cash customer, or per customer for account sales: item ledger, cost and VAT / GST;
   * **general journal** lines for tenders, gift cards, deposits, rounding, income / expense, float and differences.

The **Z Report History (Excel)** and **POS Sales Analysis** reports help you check the day.
