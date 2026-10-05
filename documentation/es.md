<!-- ELUCENIA technical documentation · ldl-calculado · es · no clinical/professional/rights approval -->

# Colesterol LDL calculado

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/ldl-calculado)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Colesterol total

`ct`

mg/dL · intervalo: 50–800

### Colesterol HDL

`hdl`

mg/dL · intervalo: 5–200

### Triglicéridos

`tg`

mg/dL · intervalo: 10–3000

## Edición del método

Friedewald 1972 TG\<400 y Sampson NIH 2020 TG≤800; coeficientes 0,948/0,971/8,56/2140/16100/9,44

## Fórmula documentada

No-HDL-c = CT − HDL

Friedewald: LDL = CT − HDL − TG ÷ 5 (válida con TG \< 400 mg/dL)

Sampson (NIH 2020): LDL = CT/0,948 − HDL/0,971 − (TG/8,56 + TG × no-HDL/2140 − TG²/16100) − 9,44 (válida hasta TG 800 mg/dL)

## Límites y población

Sampson 2020 evaluó la estimación de colesterol LDL hasta triglicéridos de 800 mg/dL; se excluyeron personas con hiperlipidemia de tipo III. La muestra de desarrollo tuvo una alta frecuencia de hipertrigliceridemia, con validación externa en otras poblaciones. La fórmula estima, en lugar de medir directamente, el colesterol LDL. Sus límites no deben trasladarse a la fórmula de Friedewald; conserve la variante elegida, la unidad y el dominio de triglicéridos indicado para cada método.

## Referencias

- [Friedewald WT, Levy RI, Fredrickson DS. Estimation of the concentration of low-density lipoprotein cholesterol in plasma, without use of the preparative ultracentrifuge. Clin Chem, 1972.](https://doi.org/10.1093/clinchem/18.6.499)

- [Sampson M et al. A new equation for calculation of low-density lipoprotein cholesterol in patients with normolipidemia and/or hypertriglyceridemia. JAMA Cardiol, 2020.](https://doi.org/10.1001/jamacardio.2020.0013)

- [Faludi AA et al. Atualização da Diretriz Brasileira de Dislipidemias e Prevenção da Aterosclerose – 2017. Arq Bras Cardiol.](https://doi.org/10.5935/abc.20170121)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
