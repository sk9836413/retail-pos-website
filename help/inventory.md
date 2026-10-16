---
title: Stock and replenishment
permalink: /help/inventory
---

# Stock and replenishment

## Items

TGS POS uses standard Business Central items, item references (barcodes), sales price lists and units of measure.
On the item card you also find: POS blocked, zero price allowed, keying in price / quantity, no discount allowed, age limit, recipe item,
serial / lot tracking, and the picture shown on POS buttons.

## Variants (size and colour)

On the item card choose **Create Variant Matrix**. Enter the first dimension (for example *Size*: `S, M, L, XL`) and the second (*Colour*: `Red, Blue`).
All combinations are created as variants (`S-RED`, `S-BLUE`, …). **Variant Matrix Stock** shows the stock per size and colour.
On the POS, the cashier picks from the size × colour grid.

## Replenishment

**Replenishment Worksheet** → **Calculate Suggestions** per store:

* forecast: *simple average* or *weighted trend* (recent weeks count more), over the sales history days;
* coverage days, plus the item's lead time if *Add Lead Time to Coverage* is on;
* safety stock, reorder point and maximum inventory from the stockkeeping units;
* open purchase and transfer orders are taken into account.

Then **Create Purchase & Transfer Orders**: purchase orders for the item's vendor, or transfer orders from the *Replenish via* location.

## Store allocation

**Store Allocation** spreads a warehouse quantity (for example a new collection) over the stores, by each store's sales share in a period
or equally. Change the quantities if needed, then **Create Transfer Orders** (one per store).

## In the store, on the POS

* **Receive Purchase Order**: choose an open (released) purchase order for the store and enter the quantities received. The receipt is posted.
* **Receive Transfer**: posts the receipt of a shipped transfer order.
* **Stock Count**: scan items (`qty*barcode` for several); the count goes to the **Store Stock Count** worksheet. Post the differences from there.
  Expected stock takes unposted POS sales into account.
* **Inventory Adjustment**: wastage, positive or negative adjustment, or transfer to another location, with a reason code.
  Posted from the **Store Inventory Journal**.

## Labels

**Shelf Labels**: add items (or *Add Items with Price Changes (last 7 days)*) and **Print Labels** with barcode, price and offer price.
