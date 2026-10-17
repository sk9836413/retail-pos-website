---
title: Move from Tally to Business Central
permalink: /help/tally-migration
---

# Move from Tally to Business Central

**TGS POS - Tally Migration** brings a TallyPrime or Tally.ERP 9 company into Business Central:

| In Tally | Becomes in Business Central |
|---|---|
| Ledgers under Sundry Debtors | Customers (with GSTIN, PAN, state, address, credit limit, credit period) |
| Ledgers under Sundry Creditors | Vendors |
| Ledgers under Bank Accounts / Bank OD A/c | Bank accounts (account no., IFSC) |
| All other ledgers | G/L accounts, with the right category (assets, liabilities, equity, income, purchases, expenses) |
| Stock items | Items (alias as item no., HSN/SAC, GST group, base and alternate unit, selling rate) |
| Units, godowns, stock groups, cost centres | Units of measure, locations, item categories, dimension values |
| Opening balances | General journal, balanced by an opening balance account |
| Bill-wise outstanding | One open invoice / credit memo per bill, with bill date and due date, so ageing works |
| Opening stock per godown | Item journal with quantity and value per location |

Nothing is posted by the app: it creates the masters and the journals, and you post the journals after checking them.
The app works without TGS POS. With the Business Central **India localization**, GSTIN, state, PAN, GST customer / vendor type,
HSN/SAC and GST group are filled in as well.

Want to try it first? Download the sample company **Sharma Traders**: [masters](../samples/tally-masters-sample.xml) and
[day book](../samples/tally-daybook-sample.xml) (go-live 1 May 2024, books begin 1 April 2024).

## 1a. Direct connection (no export files)

Use this on a PC where Tally runs, or any PC in the same office network as the Tally PC / Tally server.

1. Install the free **TGS Hardware Bridge** on that PC (the same small program the POS uses for printers; version 1.1 or later).
2. In Tally, load the company and switch on the XML server: TallyPrime **F1 (Help) > Settings > Connectivity > Client/Server configuration**,
   *TallyPrime acts as* **Server** (or **Both**), port **9000**. In Tally.ERP 9: **F12 > Advanced Configuration**, *Tally is acting as* **Both**.
3. In Business Central open the migration and choose **1. Fetch from Tally (direct)**.
4. **Tally Computer**: *localhost* for this PC, or the name / IP address of the Tally PC in your network. Port 9000. Bridge URL and token as for the POS.
5. **Connect**: the companies open in Tally are listed; choose one. The books begin date is read from Tally.
6. Enter the **Go-Live Date** and choose **Fetch from Tally**. The app reads, one after the other:
   * all masters (like *List of Accounts*);
   * the day book month by month, from the books begin date to the day before go-live;
   * Tally's own **closing balances** and **closing stock** on the day before go-live.
7. The balances are calculated straight away. With **Use Tally's Closing Balances** on (set automatically when Tally sent them) the
   ledger balances and stock values are exactly Tally's; the check lists every ledger where the day book gives a different figure.

The bridge only talks to this PC and computers in your own network (10.x, 172.16–31.x, 192.168.x, computer names), never to the internet.
Big companies: the day book is read month by month; a month above 60 MB stops with a message.

## 1b. Or: export from Tally

Use **XML (Data Interchange)** as the format. Unicode and ASCII both work.

**Masters (always)**

* TallyPrime: **Gateway of Tally > Alt+E (Export) > Masters**. Type of masters: **All Masters**, include dependent masters: **Yes**,
  file format: **XML (Data Interchange)**. Choose **Send**.
* Tally.ERP 9: **Gateway of Tally > Display > List of Accounts > Alt+E (Export)**, format **XML (Data Interchange)**,
  then the same for **Display > Inventory Info > List of Stock Items** if you didn't export all masters.

**Day book (when you go live during the financial year)**

* **Gateway of Tally > Day Book**, **F2** (period) = books begin of the current year up to the **day before go-live**.
* **Alt+E (Export) > Current**, format **XML (Data Interchange)**, all voucher types.

Going live on the first day of a financial year (1 April)? Then the masters export is enough: its opening balances are the balances on that day.

## 2. Import and map

1. Search for **Tally Migrations** (or **Assisted Setup > Move from Tally**) and create a migration.
2. **1. Import Masters** and, if needed, **1b. Import Day Book**.
3. Fill in:
   * **Books Begin Date** (usually 1 April) and **Go-Live Date** (your first day in Business Central; opening entries are posted on the day before);
   * **Opening Balance Account**: a balance sheet account that balances the opening entries (it ends at zero);
   * **Change in Stock Account** (go-live during the year): an income statement account for closing minus opening stock;
   * posting groups for new customers, vendors, bank accounts and items.
4. Check **Ledgers**: the app proposes what each ledger becomes and a number. To use an existing record, enter its number
   (for example map *CGST Output* to your GST payable account). Customers and vendors without a number get the number series.
5. Check **Stock Items** (item no., units, *Base Units per Alternate Unit*) and **GST Rate Mapping** (GST group per rate).

## 3. Calculate, check, create

1. **3. Calculate Balances**: balances, open bills and stock on the go-live date. Stock value uses the average cost (Tally's default).
   You can correct a balance or a stock line by hand afterwards.
2. **4. Check**: everything that must be fixed (red) or checked. The **Difference in opening balances** must be zero, like in Tally.
3. **5. Create Masters**: creates the records. A line that fails shows the reason; correct it and run it again (created records are kept).
4. **6. Create Opening Journals**: the general journal *TALLY-OB* and the item journal *TALLY-OB*.

## 4. Compare and post

Before posting, compare with Tally on the day before go-live:

* the **trial balance** with the general journal (and the trial balance in Business Central after posting);
* **Bills Receivable / Payable** with the customer and vendor lines;
* the **Stock Summary** (quantity and value per godown) with the item journal.

Then post the item journal first, then the general journal. The opening balance account should then be zero.

## Notes

* The opening stock posts against the **Inventory Adjmt. Account** of the general posting setup. Set it to the opening balance
  account while you post the opening stock (the check tells you).
* Batches, serial numbers and expiry dates are added up per godown; set up item tracking in Business Central if you need them.
* Foreign currency ledgers are migrated in rupees.
* Voucher types that don't change the books (memorandum, sales / purchase orders) are left out; change the list on the migration card.
  Physical stock vouchers are counted as movements: if you use them, check the stock lines.
* Cancelled and optional vouchers are left out, and so are vouchers on or after the go-live date.
