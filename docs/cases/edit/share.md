# 共有

症例情報を CaseSharing Database に登録し、他ユーザーの症例とのマッチングを行う機能。<br>
[ログイン](/overall-structure/login)済みの場合のみ症例編集モーダルに表示される。

## 画面構成

共有タブを開くと「CaseSharing Database」のヘッダーが表示され、画面内に「Submission」「Match Report」の2つのサブタブがある。

## Submission タブ {: #submission}

症例情報の登録・編集・削除を行うタブ。

<img src="../../../assets/images/share_tab.png" width="700" style="display: block;"/>

<br>

### タブラベルのステータス表示

初回登録前はステータスが表示されない。<br>
登録済みの場合は「Submission / Active」または「Submission / Suspended」と表示される。

### アクションボタン

確認モード（非編集時）のみ表示される。

| 機能 | 詳細 |
| ---- | ---- |
| Active / Suspended ボタン | サブミッションのマッチング対象ステータスを切り替える<br>Active：マッチング対象に含まれる。Match Report タブのラベルにマッチ件数がバッジで表示される<br>Suspended：マッチング対象から外れる。マッチ件数バッジは非表示 |
| Edit ボタン | 編集モードに切り替える |

### Submission Identification

| 項目名 | 詳細 | 初期値 | 備考 |
| ---- | ---- | ---- | ---- |
| Share ID | サブミッションの識別ID | 症例の PCF No. | 読み取り専用 |
| Submitter e-mail | 提出者のメールアドレス | ログインユーザーのメールアドレス（初回登録時のみ） | 必須 |
| Submitter first name | 提出者の名 | ログインユーザーの名（初回登録時のみ） | 必須 |
| Submitter last name | 提出者の姓 | ログインユーザーの姓（初回登録時のみ） | 必須 |
| Submitter institution | 提出者の所属機関 | ログインユーザーの所属機関（初回登録時のみ） | 必須 |

確認モードでは提出者情報を「{メール} - {名} {姓} - {所属機関}」の形式で1行表示する。

### Medical Info

症例の疾患情報をチェックボックスで選択する。チェックされた項目のみマッチングに使用される。

疾患情報は症例の以下の項目から取得される。

| セクション名 | 対応する症例項目 |
| ---- | ---- |
| Suspected Disease Name | 疑い病名（medical_suspected_disease_name） |
| Clinical Diagnosis | 臨床診断（medical_clinical_diagnosis_name） |
| Final Diagnosis | 確定診断（medical_final_diagnosis_name） |

- 「Select All」チェックボックスで全選択・全解除が可能
- 症例に該当データがないセクションは表示されない
- 確認モードではチェックされた項目のみ表示される

<br>
### Genotype Info

症例の遺伝子情報をチェックボックスで選択する。チェックされた項目のみマッチングに使用される。

遺伝子情報は症例の以下の項目から取得される。

| 表示ラベル | 対応する症例項目 |
| ---- | ---- |
| Gene Symbol | genotype_gene |
| Ensemble ID | genotype_ensembl_id |
| NCBI Gene ID | genotype_ncbi_gene_id |

- 各遺伝子エントリーは Gene Symbol / Ensemble ID / NCBI Gene ID をセットで表示
- 症例に該当データがない場合は表示されない
- 確認モードではチェックされた項目のみ表示される

<br>
### Matching Rules

Medical Info と Genotype Info それぞれについてマッチングルールを設定する。<br>
セクションタイトルの「?」アイコンにマウスオーバーすることでルールの説明が表示される。

| ルール | 説明（JA） |
| ---- | ---- |
| Required | 絶対条件（これが一致しないとマッチングなし） |
| Optional | 両方が Optional のときのみ有効 — どちらか一方が一致すればマッチ |
| Ignored | 無視（そもそも判定に使わない） |

初期値はいずれも「Ignored」。<br>
バリデーション：Medical Info と Genotype Info が両方 Ignored の場合、保存ボタンが非活性になる。

### Other

| 項目名 | 詳細 | 初期値 |
| ---- | ---- | ---- |
| Comment | サブミッションに関する補足情報 | 空文字 |

テキストエリアで入力する。最大500文字。<br>
確認モードでは改行をそのまま表示する。

### Submission confirmation & matching

編集モードのみ表示される。

