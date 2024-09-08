# 症状

このグラフでは、疾患に紐づく症状とその発症/治癒年齢の平均値を表す。また、バーの色で重症度を示すことでどの症状が何歳の時にどれくらいの重症度で発症したかを読み取ることができる。

![症状グラフ](../../assets/images/stats_symptons.png)

## データ仕様
| 項目名 | 説明 |
| ---- | ---- |
| データ項目 | 発症年齢（phenotype_age_onset）、治癒年齢（phenotype_resolution）、診断名（medical_final_diagnosis）、症状（phenotype_hpo_label）、重症度（phenotype_severity） |
| データ形式 | 発症年齢はYMD表記の配列、治癒年齢はYMD表記の配列、診断名は文字列、症状は各言語文字列で定義したオブジェクトの配列 |

データ例）
```
{
  "phenotype_age_onset": [
      "5Y",
      "13Y",
      "49Y"
  ],
  "phenotype_resolution": [
      "10Y7M",
      "44Y",
      "55Y"
  ],
  "medical_final_diagnosis": "marfan syndrome",
  "phenotype_hpo_label": [
      {
          "name_en": "Long fingers",
          "name_ja": "長い指",
          "name_ko": "",
          "name_zh": "",
          "name_zhcht": ""
      },
      {
          "name_en": "Reduced visual acuity",
          "name_ja": "中心視力減少",
          "name_ko": "",
          "name_zh": "",
          "name_zhcht": ""
      },
      {
          "name_en": "Aortic aneurysm",
          "name_ja": "大動脈瘤",
          "name_ko": "",
          "name_zh": "",
          "name_zhcht": ""
      }
  ],
  "phenotype_severity": [
      "moderate",
      "profound",
      "borderline"
  ]
}
```

## グラフ仕様
| 項目名 | 説明 |
| ---- | ---- |
| グラフの種類 | 水平棒グラフ |
| 軸の設定 | X軸（横軸）: 年代。Y軸（縦軸）: 症状。 |
| 凡例 | 重症度（mild〜profound）の色分布をグラデーション表示。重症度が高くなるにつれて青から赤に変化 |
| ツールチップ | ユーザーが特定のバーにマウスオーバーした際、症状と始点・終点の値を表示 |
| 疾患名セレクトボックス | グラフ中央上部に位置するセレクトボックスから表示する疾患が選択できる |
