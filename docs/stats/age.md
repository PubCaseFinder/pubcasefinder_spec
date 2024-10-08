# 年齢

![年齢グラフ](../../assets/images/stats_age.png)

## データ仕様
| 項目名 | 説明 |
| ---- | ---- |
| データ項目 | 年代（case_age）、症例数 |
| データ形式 | 年齢はYMD表記（例: 30Y1M2D）、人数は正の整数 |
| 年齢範囲 | グラフに表示する症例数の最大値は対象データに応じて動的に設定される。年齢は10歳区切り（例: 10-19, 20-29）で集計し、60代以降は一区切りとする |

## グラフ仕様
| 項目名 | 説明 |
| ---- | ---- |
| グラフの種類 | 縦棒グラフ（ヒストグラム形式） |
| 軸の設定 | X軸（横軸）: 年代。各バーは特定の年齢範囲（例: 10歳区切り）を表します。Y軸（縦軸）: 症例数。各バーの高さが該当する年代の人数を示します。 |
| 凡例 | 男性（male）、女性（female）、その他（other）、不明（unknown） |
| ツールチップ | ユーザーが特定のバーにマウスオーバーした際、年齢範囲と対応する人数を表示 |
