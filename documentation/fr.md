<!-- ELUCENIA technical documentation · ldl-calculado · fr · no clinical/professional/rights approval -->

# Cholestérol LDL calculé

[conditions, sources et autorisations](https://elucenia.org/fr/outils/ldl-calculado)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Cholestérol total

`ct`

mg/dL · intervalle: 50–800

### Cholestérol HDL

`hdl`

mg/dL · intervalle: 5–200

### Triglycérides

`tg`

mg/dL · intervalle: 10–3000

## Édition de la méthode

Friedewald 1972 TG\<400 et Sampson NIH 2020 TG≤800 ; coefficients 0,948/0,971/8,56/2140/16100/9,44

## Formule documentée

Non-HDL-c = CT − HDL

Friedewald: LDL = CT − HDL − TG ÷ 5 (valide avec TG \< 400 mg/dL)

Sampson (NIH 2020): LDL = CT/0,948 − HDL/0,971 − (TG/8,56 + TG × non-HDL/2140 − TG²/16100) − 9,44 (valide jusqu’à TG 800 mg/dL)

## Limites et population

Sampson 2020 a évalué l’estimation du LDL-cholestérol jusqu’à des triglycérides de 800 mg/dL ; les personnes présentant une hyperlipidémie de type III étaient exclues. L’échantillon de développement comportait une fréquence élevée d’hypertriglycéridémie, avec validation externe dans d’autres populations. La formule estime le LDL-cholestérol plutôt que de le mesurer directement. Ses limites ne doivent pas être transférées à la formule de Friedewald ; conservez la variante choisie, l’unité et le domaine de triglycérides indiqué pour chaque méthode.

## Références

- [Friedewald WT, Levy RI, Fredrickson DS. Estimation of the concentration of low-density lipoprotein cholesterol in plasma, without use of the preparative ultracentrifuge. Clin Chem, 1972.](https://doi.org/10.1093/clinchem/18.6.499)

- [Sampson M et al. A new equation for calculation of low-density lipoprotein cholesterol in patients with normolipidemia and/or hypertriglyceridemia. JAMA Cardiol, 2020.](https://doi.org/10.1001/jamacardio.2020.0013)

- [Faludi AA et al. Atualização da Diretriz Brasileira de Dislipidemias e Prevenção da Aterosclerose – 2017. Arq Bras Cardiol.](https://doi.org/10.5935/abc.20170121)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Résultats documentés

Les informations ci-dessous conservent les sorties de la méthode pour des exemples synthétiques. Elles ne constituent pas une validation clinique indépendante.

### 1

Comparer avec la cible de votre risque cardiovasculaire

| Détails du résultat | |
| --- | --- |
| Cholestérol non-HDL | 150 mg/dL |
| LDL-c (Sampson/NIH) | 123 mg/dL |
| LDL-c (Friedewald) | 120 mg/dL |


### 2

Comparer avec la cible de votre risque cardiovasculaire

| Détails du résultat | |
| --- | --- |
| Cholestérol non-HDL | 210 mg/dL |
| LDL-c (Sampson/NIH) | 129 mg/dL |
| LDL-c (Friedewald) | non applicable (TG ≥ 400) |

Triglycérides ≥ 400 mg/dL : n’utilisez pas Friedewald.

