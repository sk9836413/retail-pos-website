---
title: Stores, terminals, staff and profiles
permalink: /help/setup
---

# Stores, terminals, staff and profiles

All setup pages are on the **Retail Manager (POS)** role center and under **Retail POS Setup**.

## Retail POS Setup

Number series, posting accounts (gift card and voucher liability, deposits, rounding, differences, float), gift card validity,
replenishment defaults and **embedded barcodes** (scale / price labels).

Embedded barcode example: prefix `22`, item no. length `5`, value decimals `2`, type *Price*. The barcode `2212345012990` is item `12345` at price `129.90`.
With type *Weight* the value is the quantity.

## Stores

One card per shop or outlet: address, **Location Code**, **Cash (Walk-in) Customer No.**, customer price group, dimensions, statement numbering,
**Max. Statement Difference**, cash rounding, member club, service charge, tip and delivery fee codes, receipt layout,
**Receipt Language** (blank = English; most thermal printers can only print Latin characters), safe and bank account.

## More stores

On the **Stores** list choose **New Store (copy settings)**: enter the new store number and name, a new or existing location and the number of
its first POS terminal. Profiles, POS menu, walk-in customer, price group, loyalty club, dimensions and receipt texts are copied from the store you choose.
**Setup Check** then shows if anything is still missing for the new store.

A POS terminal can only be open in one browser window at a time; the POS remembers the terminal each user chose.

## Store groups

**Store Groups** collect stores (for example *North region* or *Malls*). Use them on offers, POS messages and **Store Group Assortment Blocks**
(items not sold in these stores, optionally only between two times, for example no alcohol from 22:00 to 06:00).
**Store Assortment Blocks** do the same for one store.

## POS terminals

Each till or tablet is a terminal in a store. A terminal can override the store's functionality profile, hardware profile and POS menu.
Set the default terminal for each user in **User Setup**.

## Functionality profiles

How the POS behaves: auto print receipt and copies, max. quantity and line amount, suspended sales per store, require customer, infocodes,
auto log-off, loyalty, blind tender declaration, zero-price sales, show inventory, returns (original receipt required, max. days),
Z report requires tender declaration, self-checkout mode, auto e-mail receipts, ask for variant, default deposit %, ask serial / lot no.
The Hospitality app adds *Hospitality Mode*, *Send to Kitchen on Payment* and *Show Order Number after Payment*.

## Hardware profiles

Receipt printer (browser or Hardware Bridge), receipt width, cash drawer, customer display, card terminal (EFT provider and its settings),
UPI / QR payment provider, and the Hardware Bridge devices. See [Hardware](hardware) and [Card terminals and UPI QR](payments).

## Staff and permission groups

**Staff**: ID, name, store, permission group, commission %. Set the password with **Set POS Password** (passwords are stored as salted hashes);
the **Password Set** column shows who can't log on yet. After 5 wrong passwords a staff member is locked until a new password is set.

**Permission Groups** decide what staff may do: void line or transaction, price override, line and total discount (with max. %), returns,
open drawer, X / Z report, tender declaration, float / remove tender, training mode, suspend / recall, reprint, inventory adjustment,
credit limit override (sales on account above the customer's credit limit).
*Manager Privileges* lets the group approve actions for others.

## Tender types

Cash, card, UPI / QR, gift card, voucher, points, customer account, foreign currency. Per tender: function, account, change tender,
overtender and partial payment rules, counting, open drawer, refunds, min. / max. amount, currency, button order and colour.

## POS menus and the screen designer

**POS Menus** hold the buttons (command, parameter, caption, colour, icon, size). Open **Open Screen Designer** to drag and drop buttons.
*Show Item Pictures on Buttons* shows item pictures (import pictures on the item card).
Commands are listed in [Using the POS](pos-guide); a button with command *Item* and an item number as parameter sells that item.

## Receipts

**Receipt Texts** (header and footer per store), **Receipt Layouts** with the drag-and-drop **Receipt Designer** (sections, bold, double size,
alignment, custom text with placeholders, QR code, barcode, logo, live preview).

## Infocodes

Questions asked on the POS: text, number, selection or yes / no, on item, total, return, void, price override or discount.
Use them for reasons (why was the price changed?) or data (customer's age group).

## Income / expense accounts, linked items, modifiers

* **Income/Expense Accounts**: small cash income or expenses on the POS, posted to a G/L account.
* **Linked Items**: deposits or accessories added automatically with an item.
* **Item Modifier Groups**: choices and extras (no onion, extra cheese +20) with min. / max. selection and price add-ons.

## Customer display adverts

**Customer Display Adverts**: pictures (JPG / PNG, e.g. 1280 × 720) shown on the customer display when no sale is running.
Set the store (blank = all), period, order and seconds per advert.
