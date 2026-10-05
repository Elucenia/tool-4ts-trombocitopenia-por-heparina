<!-- ELUCENIA technical documentation · 4ts-trombocitopenia-por-heparina · ja · no clinical/professional/rights approval -->

# 4Tスコア（ヘパリン起因性血小板減少症）

[条件・出典・許諾](https://elucenia.org/ja/tools/4ts-trombocitopenia-por-heparina)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 血小板減少

`trombo`

- `0` — 低下\<30%または最低値\<10,000/µL
- `1` — 低下30%～50%または最低値10,000～19,000/µL
- `2` — 低下\>50%かつ最低値≥20,000/µL

### 血小板減少の時期

`tempo`

- `0` — 最近の曝露なしで4日目より前に低下
- `1` — 5～10日目と整合するが不確か；10日目より後；または30～100日前にヘパリン曝露があり≤1日
- `2` — 5～10日目の明確な発症，または過去30日以内のヘパリン曝露があり≤1日

### 血栓またはその他の続発症

`trombose`

- `0` — なし
- `1` — 進行性または再発性血栓症，非壊死性皮膚病変，または血栓症疑い
- `2` — 新たに確認された血栓症，皮膚壊死，またはボーラス投与後の全身反応

### 血小板減少の他の原因

`outras`

- `0` — 確定
- `1` — 可能性あり
- `2` — 明らかなものなし

## 方法の版

4Ts/Lo 2006：4領域0–2、合計0–8、ASH 2018に基づく

## 記載された計算式

4項目、各0～2：T血小板減少、T時期、T血栓、T他原因。最高8。

## 限界・対象集団

ヘパリン曝露後にヘパリン起因性血小板減少症（HIT）が疑われる場合の臨床的検査前確率を推定します。血小板の推移、時間的経過、血栓症、他の原因に関する病歴に依存します。結果はHITを確定するものではなく、予測値は研究された状況によって異なりました。

## 参考文献

- [Lo GK et al. Evaluation of pretest clinical score (4 T's) for the diagnosis of heparin-induced thrombocytopenia in two clinical settings. J Thromb Haemost, 2006.](https://doi.org/10.1111/j.1538-7836.2006.01787.x)

- [Cuker A et al. American Society of Hematology 2018 guidelines for management of venous thromboembolism: heparin-induced thrombocytopenia. Blood Adv, 2018.](https://doi.org/10.1182/bloodadvances.2018024489)

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
