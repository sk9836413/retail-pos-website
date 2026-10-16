---
title: Using the POS
permalink: /help/pos-guide
---

# Using the POS (cashier guide)

## Log on

Enter your **Staff ID** and **password** and choose **Log On**. **Clock In / Out** on the log-on screen records your working hours.
The POS logs you off automatically after the time set in the functionality profile.

## Sell

* **Scan** a barcode, or type the item number and press Enter.
* **Several pieces**: type `3*` and scan, or `3*barcode`. Or select the line and use **Quantity**, **+1** and **-1**.
* **Items with sizes and colours**: the POS shows the variants (or a size × colour grid with stock) to choose from.
* **Weighed items**: put the item on the scale. The POS reads the weight (with the Hardware Bridge) or asks for it.
* **Price-embedded labels** from scales are recognised automatically.
* **Find an item**: **Item Search** shows pictures, **Item Lookup** searches by name, **Item Info** shows price and stock, **Store Stock** shows stock in every store.
* **Void Line** removes the selected line. **Void Transaction** cancels the whole sale.

## Keyboard shortcuts

| Key | Function |
|---|---|
| F1 | Show the shortcuts |
| F2 | Quantity |
| F3 | Item search |
| F4 | Void line |
| F5 / F6 | Customer / Member |
| F7 | Price check (scan an item without selling it) |
| F8 | Lock the POS |
| F9 / F10 | Suspend / Recall |
| F12 | Total; in the payment screen: pay the rest in cash |
| + / − | Quantity +1 / −1 (when the input is empty) |
| Del | Void the selected line (when the input is empty) |
| ↑ ↓ | Select the line above / below |
| Esc | Clear the input; in the payment screen: back |

## Customers, members and coupons

* **Member**: scan the member card or type the mobile number. Member prices, offers and points apply at once.
* **New Member** enrols a customer on the spot. **New Customer** creates a Business Central customer (with GSTIN in India).
* **Coupon**: scan or type the coupon code.
* **Customer**: type a customer number, mobile number (spaces and +91 are fine) or part of the name.
  Sales on account check that the customer isn't blocked and stays within the credit limit; above it a manager can approve.
* **Salesperson**: choose the staff member who served the customer (printed on the receipt, for commission reports).
* **Item Note** / **Receipt Note**: a note on the selected item (printed under it and on the kitchen ticket) or on the whole receipt.

## Discounts and price changes

**Line Discount %**, **Line Discount Amount**, **Total Discount %**, **Total Discount Amount** and **Price Override** follow the limits
of your permission group. Above your limit, a supervisor enters their ID and password to approve. Every approval is in the **POS Audit Log**.

## Payment

1. Choose **Total**.
2. Choose a payment button: **Cash**, **Card**, **UPI**, **Gift Card**, **Voucher**, **Points**, **Customer Account** or foreign currency.
3. Enter the amount or use a quick-cash button. Pay with several tenders if needed. Typing an amount and pressing Enter pays it in cash.
4. The receipt prints and the change is shown in large numbers until the next customer.

A payment button that is tapped twice is only used once, so a card is never charged twice by a double tap.

* **Card**: the card terminal starts automatically. Wait for approval. Never take a second payment if you are not sure the first one failed;
  the POS reuses an approval it already received for this receipt.
* **UPI QR**: the QR with the exact amount appears on the POS and the customer display. With a payment gateway the sale finishes
  automatically when the customer pays. With the static UPI QR, check the customer's success screen and confirm (a supervisor may need to approve).
* **Points**: if OTP is switched on, the member gets an OTP on their phone and you type it in.

After payment you can use **Print Last Receipt**, **Gift Receipt**, **E-mail Receipt** or **SMS / WhatsApp Receipt**.

## Returns

* **Return Receipt**: scan the original receipt barcode. Choose the items being returned. The refund is the price the customer paid.
  Items scanned after that are sold normally, so an **exchange** is one receipt: return the old item, add the new one, pay or refund the difference.
* **Return Mode** for returns without a receipt (if your store allows it).
* Return policies can block returns, allow exchange only, or limit the number of days. The POS tells you when that happens.
  For **exchange only**, add the new items before paying.

## Suspend and recall

**Suspend** parks the sale (for example the customer forgot something). **Recall** brings it back on any terminal in the store;
**Recall Last Sale** takes the most recent one directly.

## Lock and log off

**Lock POS** (F8) locks the screen and keeps the open sale; only the same cashier or a manager can unlock it.
After the auto log-off time the POS locks by itself if a sale is open, otherwise it logs off. After 5 wrong passwords a staff member is
locked until a manager sets a new password. Log off switches training mode off.

## Cash

* **Float Entry**: cash put into the drawer (opening float).
* **Remove Tender**: cash taken out (to the safe or a cash pickup).
* **Open Drawer**: opens the drawer without a sale; the cashier types a reason (logged in the audit log).
* **Income/Expense**: small cash income or expenses (for example courier charges).

## Other buttons

**Customer Order** (layaway, special order, click & collect, with a deposit), **Collect Order**, **Cancel Order**, **Customer Payment** (pays the
customer's account), **Sales Type** (dine-in, takeaway, delivery), **Inventory Adjustment** (wastage), **Receive Transfer**,
**Receive Purchase Order**, **Stock Count**, **POS Messages**, **Training Mode**, **Logoff**.

## Training mode

In training mode, nothing is posted, card terminals are not charged, and receipts are marked *TRAINING - NOT VALID*. Use it for new staff.
