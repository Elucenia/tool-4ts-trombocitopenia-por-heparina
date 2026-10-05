<!-- ELUCENIA technical documentation · 4ts-trombocitopenia-por-heparina · zh · no clinical/professional/rights approval -->

# 4T 评分（肝素诱导的血小板减少症）

[条件、来源与许可](https://elucenia.org/zh/tools/4ts-trombocitopenia-por-heparina)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 血小板减少

`trombo`

- `0` — 下降\<30%或最低值\<10,000/µL
- `1` — 下降30%至50%或最低值10,000至19,000/µL
- `2` — 下降\>50%且最低值≥20,000/µL

### 血小板下降时间

`tempo`

- `0` — 第4天前下降，无近期暴露
- `1` — 符合第5–10天但不确定；第10天之后；或≤1天，且30至100天前接触过肝素
- `2` — 明确在第5至第10天出现，或≤1天且过去30天接触过肝素

### 血栓或其他后果

`trombose`

- `0` — 无
- `1` — 进展性或复发性血栓，非坏死性皮损，或疑似血栓
- `2` — 新发确诊血栓、皮肤坏死或静脉推注后全身反应

### 血小板减少的其他原因

`outras`

- `0` — 确定
- `1` — 可能
- `2` — 无明显原因

## 方法版本

4Ts/Lo 2006：4领域0–2，总分0–8；ASH 2018背景

## 已记录的公式

四项，各0至2：T血小板减少 · T时间 · T血栓 · T其他原因。最高8。

## 限制与适用人群

用于在肝素暴露后疑似肝素诱导的血小板减少症（HIT）时估计临床验前概率。它依赖血小板变化、时间关系、血栓事件及其他可能病因的病史。结果不能确诊HIT；预测值在所研究的不同情境间存在差异。

## 参考文献

- [Lo GK et al. Evaluation of pretest clinical score (4 T's) for the diagnosis of heparin-induced thrombocytopenia in two clinical settings. J Thromb Haemost, 2006.](https://doi.org/10.1111/j.1538-7836.2006.01787.x)

- [Cuker A et al. American Society of Hematology 2018 guidelines for management of venous thromboembolism: heparin-induced thrombocytopenia. Blood Adv, 2018.](https://doi.org/10.1182/bloodadvances.2018024489)

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
