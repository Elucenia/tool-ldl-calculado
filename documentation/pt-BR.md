<!-- ELUCENIA technical documentation · ldl-calculado · pt-BR · no clinical/professional/rights approval -->

# LDL-colesterol calculado

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/ldl-calculado)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Colesterol total

`ct`

mg/dL · intervalo: 50–800

### HDL-colesterol

`hdl`

mg/dL · intervalo: 5–200

### Triglicerídeos

`tg`

mg/dL · intervalo: 10–3000

## Edição do método

Friedewald 1972 TG\<400 e Sampson NIH 2020 TG≤800; coeficientes 0,948/0,971/8,56/2140/16100/9,44

## Fórmula documentada

Não-HDL-c = CT − HDL

Friedewald: LDL = CT − HDL − TG ÷ 5 (válida com TG \< 400 mg/dL)

Sampson (NIH 2020): LDL = CT/0,948 − HDL/0,971 − (TG/8,56 + TG × não-HDL/2140 − TG²/16100) − 9,44 (válida até TG 800 mg/dL)

## Limites e população

Sampson 2020 avaliou a estimativa de LDL-colesterol até triglicerídeos de 800 mg/dL; pessoas com hiperlipidemia tipo III foram excluídas. A amostra de desenvolvimento teve alta frequência de hipertrigliceridemia, com validação externa em outras populações. A fórmula estima, em vez de medir diretamente, o LDL-colesterol. Seus limites não devem ser transferidos à fórmula de Friedewald; preserve a variante escolhida, a unidade e o domínio de triglicerídeos informado para cada método.

## Referências

- [Friedewald WT, Levy RI, Fredrickson DS. Estimation of the concentration of low-density lipoprotein cholesterol in plasma, without use of the preparative ultracentrifuge. Clin Chem, 1972.](https://doi.org/10.1093/clinchem/18.6.499)

- [Sampson M et al. A new equation for calculation of low-density lipoprotein cholesterol in patients with normolipidemia and/or hypertriglyceridemia. JAMA Cardiol, 2020.](https://doi.org/10.1001/jamacardio.2020.0013)

- [Faludi AA et al. Atualização da Diretriz Brasileira de Dislipidemias e Prevenção da Aterosclerose – 2017. Arq Bras Cardiol.](https://doi.org/10.5935/abc.20170121)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

As informações abaixo preservam as saídas do método para exemplos sintéticos. Não constituem validação clínica independente.

### 1

Compare com a meta do seu risco cardiovascular

| Detalhes do resultado | |
| --- | --- |
| Colesterol não-HDL | 150 mg/dL |
| LDL-c (Sampson/NIH) | 123 mg/dL |
| LDL-c (Friedewald) | 120 mg/dL |


### 2

Compare com a meta do seu risco cardiovascular

| Detalhes do resultado | |
| --- | --- |
| Colesterol não-HDL | 210 mg/dL |
| LDL-c (Sampson/NIH) | 129 mg/dL |
| LDL-c (Friedewald) | não aplicável (TG ≥ 400) |

Triglicerídeos ≥ 400 mg/dL: não use Friedewald.

