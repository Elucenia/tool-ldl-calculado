<!-- ELUCENIA technical documentation · ldl-calculado · de · no clinical/professional/rights approval -->

# Berechnetes LDL-Cholesterin

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/ldl-calculado)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Gesamtcholesterin

`ct`

mg/dL · Bereich: 50–800

### HDL-Cholesterin

`hdl`

mg/dL · Bereich: 5–200

### Triglyzeride

`tg`

mg/dL · Bereich: 10–3000

## Fassung der Methode

Friedewald 1972 TG\<400 und Sampson NIH 2020 TG≤800; Koeffizienten 0,948/0,971/8,56/2140/16100/9,44

## Dokumentierte Formel

Nicht-HDL-C = GC − HDL

Friedewald: LDL = GC − HDL − TG ÷ 5 (gültig bei TG \< 400 mg/dL)

Sampson (NIH 2020): LDL = GC/0,948 − HDL/0,971 − (TG/8,56 + TG × Nicht-HDL/2140 − TG²/16100) − 9,44 (gültig bis TG 800 mg/dL)

## Grenzen und Population

Sampson 2020 untersuchte die Schätzung von LDL-Cholesterin bei Triglyzeriden bis 800 mg/dL; Personen mit Typ-III-Hyperlipidämie wurden ausgeschlossen. Die Entwicklungsstichprobe hatte eine hohe Häufigkeit von Hypertriglyzeridämie, mit externer Validierung in anderen Populationen. Die Formel schätzt LDL-Cholesterin, statt es direkt zu messen. Ihre Grenzen dürfen nicht auf die Friedewald-Formel übertragen werden; erhalten Sie die gewählte Variante, Einheit und den für jede Methode angegebenen Triglyzeridbereich.

## Referenzen

- [Friedewald WT, Levy RI, Fredrickson DS. Estimation of the concentration of low-density lipoprotein cholesterol in plasma, without use of the preparative ultracentrifuge. Clin Chem, 1972.](https://doi.org/10.1093/clinchem/18.6.499)

- [Sampson M et al. A new equation for calculation of low-density lipoprotein cholesterol in patients with normolipidemia and/or hypertriglyceridemia. JAMA Cardiol, 2020.](https://doi.org/10.1001/jamacardio.2020.0013)

- [Faludi AA et al. Atualização da Diretriz Brasileira de Dislipidemias e Prevenção da Aterosclerose – 2017. Arq Bras Cardiol.](https://doi.org/10.5935/abc.20170121)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Dokumentierte Ergebnisse

Die folgenden Angaben bewahren die Ausgaben der Methode für synthetische Beispiele. Sie stellen keine unabhängige klinische Validierung dar.

### 1

Vergleichen Sie mit dem Zielwert Ihres kardiovaskulären Risikos

| Ergebnisdetails | |
| --- | --- |
| Nicht-HDL-Cholesterin | 150 mg/dL |
| LDL-C (Sampson/NIH) | 123 mg/dL |
| LDL-c (Friedewald) | 120 mg/dL |


### 2

Vergleichen Sie mit dem Zielwert Ihres kardiovaskulären Risikos

| Ergebnisdetails | |
| --- | --- |
| Nicht-HDL-Cholesterin | 210 mg/dL |
| LDL-C (Sampson/NIH) | 129 mg/dL |
| LDL-c (Friedewald) | nicht anwendbar (TG ≥ 400) |

Triglyzeride ≥ 400 mg/dL: Friedewald nicht verwenden.

