---
title: Hospitality
permalink: /help/hospitality
---

# Hospitality: tables, kitchen, QR ordering and kiosk

Requires the **TGS POS - Hospitality** app.

## Set up

1. **Dining Areas & Tables**: create areas (for example *Ground floor*, *Terrace*) and tables with seats.
   **Open Floor Plan Designer** to drag tables into place, resize them and choose square, round or rectangle.
2. **Hospitality Courses**: starter, main, dessert… *Hold until fired* keeps a course back until the waiter fires it.
3. **Kitchen Display Stations** and **Kitchen Routing**: which items or item categories go to which station (or kitchen printer).
4. **Item Modifier Groups** for choices and extras; **Deals (Meal Combos)** for combos with a fixed price.
5. On the terminal: functionality profile with **Hospitality Mode** (the POS starts on the tables screen) and the RESTAURANT menu.

## Table service

* **Tables** shows the floor plan: free, occupied (with amount, guests and minutes), bill printed, reserved.
* Tap a table, enter the **Guests**, and order. **Send to Kitchen** sends the new lines; held courses wait for **Fire Course**.
* **Transfer Table**, **Merge Table**, **Split Bill** (move lines to a new check), **Change Course**.
* **Print Bill** prints a pre-check with suggested tips. **Service Charge** and **Tip** are added as lines.
* A table check can be paid on any POS in the store.
* **Table Reservations** appear on the floor plan; the guest count is taken over when the guests are seated.

## Kitchen display

Open **Kitchen Display** on a screen in the kitchen and choose the station. Orders appear with table, course, modifiers and timers
(amber and red when late). Tap to start, mark ready, served or recall. Voids are shown. A sound plays for new orders.

## QR table ordering

Guests scan a QR code on the table, see the menu on their phone and order. The order goes to the table's check and,
if you want, straight to the kitchen. Guests can't order for other tables: every QR link is signed.

1. Deploy the ordering web app (*AzureConnector* in the download package) to your Azure subscription. Its README has the steps.
2. **QR Table Ordering Setup**: *Enabled*, the web app URL, staff ID and POS terminal for guest orders, max. lines per order,
   *Send guest orders to the kitchen at once*. Choose **Publish Web Service**.
3. On items: *On QR Table Menu* and a menu description for guests.
4. **Table QR Codes**: print the codes and put them on the tables. **Reset Table Links** makes all printed codes invalid (print new ones).

## Quick service and self-order kiosk

In the functionality profile:

* **Send to Kitchen on Payment**: the whole order goes to the kitchen when it is paid (counters, food courts).
* **Show Order Number after Payment**: the guest sees the order number to wait for.

Combine with *Self-Checkout Mode* and a card terminal or UPI QR for a self-order kiosk on a touch screen.

## Swiggy / Zomato orders in the kitchen

With the E-Commerce app, *Send online orders (Swiggy / Zomato / web) to the kitchen* in **QR Table Ordering Setup** sends aggregator
orders to the kitchen as soon as they arrive.
