---
title: Card terminals and UPI QR
permalink: /help/payments
---

# Card terminals and UPI QR

## Card terminals

On the **Hardware Profile**, choose the **EFT Provider**:

| Provider | App | Notes |
|---|---|---|
| Manual | Retail POS Pro | Stand-alone terminal; the cashier enters the approval code |
| Simulator | Retail POS Pro | For testing: approves everything, declines amounts ending in .13 |
| Hardware Bridge | Retail POS Pro | Terminals connected to the POS PC (bank EDC, Ingenico, Verifone, PAX, Paytm ECR) |
| Pine Labs Plutus Cloud, Razorpay POS (Ezetap), Adyen Terminal API, Stripe Terminal, Square Terminal, SumUp | Payment Terminals | Cloud terminals |
| Generic REST | Payment Terminals | Any other cloud terminal with a REST API (**Generic REST Terminal Setup**) |

Fill in the merchant ID, store / POS code, terminal ID, user name and environment (test / live), then **Set Payment Terminal Secret / API Key**.
Test with the provider's sandbox before going live; some providers also require certification.

**Card Terminal Approvals** keeps every approval the moment the terminal approves it. If recording the payment fails, the next try reuses
the approval instead of charging the card again. Check the list daily for approvals not *Recorded on Receipt*, refund them on the terminal and tick *Resolved*.

## UPI QR

Create a tender type with the function **QR Payment**. On the hardware profile, choose the **UPI / QR Payment Provider**:

| Provider | App | How it works |
|---|---|---|
| Static UPI QR | Retail POS Pro | A UPI QR with the store's UPI ID (VPA), payee name and the exact amount. The cashier checks the customer's success screen and confirms (logged; can require a supervisor). No gateway fees. |
| Razorpay UPI QR | Payment Terminals | Dynamic QR from Razorpay; the POS confirms automatically when the customer pays |
| PhonePe Dynamic QR | Payment Terminals | Dynamic QR from PhonePe; confirmed automatically |

For gateways, fill in the key ID / merchant ID, store / terminal ID and timeout, then **Set UPI / QR Gateway Secret**.
The QR is shown on the POS and on the customer display. UPI refunds are made from the gateway (or in cash); a UPI payment can't be voided on the POS.
