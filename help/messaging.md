---
title: SMS, WhatsApp and e-mail receipts
permalink: /help/messaging
---

# SMS, WhatsApp and e-mail receipts

## SMS / WhatsApp Setup

Open **SMS / WhatsApp Setup**:

| Provider | Settings |
|---|---|
| MSG91 (SMS, DLT templates) | Auth key (**Set API Key / Token**), sender ID, receipt and OTP template IDs (DLT-approved in India) |
| Twilio | Account SID, auth token, from number; tick *Send via WhatsApp (Twilio)* for WhatsApp |
| WhatsApp Cloud API (Meta) | Phone number ID, access token, approved template names and language |
| Generic REST | URL and JSON body with `{phone}`, `{text}`, `{template}`, `{var1}`… placeholders, auth header |

Other settings:

* **Default Country Code** (for example `91`), added to 10-digit mobile numbers.
* **Send receipt automatically to members / customers**: sends a short receipt after every sale when a mobile number is known.
* **Ask OTP before redeeming points**: members must give an OTP sent to their phone before paying with points.

Receipt template variables: store, receipt no., amount, date, points. OTP template variables: OTP, points, store.
On the POS, **SMS / WhatsApp Receipt** sends the last receipt to any number. **SMS / WhatsApp Log** shows what was sent and whether the provider accepted it.

## E-mail receipts

Set up an e-mail account in Business Central (**Email Accounts**). Then use **E-mail Receipt** on the POS, or switch on
*Auto E-mail Receipt to Member/Customer* in the functionality profile.
