---
title: वेब स्टोर और Swiggy / Zomato
permalink: /hi/help/ecommerce
lang: hi
---

# वेब स्टोर और Swiggy / Zomato

इसके लिए **TGS POS - E-Commerce** ऐप ज़रूरी है।

## वेब स्टोर (Shopify, WooCommerce, Magento 2, BigCommerce)

1. **वेब स्टोर** (Web Stores) → नया: प्लेटफ़ॉर्म, शॉप URL, ऑर्डर लेने या पूरा करने वाला स्टोर, और ऑनलाइन-भुगतान क्लियरिंग खाता।
2. **API क्रेडेंशियल सेट करें** (Set API Credentials): Shopify / Magento / BigCommerce एक्सेस टोकन, या WooCommerce consumer key और secret।
3. जिन आइटम को प्रकाशित करना है, उन पर *ऑनलाइन बेचें* (Sell Online) पर टिक करें।
4. **आइटम और मूल्य सिंक करें** (Sync Items & Prices), **स्टॉक सिंक करें** (Sync Inventory) और **भुगतान किए ऑर्डर आयात करें** (Import Paid Orders) चालू करें, और **अभी सिंक करें** (Sync Now) चलाएँ (जॉब कतार इसे दोहराती रहती है)।

आइटम वेब प्रोडक्ट से जुड़े होते हैं (**वेब आइटम लिंक** (Web Item Links))। भुगतान किए वेब ऑर्डर, click & collect या डिलीवरी के लिए **ग्राहक ऑर्डर** (customer orders) बन जाते हैं;
ऑनलाइन भुगतान जमा (डिपॉज़िट) के रूप में दर्ज होता है। जब ऑर्डर ले लिया जाता है या डिलीवर हो जाता है, तो पूरा होने की जानकारी वेब स्टोर पर वापस जाती है।
**वेब सिंक लॉग** (Web Sync Log) हर सिंक को, हर आइटम की त्रुटियों के साथ, दिखाता है।

## UrbanPiper के ज़रिए Swiggy / Zomato

1. अपने Swiggy और Zomato आउटलेट से जुड़ा एक UrbanPiper खाता लें।
2. कनेक्टर (डाउनलोड पैकेज में *AzureConnector*) को अपने Azure सब्सक्रिप्शन में डिप्लॉय करें और UrbanPiper वेबहुक को उसके
   `api/urbanpiper/<web store code>` पते पर secret key के साथ सेट करें।
3. **वेब स्टोर** → प्लेटफ़ॉर्म **UrbanPiper** के साथ नया स्टोर, API क्रेडेंशियल, और **एग्रीगेटर वेब सेवा प्रकाशित करें** (Publish Aggregator Web Service)।
4. वैकल्पिक: *एग्रीगेटर ऑर्डर अपने-आप स्वीकार करें* (Accept Aggregator Orders Automatically); और, Hospitality ऐप के साथ, ऑनलाइन ऑर्डर सीधे किचन भेजें।

ऑर्डर ग्राहक ऑर्डर के रूप में आते हैं। ग्राहक ऑर्डर कार्ड पर: **स्वीकार करें (Swiggy / Zomato)** (Accept (Swiggy / Zomato)), **खाना तैयार** (Food Ready) और **राइडर को सौंपा** (Handed to Rider)
एग्रीगेटर पर स्थिति अपडेट करते हैं। *ऑनलाइन बेचें* चिह्नित आइटम, उनके मूल्य और स्टॉक UrbanPiper पर भेजे जाते हैं।
