# ログイン

Google認証を使用したログイン機能。ログインすることで[共有](../../cases/edit/share)機能が利用可能

## ログインモーダル {: #login-modal}

ヘッダーのログインボタン押下で表示される。

<img src="../../assets/images/login_modal.png" width="500" style="display: block;"/>

| 番号 | 機能 | 詳細 |
| ---- | ---- | ---- |
| 1 | Log in ボタン | Googleアカウントのログイン認証画面に遷移する |
| 2 | Sign up ボタン | [新規ユーザー登録画面（Googleフォーム）](#sign-up)に遷移する |
| 3 | 機能説明 | ログイン後に利用できる機能の説明を多言語で表示する |

- Log inまたはSign upの選択時には離脱アラートが表示される
- 選択後は同ブラウザで遷移する為、作業中のデータは破棄される

<br>
### 機能説明の文言

<table>
  <thead>
    <tr>
      <th style="min-width: 300px;">JA</th>
      <th style="min-width: 300px;">EN</th>
      <th style="min-width: 300px;">KO</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="white-space: normal;">
        DiseaseSearch、CaseSharing、PanelSearchのログインにはGoogle認証を使用しています。一度ログインすると以下のサービスをご利用いただけます。<br>
        <ul>
          <li>CaseSharing：症例マッチング機能</li>
        </ul>
      </td>
      <td style="white-space: normal;">
        DiseaseSearch, CaseSharing, and PanelSearch support Google Login. Log in once to access all of these services.<br>
        <ul>
          <li>CaseSharing: Case Matching</li>
        </ul>
      </td>
      <td style="white-space: normal;">
        DiseaseSearch, CaseSharing, PanelSearch 로그인에 Google 인증을 사용합니다. 한 번의 로그인으로 다음 서비스들을 모두 이용하실 수 있습니다.<br>
        <ul>
          <li>CaseSharing: 증례 매칭(Case Matching)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## ユーザー登録 {: #sign-up}

Googleフォームで登録内容を入力して送信する。

<img src="../../assets/images/signup_form.png" width="500" />

フォーム送信後はメールアドレス認証用のメールが送信されるので、メールアドレスの確認をすることでログイン機能が利用できるようになる

<br>

## ログイン後の変化

ログイン状態によって以下の表示が変わる。

| 要素 | 未ログイン | ログイン済み |
| ---- | ---- | ---- |
| ヘッダーの右端 | ログインボタンを表示 | <ul>「My page」ドロップダウンメニューを表示（下記が可能）<li>[ユーザー情報](#user-information)ページへの遷移</li><li>ログアウト</li></ul><br><img src="../../assets/images/mypage_dropdown_menu.png" /> |
| 症例編集モーダルの[共有](../../cases/edit/share)タブ | 非表示 | 表示 |
| 症例一覧の share_id 列 | 非表示（ファイル読み込みデータに含まれていても非表示） | 表示<br>項目追加からの選択・追加も可能 |

## ユーザー情報 {: #user-information}

ユーザー情報の確認、編集、削除が可能。

<img src="../../assets/images/user_information.png" width="700" />

### Edit

Googleアカウントを除く、ユーザー情報を編集可能。

<img src="../../assets/images/user_information_edit.png" width="700" />

### Delete

確認モーダルが開き、ユーザーアカウントの削除が可能。<br>
ただし、削除後に同じGoogleアカウントで再登録は不可。

<img src="../../assets/images/user_delete_modal.png" />
