<!-- ELUCENIA technical documentation · ldl-calculado · ar · no clinical/professional/rights approval -->

# كوليسترول LDL المحسوب

[الشروط والمصادر والأذونات](https://elucenia.org/ar/tools/ldl-calculado)

## كيفية الاستخدام

استخدم الأداة في البوابة أو افتح index.html عبر خادم HTTP محلي. اختر اللغة، وأكمل الحقول، ثم أجرِ الحساب.

## المدخلات والوحدات

### الكوليسترول الكلي

`ct`

mg/dL · النطاق: ٥٠–٨٠٠

### كوليسترول HDL

`hdl`

mg/dL · النطاق: ٥–٢٠٠

### الدهون الثلاثية

`tg`

mg/dL · النطاق: ١٠–٣٠٠٠

## إصدار الطريقة

Friedewald 1972 TG\<400 وSampson NIH 2020 TG≤800؛ المعاملات 0.948/0.971/8.56/2140/16100/9.44

## المعادلة الموثقة

الكوليسترول غير HDL = CT − HDL

Friedewald: LDL = CT − HDL − TG ÷ 5 (صالحة مع TG \< 400 mg/dL)

Sampson (NIH 2020): LDL = CT/0.948 − HDL/0.971 − (TG/8.56 + TG × غير HDL/2140 − TG²/16100) − 9.44 (صالحة حتى TG 800 mg/dL)

## الحدود والفئة السكانية

قيّمت دراسة Sampson 2020 تقدير كوليسترول LDL حتى مستوى ثلاثي الغليسريد 800 mg/dL؛ واستُبعد المصابون بفرط شحميات الدم من النوع III. كان ارتفاع ثلاثي الغليسريد شائعًا في عينة التطوير، مع تحقق خارجي في فئات أخرى. تقدّر المعادلة كوليسترول LDL بدلًا من قياسه مباشرة. لا ينبغي نقل حدودها إلى معادلة Friedewald؛ حافظ على النسخة المختارة والوحدة ومجال ثلاثي الغليسريد المحدد لكل طريقة.

## المراجع

- [Friedewald WT, Levy RI, Fredrickson DS. Estimation of the concentration of low-density lipoprotein cholesterol in plasma, without use of the preparative ultracentrifuge. Clin Chem, 1972.](https://doi.org/10.1093/clinchem/18.6.499)

- [Sampson M et al. A new equation for calculation of low-density lipoprotein cholesterol in patients with normolipidemia and/or hypertriglyceridemia. JAMA Cardiol, 2020.](https://doi.org/10.1001/jamacardio.2020.0013)

- [Faludi AA et al. Atualização da Diretriz Brasileira de Dislipidemias e Prevenção da Aterosclerose – 2017. Arq Bras Cardiol.](https://doi.org/10.5935/abc.20170121)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/)

## إعادة إجراء الاختبارات التقنية

شغّل node test.cjs في المجلد الجذري لهذا المستودع لتكرار الحالات الاصطناعية المسجلة. تُحفظ المدخلات والنتائج المتوقعة وحدود التفاوت الأصلية. لا تُعدّ الاختبارات التقنية تحققًا سريريًا.

```sh
node test.cjs
```

يحتوي tool.json على المصادر والإصدار ونطاق المراجعة. يحتفظ examples.json بالمدخلات والنتائج المتوقعة للحالات الاصطناعية؛ ويسجل results.json النتائج التي تم الحصول عليها.

[السجل والمراجع](../tool.json) · [شيفرة JavaScript](../calculator.js) · [حالات مرجعية](../examples.json) · [results.json](../results.json)

## المراجعة وشروط الاستخدام

لم تُجرَ مراجعة سريرية مستقلة.

هذه الواجهة ترجمة أعدّها مؤلفوها، وليست إصدارًا رسميًا أو معتمدًا. لم تُجرَ مراجعة سريرية مستقلة أو مراجعة لغوية مهنية، ولم تُستكمل الموافقة على حقوق استخدام الأدوات.

نتيجة المعادلة أو التصنيف. يعتمد التفسير والتصرف ومدى الانطباق على التقييم المهني والمصدر المحدد.

## الترخيص ونسبة العمل إلى أصحابه

ينطبق Apache-2.0 على كود ELUCENIA فقط. تبقى حقوق الأدوات والمنشورات والترجمات والبيانات لأصحابها المعنيين. احتفظ بملفّي LICENSE وNOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
