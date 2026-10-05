<!-- ELUCENIA technical documentation · ldl-calculado · en · no clinical/professional/rights approval -->

# Calculated LDL cholesterol

[conditions, sources and permissions](https://elucenia.org/en/tools/ldl-calculado)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Total cholesterol

`ct`

mg/dL · range: 50–800

### HDL cholesterol

`hdl`

mg/dL · range: 5–200

### Triglycerides

`tg`

mg/dL · range: 10–3000

## Method edition

Friedewald 1972 TG\<400 and Sampson NIH 2020 TG≤800; coefficients 0.948/0.971/8.56/2140/16100/9.44

## Documented formula

Non-HDL-C = TC − HDL

Friedewald: LDL = TC − HDL − TG ÷ 5 (valid with TG \< 400 mg/dL)

Sampson (NIH 2020): LDL = TC/0.948 − HDL/0.971 − (TG/8.56 + TG × non-HDL/2140 − TG²/16100) − 9.44 (valid up to TG 800 mg/dL)

## Limits and population

Sampson 2020 assessed LDL-cholesterol estimation up to triglycerides of 800 mg/dL; people with type III hyperlipidemia were excluded. The development sample had a high frequency of hypertriglyceridemia, with external validation in other populations. The formula estimates, rather than directly measures, LDL cholesterol. Its limits must not be transferred to the Friedewald formula; preserve the selected variant, unit and triglyceride domain stated for each method.

## References

- [Friedewald WT, Levy RI, Fredrickson DS. Estimation of the concentration of low-density lipoprotein cholesterol in plasma, without use of the preparative ultracentrifuge. Clin Chem, 1972.](https://doi.org/10.1093/clinchem/18.6.499)

- [Sampson M et al. A new equation for calculation of low-density lipoprotein cholesterol in patients with normolipidemia and/or hypertriglyceridemia. JAMA Cardiol, 2020.](https://doi.org/10.1001/jamacardio.2020.0013)

- [Faludi AA et al. Atualização da Diretriz Brasileira de Dislipidemias e Prevenção da Aterosclerose – 2017. Arq Bras Cardiol.](https://doi.org/10.5935/abc.20170121)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