| 機能 | 詳細 |
| ---- | ---- |
| Match against チェックボックス | 「Match against other CaseSharing submissions when this submission is saved」<br>保存時に他のサブミッションとのマッチングを実行することへの確認チェックボックス。初期値：チェックあり |
| ファイル保存確認チェックボックス | 「I understand that a window will automatically open after Submit to save the Submission ID in the JSON file.」<br>保存後に JSON ファイルの保存ウィンドウが開くことへの確認チェックボックス。このチェックがないと保存ボタンが非活性 |
| Submit & Download File ボタン | 初回登録時に表示。サブミッションを新規登録し JSON ファイルを保存する |
| Save & Download File ボタン | 2回目以降の編集時に表示。サブミッションを更新し JSON ファイルを保存する |
| Cancel ボタン | 編集内容を破棄して確認モードに戻る |
| Delete submission ボタン | サブミッションの削除確認モーダルを表示する |

#### 保存後の動作

- 症例データの `share_id` に Share ID（PCF No.）が書き込まれる
- 症例データの `submission_id` にサブミッション ID が書き込まれる
- ログイン済みの場合、症例一覧テーブルに share_id 列が追加される
- JSON ファイルの保存ウィンドウが自動で開く

<br>
#### 削除確認モーダル

| 機能 | 詳細 |
| ---- | ---- |
| タイトル | 「Submissionの削除 & JSONの上書き保存」（JA） |
| メッセージ | 「サブミッション情報を削除しますか？削除すると、サブミッションに紐づくIDがクリアされた新しいJSONファイルが保存されます。」（JA） |
| Cancel ボタン | モーダルを閉じる |
| Delete & Download JSON ボタン | サブミッションを削除し JSON ファイルを保存する |

#### 削除後の動作

- 症例データの `share_id` と `submission_id` が削除される
- JSON ファイルが自動で上書き保存される（保存ウィンドウが開く）
- フォームが初期状態にリセットされ、編集モードに移行する

<br>
#### 症例削除との関係

サブミッションに紐づいた症例は、症例一覧から直接削除できない。<br>
削除しようとすると以下のアラートが表示される。

「この症例はサブミッションと紐づいているため削除できません。削除するには、共有タブからサブミッションを削除してから症例を削除してください。」（JA）

### ローカルデータ変更時の挙動

症例一覧で症例情報を変更した後に共有タブを開き、ローカルの症例データとサーバー上のサブミッションデータに差分が検出された場合、以下のアラートが表示されて編集モードに移行する。

「症例情報が変更されました。Editモードに移行します。」（JA）

---

## Match Report タブ {: #match-report}

自分のサブミッションにマッチした他ユーザーの症例の一覧を表示するタブ。<br>

<img src="../../../assets/images/maching_tab.png" width="700" style="display: block;"/>

<br>
Submission タブを開いた際にデータが取得される。

### 表示内容

マッチ件数が「Match: {件数}」として表示される。<br>
マッチがない場合は「No matches found for this submission.」と表示される。

各マッチには以下の情報が表示される。

**マッチした症例の登録者情報（Matched case owner information）**

| 項目 | 詳細 |
| ---- | ---- |
| Name | 相手の姓名（first name + last name） |
| Institution | 相手の所属機関 |
| Email | 相手のメールアドレス。押下でメーラーが開く |

**比較テーブル**

自分の症例（My case）とマッチした症例（Matched case）を並べて表示する。

| 列 | 詳細 |
| ---- | ---- |
| Share ID | 各サブミッションの Share ID |
| Gene Symbols | チェックされた遺伝子シンボル |
| Ensembl IDs | チェックされた Ensembl ID |
| NCBI Gene IDs | チェックされた NCBI Gene ID |
| Suspected Diseases | チェックされた疑い病名（MONDO ID + 病名） |
| Clinical Diagnoses | チェックされた臨床診断（MONDO ID + 病名） |
| Final Diagnoses | チェックされた確定診断（MONDO ID + 病名） |
| comment | コメント |

### Email リンク

Email 押下でメーラーが開く。以下の情報がメール本文にテンプレートとして入力される。

- 自分の症例情報（Share ID・遺伝子情報・疾患情報・コメント）
- 相手の症例情報（Share ID・遺伝子情報・疾患情報・コメント）
