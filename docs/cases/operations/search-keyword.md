#　キーワード検索

## 仕様

- input type="search"の検索フォーム
    - 文字が入力されると検索フォーム内にクリアボタンを表示し、押下すると入力文字をクリア（挙動や表示はブラウザによる）
- プレースホルダーは「キーワード検索」
- 入力途中で検索が実行されないように、一度キーを離してから0.5秒間キーを離す操作がなければ検索実行
    - 入力したキーワードを含む症例を絞り込む
        - 絞り込まれた症例数を検索フォーム内の右側に表示
    - キーワードを含む症例の項目はハイライト
    - キーワードはスペースで区切って複数入力して検索可能
        - 複数キーワードすべてを含む症例を絞り込む
        - ハイライトする項目はキーワードを1つでも含んでいるもの
- 一覧表の検索実行にはHandsontableのPlugin（[search](https://handsontable.com/docs/12.3/javascript-data-grid/api/search/)）を使用
- 一覧表の検索実行後の絞り込み表示にはHandsontableのPlugin（[hiddenRows](https://handsontable.com/docs/12.3/javascript-data-grid/api/hidden-rows/)）を使用

<br>

## 例

### 検索実行前の表示データ

![実行例1](/assets/images/cases_search_keyword01.png)

### 「Aグループ」で検索実行

![実行例2](/assets/images/cases_search_keyword02.png)

### 「Aグループ　母」で検索実行

![実行例3](/assets/images/cases_search_keyword03.png)

---

### 翻訳 {: #translate}
<table>
  <thead>
    <tr>
      <th>種別</th>
      <th>JA</th>
      <th>EN</th>
      <th>KO</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>プレースホルダー</td>
      <td><strong>キーワード検索</strong></td>
      <td>Search keyword</td>
      <td>키워드 검색</td>
    </tr>
  </tbody>
</table>
