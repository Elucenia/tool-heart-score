<!-- ELUCENIA technical documentation · heart-score · zh · no clinical/professional/rights approval -->

# HEART 评分

[条件、来源与许可](https://elucenia.org/zh/tools/heart-score)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 病史

`h`

- `0` — 低度可疑
- `1` — 中度可疑
- `2` — 高度可疑

### ECG

`e`

- `0` — 正常
- `1` — 非特异性复极改变
- `2` — 显著ST段压低

### 年龄

`a`

- `0` — ≤ 45岁
- `1` — \> 45岁且 \< 65岁
- `2` — ≥ 65 岁

### 危险因素

`r`

- `0` — 无
- `1` — 1或2
- `2` — ≥3或已知动脉粥样硬化性疾病

### 肌钙蛋白

`t`

- `0` — ≤正常上限
- `1` — \> 正常上限的1倍且 \< 3倍
- `2` — ≥ 正常上限的3倍

## 方法版本

HEART/Backus 2013：5个组成部分各计0–2分，总分0–10；年龄≤45岁、\>45岁且\<65岁、≥65岁；肌钙蛋白≤正常上限、\>正常上限的1倍且\<3倍、≥正常上限的3倍；不等同于采用连续评估的HEART Pathway

## 已记录的公式

每项0至2分：H病史、E心电图、A年龄、R危险因素、T肌钙蛋白。总计0至10。

危险因素：高血压、血脂异常、糖尿病、肥胖（BMI\>30）、当前或近期吸烟、早发冠心病家族史。

## 限制与适用人群

原始HEART评分在急诊胸痛、疑似非ST段抬高型急性冠脉综合征患者中研究。低评分不意味着零风险，原始总分也不等同于包含序贯评估的HEART Pathway。出院安全性、肌钙蛋白采样时间及排除条件须依据相应方案。

## 参考文献

- [Six AJ, Backus BE, Kelder JC. Chest pain in the emergency room: value of the HEART score. Neth Heart J, 2008.](https://doi.org/10.1007/BF03086144)

- [Backus BE et al. A prospective validation of the HEART score for chest pain patients at the emergency department. Int J Cardiol, 2013.](https://doi.org/10.1016/j.ijcard.2013.01.255)

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
