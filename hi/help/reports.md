---
title: रिपोर्ट और Power BI
permalink: /hi/help/reports
lang: hi
---

# रिपोर्ट और Power BI

## Business Central में

| रिपोर्ट / पेज | क्या दिखाता है |
|---|---|
| **POS बिक्री विश्लेषण (Excel)** (POS Sales Analysis (Excel)) | स्टोर, तारीख, आइटम, आइटम श्रेणी, स्टाफ़, भुगतान प्रकार या घंटे के अनुसार बिक्री, Excel में निर्यात |
| **Z रिपोर्ट इतिहास (Excel)** (Z Report History (Excel)) | हर Z रिपोर्ट, हर भुगतान प्रकार के कुल के साथ |
| **आइटम / स्टाफ़ / स्टोर और तारीख / भुगतान प्रकार के अनुसार POS बिक्री** (POS Sales by Item / Staff / Store & Date / Tender) | विश्लेषण क्वेरी जिन्हें आप Excel में खोल सकते हैं |
| **ऑफ़र प्रदर्शन** (Offer Performance) | हर ऑफ़र की बिक्री और छूट |
| **स्टाफ़ प्रदर्शन** (Staff Performance) | बिक्री, लेन-देन, औसत बिल, छूट, रद्द (void), घंटे, प्रति घंटा बिक्री और कमीशन |
| **बिक्री बजट** (Sales Budgets) | हर स्टोर और दिन का बजट बनाम असली बिक्री |
| **POS लेन-देन** (POS Transactions), **बिक्री प्रविष्टियाँ** (Sales Entries), **भुगतान प्रविष्टियाँ** (Payment Entries) | हर रसीद और लाइन |
| **POS ऑडिट लॉग** (POS Audit Log) | रद्द (void), मूल्य बदलना, छूट, ड्रॉअर खोलना, स्वीकृतियाँ |

भारत GST रिपोर्ट [भारत GST](india-gst) में बताई गई हैं।

## Power BI

TGS POS, Power BI, Excel और Fabric के लिए `knack/retailPosAnalytics/v1.0` के तहत केवल-पढ़ने वाले डेटा फ़ीड देता है:
`posSalesLines`, `posReceipts`, `posPayments`, `posDiscounts`, `posStores`, `posStaff`।

Power BI Desktop में: **Get Data → Dynamics 365 Business Central**, साइन इन करें, फिर अपना एनवायरनमेंट और कंपनी चुनें,
**Advanced APIs → knack/retailPosAnalytics/v1.0**। डाउनलोड पैकेज की PowerBI गाइड में डेटा मॉडल, एक तारीख टेबल और
तैयार DAX मेज़र हैं (बिक्री, शुद्ध बिक्री, औसत बिल, वापसी %, पिछले साल की तुलना में बढ़त, प्रति कवर बिक्री, वसूला गया GST)।
