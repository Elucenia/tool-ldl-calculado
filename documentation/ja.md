<!-- ELUCENIA technical documentation · ldl-calculado · ja · no clinical/professional/rights approval -->

# 計算LDLコレステロール

[条件・出典・許諾](https://elucenia.org/ja/tools/ldl-calculado)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 総コレステロール

`ct`

mg/dL · 範囲: 50–800

### HDLコレステロール

`hdl`

mg/dL · 範囲: 5–200

### 中性脂肪

`tg`

mg/dL · 範囲: 10–3000

## 方法の版

Friedewald 1972 TG\<400とSampson NIH 2020 TG≤800；係数0.948/0.971/8.56/2140/16100/9.44

## 記載された計算式

非HDL-C = TC − HDL

Friedewald: LDL = TC − HDL − TG ÷ 5 (TG \< 400 mg/dLの場合に有効)

Sampson (NIH 2020): LDL = TC/0.948 − HDL/0.971 − (TG/8.56 + TG × 非HDL/2140 − TG²/16100) − 9.44 (TG 800 mg/dLまで有効)

## 限界・対象集団

Sampson 2020は、トリグリセリド800 mg/dLまでのLDLコレステロールの推定を評価し、III型高脂血症の人を除外しました。開発標本には高トリグリセリド血症が多く、他の集団で外部検証が行われました。式はLDLコレステロールを直接測定するのではなく、推定します。その限界をFriedewaldの式へ転用してはいけません。選択した変法、単位、各方法で示されたトリグリセリドの範囲を維持してください。

## 参考文献

- [Friedewald WT, Levy RI, Fredrickson DS. Estimation of the concentration of low-density lipoprotein cholesterol in plasma, without use of the preparative ultracentrifuge. Clin Chem, 1972.](https://doi.org/10.1093/clinchem/18.6.499)

- [Sampson M et al. A new equation for calculation of low-density lipoprotein cholesterol in patients with normolipidemia and/or hypertriglyceridemia. JAMA Cardiol, 2020.](https://doi.org/10.1001/jamacardio.2020.0013)

- [Faludi AA et al. Atualização da Diretriz Brasileira de Dislipidemias e Prevenção da Aterosclerose – 2017. Arq Bras Cardiol.](https://doi.org/10.5935/abc.20170121)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
