# 家系数

![家系数の統計情報](../../assets/images/stats_family_count.png)

## データ仕様
| 表示情報 | 説明 |
| ---- | ---- |
| 家系数 | 家族ID（case_family_id）の種類の数。データがFalsy（nullや空白）の家族IDはカウントされない。 |
| 一番多い家系 | 家族ID（case_family_id）の中で症例数が1番多い家族IDを表示。<br><ul><li>1番多い家族IDが複数ある場合は「,」区切りで表示</li><li>家系数が0の場合は「-」を表示</li></ul> |
