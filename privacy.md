---
title: Privacy statement
permalink: /privacy
---

<!-- DRAFT: fill in the [bracketed] parts and have it checked by a lawyer before publishing. -->

# Privacy statement

Last updated: [date]

This statement explains how **[Company legal name]** ("we") handles personal data in connection with the Retail POS Pro apps
for Microsoft Dynamics 365 Business Central ("the apps").

## 1. Who controls the data

The apps run inside **your** Business Central environment, which Microsoft hosts for you. The data you enter or create with the apps
(sales, customers, loyalty members, staff, stock, payments) is stored in your Business Central database. **You are the data controller**
for that data. Microsoft processes it as described in the Microsoft Product Terms and the Microsoft Privacy Statement.
We do not have access to your Business Central environment or your data unless you give us access for support.

## 2. Data the apps send to other services

The apps only send data to services that **you** switch on and configure:

| Feature | Service you choose | Data sent |
|---|---|---|
| Card terminals | Your payment provider (e.g. Pine Labs, Razorpay, Adyen, Stripe, Square, SumUp) | Amount, currency, receipt reference, terminal ID |
| UPI QR payments | Your payment gateway (e.g. Razorpay, PhonePe) | Amount, receipt reference |
| SMS / WhatsApp receipts and OTPs | Your messaging provider (e.g. MSG91, Twilio, Meta WhatsApp) | Customer mobile number, receipt summary or OTP |
| E-mail receipts | Your e-mail account set up in Business Central | Customer e-mail address, receipt |
| GST e-invoice and e-way bill | Your GST Suvidha Provider (GSP) and the government IRP | Invoice, buyer GSTIN, items, tax, transport details |
| Web stores and food aggregators | Your Shopify, WooCommerce, Magento, BigCommerce or UrbanPiper account | Items, prices, stock; orders with customer name, phone and delivery address |
| QR table ordering | The ordering web app you deploy in your own Azure subscription | Menu, table number, ordered items, guest notes |

These services process the data under their own terms and privacy statements, which you agree with them directly.
Credentials (API keys, tokens, secrets) are stored encrypted in Business Central isolated storage.

## 3. Data we collect

[Choose one and delete the other:]

* We do **not** collect any personal data from the apps.
* The apps send **technical telemetry** (for example error messages, feature usage, performance) to our Azure Application Insights
  resource. Telemetry contains no customer, member or payment data. It is used only to support you and improve the apps and is kept
  for [90] days.

If you contact our support, we process your name, e-mail address and the information you send us to answer your request.

## 4. Your customers' rights

Requests from your customers or members (access, correction, deletion) are handled by you in Business Central, for example on the
member, customer and contact cards. Posted sales and tax documents may have to be kept by law.

## 5. Security

The apps use the security of Business Central online: Microsoft Entra ID sign-in, permission sets, encrypted isolated storage for
secrets and HTTPS for all calls to other services.

## 6. Contact

[Company legal name], [address], [country]
E-mail: [privacy@example.com]
