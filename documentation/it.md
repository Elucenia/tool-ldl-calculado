<!-- ELUCENIA technical documentation · ldl-calculado · it · no clinical/professional/rights approval -->

# Colesterolo LDL calcolato

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/ldl-calculado)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Colesterolo totale

`ct`

mg/dL · intervallo: 50–800

### Colesterolo HDL

`hdl`

mg/dL · intervallo: 5–200

### Trigliceridi

`tg`

mg/dL · intervallo: 10–3000

## Edizione del metodo

Friedewald 1972 TG\<400 e Sampson NIH 2020 TG≤800; coefficienti 0,948/0,971/8,56/2140/16100/9,44

## Formula documentata

Non-HDL-c = CT − HDL

Friedewald: LDL = CT − HDL − TG ÷ 5 (valida con TG \< 400 mg/dL)

Sampson (NIH 2020): LDL = CT/0,948 − HDL/0,971 − (TG/8,56 + TG × non-HDL/2140 − TG²/16100) − 9,44 (valida fino a TG 800 mg/dL)

## Limiti e popolazione

Sampson 2020 ha valutato la stima del colesterolo LDL fino a trigliceridi di 800 mg/dL; sono state escluse persone con iperlipidemia di tipo III. Il campione di sviluppo aveva un’alta frequenza di ipertrigliceridemia, con validazione esterna in altre popolazioni. La formula stima, invece di misurare direttamente, il colesterolo LDL. I suoi limiti non devono essere trasferiti alla formula di Friedewald; preservare la variante scelta, l’unità e il dominio dei trigliceridi indicato per ogni metodo.

## Riferimenti

- [Friedewald WT, Levy RI, Fredrickson DS. Estimation of the concentration of low-density lipoprotein cholesterol in plasma, without use of the preparative ultracentrifuge. Clin Chem, 1972.](https://doi.org/10.1093/clinchem/18.6.499)

- [Sampson M et al. A new equation for calculation of low-density lipoprotein cholesterol in patients with normolipidemia and/or hypertriglyceridemia. JAMA Cardiol, 2020.](https://doi.org/10.1001/jamacardio.2020.0013)

- [Faludi AA et al. Atualização da Diretriz Brasileira de Dislipidemias e Prevenção da Aterosclerose – 2017. Arq Bras Cardiol.](https://doi.org/10.5935/abc.20170121)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
