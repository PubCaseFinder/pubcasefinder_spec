# 症例基本情報

## 大項目

| 項目名 | 説明 |
| ---- | ---- |
| **[ID](#id)** | 症例に紐づく各種ID情報を確認/編集することができます。|
| **[基本情報](#basic-info)** | 症例についての基本情報を編集することができます。|
| **[民族・出生地](#etnicity)** | 症例者のルーツについての情報を編集することができます。|
| **[出生時](#birth-info)** | 症例者の出生時についての情報を編集することができます。|
| **[生殖補助](#assisted-reproduction)** | 症例者の生殖補助についての情報を編集することができます。|
| **[入力者情報](#inputter-info)** | 症例の入力者についての情報を編集することができます。|

---


## ID {: #id}

<table>
  <thead>
    <tr>
      <th rowspan="2">項目名</th>
      <th rowspan="2">ID</th>
      <th rowspan="2">型定義</th>
      <th rowspan="2">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2">初期値</th>
      <th rowspan="2">clearボタン</th>
      <th rowspan="2">deleteボタン</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>PCF No.</strong></td>
      <td>PCFNo</td>
      <td>string</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>P{yyyy}{M}{d}{HH}{mm}{ss}{SSS}{※}</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>※箇所は、ランダムな数値を36進数の文字列にし、3文字目から7文字目までの5文字</td>
    </tr>
    <tr>
      <td><strong>症例ID</strong></td>
      <td>case_id</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>C{※}</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.id. / subject.id / pedigree.persons.individual_id</td>
      <td>※箇所は、「症例が追加される毎にオートインクリメントされるカウント+1」の数値を0埋めした7桁の文字列</td>
    </tr>
    <tr>
      <td><strong>家族ID</strong></td>
      <td>case_family_id</td>
      <td>string</td>
      <td>テキストボックス、セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>id  / pedigree.persons.family_id</td>
      <td>一覧に表示中の家族IDをプルダウンから選択可能</td>
    </tr>
    <tr>
      <td><strong>グループ名</strong></td>
      <td>case_group</td>
      <td>string</td>
      <td>テキストボックス、セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>一覧に表示中のグループIDをプルダウンから選択可能</td>
    </tr>
  </tbody>
</table>

## 基本情報 {: #basic-info}

<table>
  <thead>
    <tr>
      <th rowspan="2">項目名</th>
      <th rowspan="2">ID</th>
      <th rowspan="2">型定義</th>
      <th rowspan="2">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2">初期値</th>
      <th rowspan="2">clearボタン</th>
      <th rowspan="2">deleteボタン</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>続柄</strong></td>
      <td>case_relationship</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>proband_individual</li>
          <li>father</li>
          <li>mother</li>
          <li>parent_unknown</li>
          <li>spouse_proband</li>
          <li>spouse_child</li>
          <li>spouse_sibling</li>
          <li>spouse_uncle_aunt</li>
          <li>sibling</li>
          <li>child</li>
          <li>grandparent_paternal</li>
          <li>grandparent_maternal</li>
          <li>grandparent_unknown</li>
          <li>uncle_paternal</li>
          <li>uncle_maternal</li>
          <li>aunt_paternal</li>
          <li>aunt_maternal</li>
          <li>nephew_niece</li>
          <li>grandchild</li>
          <li>cousin</li>
          <li>unknown</li>
          <li>other_paternal</li>
          <li>other_maternal</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>発端者（本人）</li>
          <li>父</li>
          <li>母</li>
          <li>親（詳細不明）</li>
          <li>本人の配偶者</li>
          <li>子どもの配偶者</li>
          <li>兄弟の配偶者</li>
          <li>おじおばの配偶者</li>
          <li>同胞</li>
          <li>子ども</li>
          <li>祖父母（父方）</li>
          <li>祖父母（母方）</li>
          <li>祖父母（詳細不明）</li>
          <li>おじ（父方）</li>
          <li>おじ（母方）</li>
          <li>おば（父方）</li>
          <li>おば（母方）</li>
          <li>甥姪</li>
          <li>孫</li>
          <li>いとこ</li>
          <li>不明</li>
          <li>その他（父方）</li>
          <li>その他（母方）</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>血縁者の本研究参加の有無</strong></td>
      <td>case_participation_of_relatives_in_this_study</td>
      <td>string</td>
      <td>ラジオボタン        </td>
      <td>
        <ul>
          <li>"not_applicable"</li>
          <li>not_participated</li>
          <li>already_participated</li>
          <li>plan_to_participate</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>なし</li>
          <li>あり</li>
          <li>参加予定</li>
        </ul>
      </td>
      <td>"not_applicable"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>性別</strong></td>
      <td>case_sex</td>
      <td>string</td>
      <td>ラジオボタン        </td>
      <td>
        <ul>
          <li>unknown</li>
          <li>male</li>
          <li>female</li>
          <li>other</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>男性</li>
          <li>女性</li>
          <li>その他</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.subject.sex</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>性別 その他詳細</strong></td>
      <td>case_sex_details</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>性別で「その他」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>発症の有無</strong></td>
      <td>case_presence_or_absence_of_onset</td>
      <td>string</td>
      <td>ラジオボタン        </td>
      <td>
        <ul>
          <li>unknown</li>
          <li>onset</li>
          <li>asymptomatic</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>発症</li>
          <li>未発症</li>
        </ul>
      </td>
      <td>unkown</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>pedigree.persons.affectedStatus</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>状態</strong></td>
      <td>case_life_status</td>
      <td>string</td>
      <td>ラジオボタン        </td>
      <td>
        <ul>
          <li>unknown</li>
          <li>alive</li>
          <li>deceased</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>生存</li>
          <li>故人</li>
        </ul>
      </td>
      <td>unkown</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.subject.vitalStatus.status</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>生年月 (yyyy/mm)</strong></td>
      <td>case_birth</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>1800〜現在の年</li>
          <li>1~12</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>1800〜現在の年</li>
          <li>1~12</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>登録時年齢 (YMD)</strong></td>
      <td>case_age</td>
      <td>string</td>
      <td>テキストボックス (数字)、セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>診察時年齢 (YMD)</strong></td>
      <td>case_age_on_examination</td>
      <td>string</td>
      <td>テキストボックス (数字)、セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.subject.timeAtLastEncounter.age.iso8601duration</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>没年月 (yyyy/mm)</strong></td>
      <td>case_death</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>状態で「故人」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>死因</strong></td>
      <td>case_cause_of_death</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>concerned_disease</li>
          <li>other_disease</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>当該疾患</li>
          <li>当該疾患以外</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>状態で「故人」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>当該疾患以外のときの死因詳細</strong></td>
      <td>case_cause_of_death_details</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>状態で「故人」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>死因ICD-11コード</strong></td>
      <td>case_icd_11_code_of_cause_of_death</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>状態で「故人」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>最終生存確認日 (yyyy/mm/dd)</strong></td>
      <td>case_last_date_of_confirmation_of_survival</td>
      <td>string</td>
      <td>カレンダー選択</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 民族・出生地 {: #etnicity}

<table>
  <thead>
    <tr>
      <th rowspan="2">項目名</th>
      <th rowspan="2">ID</th>
      <th rowspan="2">型定義</th>
      <th rowspan="2">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2">初期値</th>
      <th rowspan="2">clearボタン</th>
      <th rowspan="2">deleteボタン</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>民族 / 集団</strong></td>
      <td>case_ethnicity_group</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>
        <a href="../master#country-master">国マスタ</a>
      </td>
      <td>
        <a href="../master#country-master">国マスタ</a>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>自由記載</strong></td>
      <td>case_free_comment_about_ethnicity_group</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>出生地 国</strong></td>
      <td>case_country_of_birth</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>
        <a href="../master#country-master">国マスタ</a>
      </td>
      <td>
        <a href="../master#country-master">国マスタ</a>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>都道府県</strong></td>
      <td>case_state_of_birth</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>市区町村</strong></td>
      <td>case_city_of_birth</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>自由記載</strong></td>
      <td>case_free_comment_about_birth</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 出生時 {: #birth-info}

<table>
  <thead>
    <tr>
      <th rowspan="2">項目名</th>
      <th rowspan="2">ID</th>
      <th rowspan="2">型定義</th>
      <th rowspan="2">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2">初期値</th>
      <th rowspan="2">clearボタン</th>
      <th rowspan="2">deleteボタン</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>出生前（胎児）の異常の有無</strong></td>
      <td>case_presence_of_prenatal_abnormalities</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>unknown</li>
          <li>absent</li>
          <li>present</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>なし</li>
          <li>あり</li>
        </ul>
      </td>
      <td>"不明"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>異常（黄疸等）の有無</strong></td>
      <td>case_presence_of_abnormalities_at_birth</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>unknown</li>
          <li>absent</li>
          <li>present</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>なし</li>
          <li>あり</li>
        </ul>
      </td>
      <td>"不明"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>医療介助の有無（出産時）</strong></td>
      <td>case_presence_of_medical_assistance_at_birth</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>unknown</li>
          <li>absent</li>
          <li>present</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>なし</li>
          <li>あり</li>
        </ul>
      </td>
      <td>"不明"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>在胎週数 (週)</strong></td>
      <td>case_gestational_age_at_birth</td>
      <td>string</td>
      <td>テキストボックス (数字)</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3"><strong>母親の年齢 (YMD)</strong></td>
      <td rowspan="3">case_age_of_mother_at_birth</td>
      <td rowspan="3">string</td>
      <td>テキストボックス (数字)</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td rowspan="3">
        「{{yyyy}} + Y + {{mm}} + M + {{dd}} + D」の形式でjsonに保存される
      </td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>- ヶ月を選択 -</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>- 日を選択 -</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3"><strong>父親の年齢 (YMD)</strong></td>
      <td rowspan="3">case_age_of_father_at_birth</td>
      <td rowspan="3">string</td>
      <td>テキストボックス (数字)</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td rowspan="3">
        「{{yyyy}} + Y + {{mm}} + M + {{dd}} + D」の形式でjsonに保存される
      </td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>- ヶ月を選択 -</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>- 日を選択 -</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 生殖補助 {: #assisted-reproduction}

<table>
  <thead>
    <tr>
      <th rowspan="2">項目名</th>
      <th rowspan="2">ID</th>
      <th rowspan="2">型定義</th>
      <th rowspan="2">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2">初期値</th>
      <th rowspan="2">clearボタン</th>
      <th rowspan="2">deleteボタン</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>生殖補助医療の有無</strong></td>
      <td>case_presence_of_assisted_reproductive_technology</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>unknown</li>
          <li>absent</li>
          <li>present</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>なし</li>
          <li>あり</li>
        </ul>
      </td>
      <td>"不明"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>生殖補助医療の種類</strong></td>
      <td>case_type_of_assisted_reproductive_technology</td>
      <td>Array&lt;string|null&gt;</td>
      <td>チェックボックス</td>
      <td>
        <ul>
          <li>ivf_et</li>
          <li>icsi</li>
          <li>frozen_embryo</li>
          <li>other</li>
          <li>unknown</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>体外受精・胚移植（IVF-ET）</li>
          <li>顕微授精（卵細胞質内精子注入法、ICSI）</li>
          <li>凍結胚・融解移植</li>
          <li>その他</li>
          <li>不明</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 入力者情報 {: #inputter-info}

<table>
  <thead>
    <tr>
      <th rowspan="2">項目名</th>
      <th rowspan="2">ID</th>
      <th rowspan="2">型定義</th>
      <th rowspan="2">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2">初期値</th>
      <th rowspan="2">clearボタン</th>
      <th rowspan="2">deleteボタン</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>調査実施日 (yyyy/mm/dd)</strong></td>
      <td>case_date_of_survey</td>
      <td>string</td>
      <td>カレンダー選択</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>診察日 (yyyy/mm/dd)</strong></td>
      <td>case_examination_day</td>
      <td>string</td>
      <td>カレンダー選択</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>施設名</strong></td>
      <td>case_name_of_facility</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>施設コード</strong></td>
      <td>case_code_of_facility</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>担当医師名（姓）</strong></td>
      <td>case_family_name_of_doctor_in_charge</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>担当医師名（名）</strong></td>
      <td>case_first_name_of_doctor_in_charge</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>入力者名（姓）</strong></td>
      <td>case_family_name_of_inputter</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.metadata.createdBy</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>入力者名（名）</strong></td>
      <td>case_first_name_of_inputter</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.metadata.createdBy</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>備考</strong></td>
      <td>case_note</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>作成日時</strong></td>
      <td>case_created_at</td>
      <td>string</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>{yyyy}/{M}/{d} {HH}:{mm}:{ss}</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.metadata.created / metadata.created</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>更新日時</strong></td>
      <td>case_updated_at</td>
      <td>string</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>{yyyy}/{M}/{d} {HH}:{mm}:{ss}</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>