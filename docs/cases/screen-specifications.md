# 画面仕様

![Casesのスクリーンショット](/assets/images/cases_20240804.png)

<!-- TODO: Cases編集の家系、検体・検査、登録がファイル作成したら7.症例編集の詳細にリンク追加 -->

| 番号 | 機能 | 詳細 |
| ---- | ---- | ---- |
| 1 | 表の症例数 | 症例数の更新に応じて自動で表示数を更新 |
| 2 | リロード | 確認アラートを表示し、「OK」押下時のみページのリロードを行う<br>リロード後は一覧表の内容は初期化 |
| 3 | [キーワード検索](/cases/operations/keyword-search) | 入力したキーワードを含む症例を絞り込む |
| 4 | [項目追加](/cases/operations/add-items) | 項目の編集ドロップダウンを開く<br>項目の新規作成、表示項目の追加や削除が可能 |
| 5 | [症例追加](/cases/operations/add-case) | 一覧表の後ろに症例を追加 |
| 6 | 症例削除 | 下記文言の確認アラートを表示し、「OK」押下時のみ実行<br>「症例ID {caseId} を削除しますか？」 |
| 7 | 症例編集 | 症例の編集モーダルが開く<br>各項目の編集内容詳細は下記参照<br><ul><li>[症例基本情報](/cases/edit/case-basic-information)</li><li>[診療](/cases/edit/medical)</li><li>[表現型](/cases/edit/phenotype)</li><li>[遺伝型](/cases/edit/genotype)</li><li>家系</li><li>検体・検査</li><li>登録</li></ul> |
| 8 | [列の操作](/cases/operations/operation-column) | 列の操作一覧が開く<br>列のデータの一括操作やフィルターをかけることが可能 |
| 9 | File open | 枠内にファイルをドラッグ&ドロップすることでデータファイルを取り込み<br>編集モーダルを開いている場合はドラッグ&ドロップしてもデータファイルの取り込みは不可 |
|  | [その他の一覧表操作](/cases/operations/other) | 一覧表でのデータ編集やその他操作 |


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
      <td>確認アラート</td>
      <td><strong>症例ID {caseId} を削除しますか？</strong></td>
      <td>Are you sure you want to delete case {caseId}?</td>
      <td>케이스 ID {caseId}를 삭제하시겠습니까?</td>
    </tr>
  </tbody>
</table>