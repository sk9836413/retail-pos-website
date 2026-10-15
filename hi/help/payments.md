---
title: कार्ड टर्मिनल और UPI QR
permalink: /hi/help/payments
lang: hi
---

# कार्ड टर्मिनल और UPI QR

## कार्ड टर्मिनल

**हार्डवेयर प्रोफ़ाइल** (Hardware Profile) पर **EFT प्रदाता** (EFT Provider) चुनें:

| प्रदाता | ऐप | टिप्पणी |
|---|---|---|
| मैनुअल (Manual) | Retail POS Pro | अलग टर्मिनल; कैशियर स्वीकृति कोड डालता है |
| सिम्युलेटर (Simulator) | Retail POS Pro | परीक्षण के लिए: सब कुछ स्वीकार करता है, .13 पर खत्म होने वाली राशि अस्वीकार करता है |
| हार्डवेयर ब्रिज (Hardware Bridge) | Retail POS Pro | POS PC से जुड़े टर्मिनल (बैंक EDC, Ingenico, Verifone, PAX, Paytm ECR) |
| Pine Labs Plutus Cloud, Razorpay POS (Ezetap), Adyen Terminal API, Stripe Terminal, Square Terminal, SumUp | Payment Terminals | क्लाउड टर्मिनल |
| सामान्य REST (Generic REST) | Payment Terminals | REST API वाला कोई भी दूसरा क्लाउड टर्मिनल (**सामान्य REST टर्मिनल सेटअप** (Generic REST Terminal Setup)) |

मर्चेंट आईडी, स्टोर / POS कोड, टर्मिनल आईडी, यूज़र नाम और एनवायरनमेंट (test / live) भरें, फिर **भुगतान टर्मिनल सीक्रेट / API कुंजी सेट करें** (Set Payment Terminal Secret / API Key)।
लाइव जाने से पहले प्रदाता के sandbox में परीक्षण करें; कुछ प्रदाताओं को सर्टिफ़िकेशन भी चाहिए।

**कार्ड टर्मिनल स्वीकृतियाँ** (Card Terminal Approvals) हर स्वीकृति उसी पल सहेज लेता है जब टर्मिनल उसे स्वीकार करता है। अगर भुगतान दर्ज करना विफल हो जाए, तो अगली कोशिश में
कार्ड से दोबारा पैसे काटने की बजाय वही स्वीकृति फिर से उपयोग होती है। रोज़ सूची जाँचें कि कौन सी स्वीकृतियाँ *रसीद पर दर्ज* (Recorded on Receipt) नहीं हैं, उनका टर्मिनल पर रिफ़ंड करें और *हल किया गया* (Resolved) पर टिक करें।

## UPI QR

**UPI / QR भुगतान** (QR Payment) फ़ंक्शन वाला एक भुगतान प्रकार बनाएँ। हार्डवेयर प्रोफ़ाइल पर **UPI / QR भुगतान प्रदाता** (UPI / QR Payment Provider) चुनें:

| प्रदाता | ऐप | यह कैसे काम करता है |
|---|---|---|
| स्थिर UPI QR (Static UPI QR) | Retail POS Pro | स्टोर की UPI ID (VPA), प्राप्तकर्ता का नाम और सही राशि वाला UPI QR। कैशियर ग्राहक की सफलता स्क्रीन देखकर पुष्टि करता है (लॉग होता है; सुपरवाइज़र की ज़रूरत रखी जा सकती है)। कोई गेटवे शुल्क नहीं। |
| Razorpay UPI QR | Payment Terminals | Razorpay से डायनामिक QR; ग्राहक के भुगतान करते ही POS अपने-आप पुष्टि करता है |
| PhonePe Dynamic QR | Payment Terminals | PhonePe से डायनामिक QR; अपने-आप पुष्टि होती है |

गेटवे के लिए key ID / मर्चेंट आईडी, स्टोर / टर्मिनल आईडी और टाइमआउट भरें, फिर **UPI / QR गेटवे सीक्रेट सेट करें** (Set UPI / QR Gateway Secret)।
QR, POS पर और ग्राहक डिस्प्ले पर दिखता है। UPI रिफ़ंड गेटवे से (या नकद में) किए जाते हैं; UPI भुगतान को POS पर रद्द (void) नहीं किया जा सकता।
