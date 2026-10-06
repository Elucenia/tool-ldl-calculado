<!-- ELUCENIA technical documentation · ldl-calculado · zh · no clinical/professional/rights approval -->

# 计算 LDL 胆固醇

[条件、来源与许可](https://elucenia.org/zh/tools/ldl-calculado)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 总胆固醇

`ct`

mg/dL · 范围: 50–800

### HDL 胆固醇

`hdl`

mg/dL · 范围: 5–200

### 甘油三酯

`tg`

mg/dL · 范围: 10–3000

## 方法版本

Friedewald 1972 TG\<400和Sampson NIH 2020 TG≤800；系数0.948/0.971/8.56/2140/16100/9.44

## 已记录的公式

非HDL-C = TC − HDL

Friedewald: LDL = TC − HDL − TG ÷ 5 (适用于TG \< 400 mg/dL)

Sampson (NIH 2020): LDL = TC/0.948 − HDL/0.971 − (TG/8.56 + TG × 非HDL/2140 − TG²/16100) − 9.44 (适用至TG 800 mg/dL)

## 限制与适用人群

Sampson 2020评估了甘油三酯达800 mg/dL时的LDL胆固醇估计；排除了III型高脂蛋白血症患者。开发样本中高甘油三酯血症较常见，并在其他人群中进行了外部验证。公式估计LDL胆固醇，而不是直接测量。其限值不能移用于Friedewald公式；应保留所选变体、单位及各方法所列甘油三酯适用范围。

## 参考文献

- [Friedewald WT, Levy RI, Fredrickson DS. Estimation of the concentration of low-density lipoprotein cholesterol in plasma, without use of the preparative ultracentrifuge. Clin Chem, 1972.](https://doi.org/10.1093/clinchem/18.6.499)

- [Sampson M et al. A new equation for calculation of low-density lipoprotein cholesterol in patients with normolipidemia and/or hypertriglyceridemia. JAMA Cardiol, 2020.](https://doi.org/10.1001/jamacardio.2020.0013)

- [Faludi AA et al. Atualização da Diretriz Brasileira de Dislipidemias e Prevenção da Aterosclerose – 2017. Arq Bras Cardiol.](https://doi.org/10.5935/abc.20170121)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7240357/)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026

## 已记录的结果

以下信息保留该方法对合成示例的输出，不构成独立的临床验证。

### 1

与您的心血管风险目标比较

| 结果详情 | |
| --- | --- |
| 非 HDL 胆固醇 | 150 mg/dL |
| LDL-c (Sampson/NIH) | 123 mg/dL |
| LDL-c（Friedewald） | 120 mg/dL |


### 2

与您的心血管风险目标比较

| 结果详情 | |
| --- | --- |
| 非 HDL 胆固醇 | 210 mg/dL |
| LDL-c (Sampson/NIH) | 129 mg/dL |
| LDL-c（Friedewald） | 不适用 (TG ≥ 400) |

甘油三酯 ≥ 400 mg/dL：不要使用 Friedewald。

