---
title: SMS, WhatsApp और ई-मेल रसीदें
permalink: /hi/help/messaging
lang: hi
---

# SMS, WhatsApp और ई-मेल रसीदें

## SMS / WhatsApp सेटअप

**SMS / WhatsApp सेटअप** (SMS / WhatsApp Setup) खोलें:

| प्रदाता | सेटिंग |
|---|---|
| MSG91 (SMS, DLT टेम्पलेट) | ऑथ कुंजी (**API कुंजी / टोकन सेट करें** (Set API Key / Token)), सेंडर आईडी, रसीद और OTP टेम्पलेट आईडी (भारत में DLT-स्वीकृत) |
| Twilio | Account SID, ऑथ टोकन, भेजने वाला नंबर; WhatsApp के लिए *WhatsApp से भेजें (Twilio)* (Send via WhatsApp (Twilio)) पर टिक करें |
| WhatsApp Cloud API (Meta) | फ़ोन नंबर आईडी, एक्सेस टोकन, स्वीकृत टेम्पलेट नाम और भाषा |
| सामान्य REST (Generic REST) | URL और JSON बॉडी, `{phone}`, `{text}`, `{template}`, `{var1}`… प्लेसहोल्डर के साथ, ऑथ हेडर |

अन्य सेटिंग:

* **डिफ़ॉल्ट देश कोड** (Default Country Code) (उदाहरण के लिए `91`), 10 अंकों वाले मोबाइल नंबरों के आगे जोड़ा जाता है।
* **सदस्यों / ग्राहकों को रसीद अपने-आप भेजें** (Send receipt automatically to members / customers): मोबाइल नंबर पता हो तो हर बिक्री के बाद छोटी रसीद भेजता है।
* **पॉइंट्स भुनाने से पहले OTP पूछें** (Ask OTP before redeeming points): पॉइंट्स से भुगतान करने से पहले सदस्यों को अपने फ़ोन पर भेजा गया OTP देना होगा।

रसीद टेम्पलेट के वेरिएबल: स्टोर, रसीद नं., राशि, तारीख, पॉइंट्स। OTP टेम्पलेट के वेरिएबल: OTP, पॉइंट्स, स्टोर।
POS पर, **SMS / WhatsApp रसीद** (SMS / WhatsApp Receipt) आखिरी रसीद किसी भी नंबर पर भेजता है। **SMS / WhatsApp लॉग** (SMS / WhatsApp Log) दिखाता है कि क्या भेजा गया और प्रदाता ने उसे स्वीकार किया या नहीं।

## ई-मेल रसीदें

Business Central में एक ई-मेल खाता सेट करें (**ई-मेल खाते** (Email Accounts))। फिर POS पर **रसीद ई-मेल करें** (E-mail Receipt) का उपयोग करें, या कार्यक्षमता प्रोफ़ाइल में
*सदस्य/ग्राहक को रसीद अपने-आप ई-मेल करें* (Auto E-mail Receipt to Member/Customer) चालू करें।
