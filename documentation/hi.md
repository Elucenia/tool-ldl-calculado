<!-- ELUCENIA technical documentation · ldl-calculado · hi · no clinical/professional/rights approval -->

# गणना किया गया LDL कोलेस्ट्रॉल

[शर्तें, स्रोत और अनुमतियाँ](https://elucenia.org/hi/tools/ldl-calculado)

## उपयोग कैसे करें

पोर्टल पर उपकरण का उपयोग करें या स्थानीय HTTP सर्वर के माध्यम से index.html खोलें। भाषा चुनें, फ़ील्ड भरें और गणना करें।

## इनपुट और इकाइयाँ

### कुल कोलेस्ट्रॉल

`ct`

mg/dL · सीमा: 50–800

### HDL कोलेस्ट्रॉल

`hdl`

mg/dL · सीमा: 5–200

### ट्राइग्लिसराइड्स

`tg`

mg/dL · सीमा: 10–3000

## विधि का संस्करण

Friedewald 1972 TG\<400 और Sampson NIH 2020 TG≤800; गुणांक 0.948/0.971/8.56/2140/16100/9.44

## दस्तावेज़ित सूत्र

गैर-HDL-c = TC − HDL

Friedewald: LDL = TC − HDL − TG ÷ 5 (TG \< 400 mg/dL पर मान्य)

Sampson (NIH 2020): LDL = TC/0.948 − HDL/0.971 − (TG/8.56 + TG × गैर-HDL/2140 − TG²/16100) − 9.44 (TG 800 mg/dL तक मान्य)

## सीमाएँ और जनसमूह

Sampson 2020 ने ट्राइग्लिसराइड 800 mg/dL तक होने पर LDL-कोलेस्ट्रॉल के अनुमान का आकलन किया; टाइप III हाइपरलिपिडीमिया वाले व्यक्तियों को बाहर रखा गया। विकास नमूने में हाइपरट्राइग्लिसरिडीमिया की आवृत्ति अधिक थी और अन्य जनसंख्याओं में बाहरी सत्यापन हुआ। सूत्र LDL-कोलेस्ट्रॉल को सीधे मापने के बजाय अनुमान लगाता है। उसकी सीमाएँ Friedewald सूत्र पर लागू नहीं करनी चाहिए; चुने गए रूप, इकाई और हर विधि के लिए बताए गए ट्राइग्लिसराइड के क्षेत्र को बनाए रखें।

## संदर्भ

- [Friedewald WT, Levy RI, Fredrickson DS. Estimation of the concentration of low-density lipoprotein cholesterol in plasma, without use of the preparative ultracentrifuge. Clin Chem, 1972.](https://doi.org/10.1093/clinchem/18.6.499)

- [Sampson M et al. A new equation for calculation of low-density lipoprotein cholesterol in patients with normolipidemia and/or hypertriglyceridemia. JAMA Cardiol, 2020.](https://doi.org/10.1001/jamacardio.2020.0013)

- [Faludi AA et al. Atualização da Diretriz Brasileira de Dislipidemias e Prevenção da Aterosclerose – 2017. Arq Bras Cardiol.](https://doi.org/10.5935/abc.20170121)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/)

## तकनीकी परीक्षण दोहराएँ

दर्ज कृत्रिम मामलों को दोहराने के लिए इस रिपॉज़िटरी की मूल निर्देशिका में node test.cjs चलाएँ। मूल इनपुट, अपेक्षित परिणाम और सहनशीलता सीमाएँ सुरक्षित रखी गई हैं। तकनीकी परीक्षण नैदानिक सत्यापन नहीं हैं।

```sh
node test.cjs
```

tool.json में स्रोत, संस्करण और समीक्षा का दायरा दिया गया है। examples.json में कृत्रिम इनपुट और अपेक्षित परिणाम सुरक्षित हैं; results.json में प्राप्त परिणाम दर्ज हैं।

[रिकॉर्ड और संदर्भ](../tool.json) · [JavaScript कोड](../calculator.js) · [संदर्भ मामले](../examples.json) · [results.json](../results.json)

## समीक्षा और उपयोग की शर्तें

स्वतंत्र नैदानिक समीक्षा नहीं की गई है।

यह इंटरफ़ेस लेखकों द्वारा किया गया अनुवाद है, कोई आधिकारिक या प्रमाणित संस्करण नहीं। स्वतंत्र नैदानिक समीक्षा, पेशेवर भाषाई समीक्षा और उपकरणों के अधिकारों की अनुमति की प्रक्रिया पूरी नहीं हुई है।

सूत्र या वर्गीकरण का परिणाम। व्याख्या, कार्यवाही और उपयुक्तता पेशेवर मूल्यांकन और चुने गए स्रोत पर निर्भर है।

## लाइसेंस और श्रेय

Apache-2.0 केवल ELUCENIA के कोड पर लागू होता है। उपकरणों, प्रकाशनों, अनुवादों और डेटा के अधिकार उनके संबंधित अधिकारधारकों के पास रहते हैं। LICENSE और NOTICE सुरक्षित रखें।

ELUCENIA · Felipe Guedes · Copyright © 2026
