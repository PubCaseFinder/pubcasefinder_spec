# 症例情報を結合する

画面左部メニューバーの「File merge」から json ファイルを読み込むと、現在の編集中の Cases のデータを残したまま、読み込んだ症例データを追加します。<br />
読み込まれた症例データは、現在の編集中の Cases の症例データの下に追加されます。

<img style="width: 100%" src="../../assets/images/PubCaseFinder_fig-2_20230728_mark_file_merge.png">

読み込むことができるファイルは以下の形式です。

| 番号 | 機能 | 詳細                                                                                                                            |
| ---- | ---- | ------------------------------------------------------------------------------------------------------------------------------- |
| 1    | json | データを編集・保存するのに一般的な形式です。読み込んだ json ファイルは現在の編集中の Cases のデータに結合させることができます。 |

## File merge 確認アラート

「File merge」から症例情報データを結合しようとすると、データを結合する前に確認アラートを表示します。

<img style="width: 500px" src="../../assets/images/confirm_file_merge_modal.png">
