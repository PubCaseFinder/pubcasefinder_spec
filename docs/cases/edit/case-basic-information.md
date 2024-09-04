# 症例基本情報

症例基本情報では、症例者の性別・年齢・出生地などの一般的な情報及び症例の基本情報を包括的に管理します。<br />
また、症例基本情報のデータ入力者自身の情報も記録することができます。

## 大項目

| 項目名                                 | 説明                                                         |
| -------------------------------------- | ------------------------------------------------------------ |
| **[ID](#id)**                          | 症例に関連する各種識別情報を確認/編集することができます。    |
| **[基本情報](#basic-info)**            | 症例者についての基本情報を編集することができます。           |
| **[民族・出生地](#etnicity)**          | 症例者のルーツについての情報を編集することができます。       |
| **[出生時](#birth-info)**              | 症例者の出生時についての情報を編集することができます。       |
| **[生殖補助](#assisted-reproduction)** | 症例者の生殖補助についての情報を編集することができます。     |
| **[入力者情報](#inputter-info)**       | 症例基本情報の入力者についての情報を編集することができます。 |

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
      <td>P + {{作成年}} + {{月}} + {{日}} + {{時間}} + {{秒}} + {{ミリ秒}}</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>症例ID</strong></td>
      <td>case_id</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>C + {{表示中の症例の連番7桁}}</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.id. / subject.id / pedigree.persons.individual_id</td>
      <td></td>
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
          <li>not_applicable</li>
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
      <td>not_applicable</td>
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
        <a href="#country-master">国マスタ</a>
      </td>
      <td>
        <a href="#country-master">国マスタ</a>
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
        <a href="#country-master">国マスタ</a>
      </td>
      <td>
        <a href="#country-master">国マスタ</a>
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
      <td>不明</td>
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
      <td>不明</td>
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
      <td>不明</td>
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
      <td><strong>母親の年齢 (YMD)</strong></td>
      <td>case_age_of_mother_at_birth</td>
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
      <td><strong>父親の年齢 (YMD)</strong></td>
      <td>case_age_of_father_at_birth</td>
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
      <td>不明</td>
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
      <td>-</td>
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
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 国マスタ {: #country-master}

<table>
  <thead>
    <tr>
      <th>コード</th>
      <th>国名</th>
      <th>国名（英）</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>AFG</td>
      <td>アフガニスタン</td>
      <td>Afghanistan</td>
    </tr>
    <tr>
      <td>ALB</td>
      <td>アルバニア</td>
      <td>Albania</td>
    </tr>
    <tr>
      <td>DZA</td>
      <td>アルジェリア</td>
      <td>Algeria</td>
    </tr>
    <tr>
      <td>ASM</td>
      <td>アメリカ領サモア</td>
      <td>American territory Samoa</td>
    </tr>
    <tr>
      <td>AND</td>
      <td>アンドラ</td>
      <td>Andra</td>
    </tr>
    <tr>
      <td>AGO</td>
      <td>アンゴラ</td>
      <td>Angola</td>
    </tr>
    <tr>
      <td>AIA</td>
      <td>アンギラ</td>
      <td>Angilla</td>
    </tr>
    <tr>
      <td>ATA</td>
      <td>南極</td>
      <td>Antarctic</td>
    </tr>
    <tr>
      <td>ATG</td>
      <td>アンティグア・バーブーダ</td>
      <td>Antigua Berbuda</td>
    </tr>
    <tr>
      <td>ARG</td>
      <td>アルゼンチン</td>
      <td>Argentina</td>
    </tr>
    <tr>
      <td>ARM</td>
      <td>アルメニア</td>
      <td>Armenia</td>
    </tr>
    <tr>
      <td>ABW</td>
      <td>アルバ</td>
      <td>Alba</td>
    </tr>
    <tr>
      <td>AUS</td>
      <td>オーストラリア</td>
      <td>Australia</td>
    </tr>
    <tr>
      <td>AUT</td>
      <td>オーストリア</td>
      <td>Austria</td>
    </tr>
    <tr>
      <td>AZE</td>
      <td>アゼルバイジャン</td>
      <td>Azerbaijan</td>
    </tr>
    <tr>
      <td>BHS</td>
      <td>バハマ</td>
      <td>Bahamas</td>
    </tr>
    <tr>
      <td>BHR</td>
      <td>バーレーン</td>
      <td>Barrane</td>
    </tr>
    <tr>
      <td>BGD</td>
      <td>バングラデシュ</td>
      <td>Bangladesh</td>
    </tr>
    <tr>
      <td>BRB</td>
      <td>バルバドス</td>
      <td>Barbados</td>
    </tr>
    <tr>
      <td>BLR</td>
      <td>ベラルーシ</td>
      <td>Belarus</td>
    </tr>
    <tr>
      <td>BEL</td>
      <td>ベルギー</td>
      <td>Belgium</td>
    </tr>
    <tr>
      <td>BLZ</td>
      <td>ベリーズ</td>
      <td>Belize</td>
    </tr>
    <tr>
      <td>BEN</td>
      <td>ベナン</td>
      <td>Benan</td>
    </tr>
    <tr>
      <td>BMU</td>
      <td>バミューダ</td>
      <td>Bermuda</td>
    </tr>
    <tr>
      <td>BTN</td>
      <td>ブータン</td>
      <td>Bhutan</td>
    </tr>
    <tr>
      <td>BOL</td>
      <td>ボリビア多民族国</td>
      <td>Bolivia multi -ethnic country</td>
    </tr>
    <tr>
      <td>BES</td>
      <td>ボネール、シント・ユースタティウスおよびサバ</td>
      <td>Bonnaire, Sint Estatius and Saba"</td>
    </tr>
    <tr>
      <td>BIH</td>
      <td>ボスニア・ヘルツェゴビナ</td>
      <td>Bosnia-Herzegovina</td>
    </tr>
    <tr>
      <td>BWA</td>
      <td>ボツワナ</td>
      <td>Botwana</td>
    </tr>
    <tr>
      <td>BVT</td>
      <td>ブーベ島</td>
      <td>Bouve Island</td>
    </tr>
    <tr>
      <td>BRA</td>
      <td>ブラジル</td>
      <td>Brazil</td>
    </tr>
    <tr>
      <td>IOT</td>
      <td>イギリス領インド洋地域</td>
      <td>British Indian Ocean region</td>
    </tr>
    <tr>
      <td>BRN</td>
      <td>ブルネイ・ダルサラーム</td>
      <td>Brunei Dal Salam</td>
    </tr>
    <tr>
      <td>BGR</td>
      <td>ブルガリア</td>
      <td>Bulgaria</td>
    </tr>
    <tr>
      <td>BFA</td>
      <td>ブルキナファソ</td>
      <td>Burkina Faso</td>
    </tr>
    <tr>
      <td>BDI</td>
      <td>ブルンジ</td>
      <td>Brush</td>
    </tr>
    <tr>
      <td>KHM</td>
      <td>カンボジア</td>
      <td>Cambodia</td>
    </tr>
    <tr>
      <td>CMR</td>
      <td>カメルーン</td>
      <td>Cameroon</td>
    </tr>
    <tr>
      <td>CAN</td>
      <td>カナダ</td>
      <td>Canada</td>
    </tr>
    <tr>
      <td>CPV</td>
      <td>カーボベルデ</td>
      <td>Carbo Verde</td>
    </tr>
    <tr>
      <td>CYM</td>
      <td>ケイマン諸島</td>
      <td>Cayman Islands</td>
    </tr>
    <tr>
      <td>CAF</td>
      <td>中央アフリカ共和国</td>
      <td>Central Africa</td>
    </tr>
    <tr>
      <td>TCD</td>
      <td>チャド</td>
      <td>Chad</td>
    </tr>
    <tr>
      <td>CHL</td>
      <td>チリ</td>
      <td>Chile</td>
    </tr>
    <tr>
      <td>CHN</td>
      <td>中華人民共和国</td>
      <td>People's Republic of China</td>
    </tr>
    <tr>
      <td>CXR</td>
      <td>クリスマス島</td>
      <td>Christmas Island</td>
    </tr>
    <tr>
      <td>CCK</td>
      <td>ココス(キーリング)諸島</td>
      <td>Cocos (keyling) Islands</td>
    </tr>
    <tr>
      <td>COL</td>
      <td>コロンビア</td>
      <td>Columbia</td>
    </tr>
    <tr>
      <td>COM</td>
      <td>コモロ</td>
      <td>Komoro</td>
    </tr>
    <tr>
      <td>COG</td>
      <td>コンゴ共和国</td>
      <td>Congo Republic</td>
    </tr>
    <tr>
      <td>COD</td>
      <td>コンゴ民主共和国</td>
      <td>Congo Democratic Republic</td>
    </tr>
    <tr>
      <td>COK</td>
      <td>クック諸島</td>
      <td>Cook Islands</td>
    </tr>
    <tr>
      <td>CRI</td>
      <td>コスタリカ</td>
      <td>Costa Rica</td>
    </tr>
    <tr>
      <td>HRV</td>
      <td>クロアチア</td>
      <td>Croatia</td>
    </tr>
    <tr>
      <td>CUB</td>
      <td>キューバ</td>
      <td>Cuba</td>
    </tr>
    <tr>
      <td>CUW</td>
      <td>キュラソー</td>
      <td>Curaseau</td>
    </tr>
    <tr>
      <td>CYP</td>
      <td>キプロス</td>
      <td>Cyprus</td>
    </tr>
    <tr>
      <td>CZE</td>
      <td>チェコ</td>
      <td>Czech Republic</td>
    </tr>
    <tr>
      <td>CIV</td>
      <td>コートジボワール</td>
      <td>Court Jiboire</td>
    </tr>
    <tr>
      <td>DNK</td>
      <td>デンマーク</td>
      <td>Denmark</td>
    </tr>
    <tr>
      <td>DJI</td>
      <td>ジブチ</td>
      <td>Jibuchi</td>
    </tr>
    <tr>
      <td>DMA</td>
      <td>ドミニカ国</td>
      <td>Dominica country</td>
    </tr>
    <tr>
      <td>DOM</td>
      <td>ドミニカ共和国</td>
      <td>dominican republic</td>
    </tr>
    <tr>
      <td>ECU</td>
      <td>エクアドル</td>
      <td>Ecuador</td>
    </tr>
    <tr>
      <td>EGY</td>
      <td>エジプト</td>
      <td>Egypt</td>
    </tr>
    <tr>
      <td>SLV</td>
      <td>エルサルバドル</td>
      <td>El Salvador</td>
    </tr>
    <tr>
      <td>GNQ</td>
      <td>赤道ギニア</td>
      <td>Equatorial guinea</td>
    </tr>
    <tr>
      <td>ERI</td>
      <td>エリトリア</td>
      <td>Eritria</td>
    </tr>
    <tr>
      <td>EST</td>
      <td>エストニア</td>
      <td>Estonia</td>
    </tr>
    <tr>
      <td>ETH</td>
      <td>エチオピア</td>
      <td>Ethiopia</td>
    </tr>
    <tr>
      <td>FLK</td>
      <td>フォークランド(マルビナス)諸島</td>
      <td>Folkland (Marbinas) Islands"</td>
    </tr>
    <tr>
      <td>FRO</td>
      <td>フェロー諸島</td>
      <td>Fellow Islands</td>
    </tr>
    <tr>
      <td>FJI</td>
      <td>フィジー</td>
      <td>Fiji</td>
    </tr>
    <tr>
      <td>FIN</td>
      <td>フィンランド</td>
      <td>Finland</td>
    </tr>
    <tr>
      <td>FRA</td>
      <td>フランス</td>
      <td>France</td>
    </tr>
    <tr>
      <td>GUF</td>
      <td>フランス領ギアナ</td>
      <td>French territory</td>
    </tr>
    <tr>
      <td>PYF</td>
      <td>フランス領ポリネシア</td>
      <td>French Polynesia</td>
    </tr>
    <tr>
      <td>ATF</td>
      <td>フランス領南方・南極地域</td>
      <td>Southern France and Antarctica</td>
    </tr>
    <tr>
      <td>GAB</td>
      <td>ガボン</td>
      <td>Gabon</td>
    </tr>
    <tr>
      <td>GMB</td>
      <td>ガンビア</td>
      <td>Gambia</td>
    </tr>
    <tr>
      <td>GEO</td>
      <td>ジョージア</td>
      <td>Georgia</td>
    </tr>
    <tr>
      <td>DEU</td>
      <td>ドイツ</td>
      <td>Germany</td>
    </tr>
    <tr>
      <td>GHA</td>
      <td>ガーナ</td>
      <td>Ghana</td>
    </tr>
    <tr>
      <td>GIB</td>
      <td>ジブラルタル</td>
      <td>Gibraltar</td>
    </tr>
    <tr>
      <td>GRC</td>
      <td>ギリシャ</td>
      <td>Greece</td>
    </tr>
    <tr>
      <td>GRL</td>
      <td>グリーンランド</td>
      <td>Greenland</td>
    </tr>
    <tr>
      <td>GRD</td>
      <td>グレナダ</td>
      <td>Grenada</td>
    </tr>
    <tr>
      <td>GLP</td>
      <td>グアドループ</td>
      <td>Guadroop</td>
    </tr>
    <tr>
      <td>GUM</td>
      <td>グアム</td>
      <td>Guam</td>
    </tr>
    <tr>
      <td>GTM</td>
      <td>グアテマラ</td>
      <td>Guatemala</td>
    </tr>
    <tr>
      <td>GGY</td>
      <td>ガーンジー</td>
      <td>Gangnzie</td>
    </tr>
    <tr>
      <td>GIN</td>
      <td>ギニア</td>
      <td>Guinea</td>
    </tr>
    <tr>
      <td>GNB</td>
      <td>ギニアビサウ</td>
      <td>Guinea Visau</td>
    </tr>
    <tr>
      <td>GUY</td>
      <td>ガイアナ</td>
      <td>Gaiana</td>
    </tr>
    <tr>
      <td>HTI</td>
      <td>ハイチ</td>
      <td>Haiti</td>
    </tr>
    <tr>
      <td>HMD</td>
      <td>ハード島とマクドナルド諸島</td>
      <td>Hard Island and McDonald's Islands"</td>
    </tr>
    <tr>
      <td>VAT</td>
      <td>バチカン市国</td>
      <td>Vatican City</td>
    </tr>
    <tr>
      <td>HND</td>
      <td>ホンジュラス</td>
      <td>Honduras</td>
    </tr>
    <tr>
      <td>HKG</td>
      <td>香港</td>
      <td>Hong Kong</td>
    </tr>
    <tr>
      <td>HUN</td>
      <td>ハンガリー</td>
      <td>Hungary</td>
    </tr>
    <tr>
      <td>ISL</td>
      <td>アイスランド</td>
      <td>Iceland</td>
    </tr>
    <tr>
      <td>IND</td>
      <td>インド</td>
      <td>India</td>
    </tr>
    <tr>
      <td>IDN</td>
      <td>インドネシア</td>
      <td>Indonesia</td>
    </tr>
    <tr>
      <td>IRN</td>
      <td>イラン・イスラム共和国</td>
      <td>Iran Islamic Republic</td>
    </tr>
    <tr>
      <td>IRQ</td>
      <td>イラク</td>
      <td>Iraq</td>
    </tr>
    <tr>
      <td>IRL</td>
      <td>アイルランド</td>
      <td>Ireland</td>
    </tr>
    <tr>
      <td>IMN</td>
      <td>マン島</td>
      <td>Island</td>
    </tr>
    <tr>
      <td>ISR</td>
      <td>イスラエル</td>
      <td>Israel</td>
    </tr>
    <tr>
      <td>ITA</td>
      <td>イタリア</td>
      <td>Italy</td>
    </tr>
    <tr>
      <td>JAM</td>
      <td>ジャマイカ</td>
      <td>Jamaica</td>
    </tr>
    <tr>
      <td>JPN</td>
      <td>日本</td>
      <td>Japan</td>
    </tr>
    <tr>
      <td>JEY</td>
      <td>ジャージー</td>
      <td>Jersey</td>
    </tr>
    <tr>
      <td>JOR</td>
      <td>ヨルダン</td>
      <td>Jordan</td>
    </tr>
    <tr>
      <td>KAZ</td>
      <td>カザフスタン</td>
      <td>Kazakhstan</td>
    </tr>
    <tr>
      <td>KEN</td>
      <td>ケニア</td>
      <td>Kenya</td>
    </tr>
    <tr>
      <td>KIR</td>
      <td>キリバス</td>
      <td>Kiribass</td>
    </tr>
    <tr>
      <td>PRK</td>
      <td>朝鮮民主主義人民共和国</td>
      <td>Korean Democracy People's Republic"</td>
    </tr>
    <tr>
      <td>KOR</td>
      <td>大韓民国</td>
      <td>South Korea</td>
    </tr>
    <tr>
      <td>KWT</td>
      <td>クウェート</td>
      <td>Kuwait</td>
    </tr>
    <tr>
      <td>KGZ</td>
      <td>キルギス</td>
      <td>Kyrgyzstan</td>
    </tr>
    <tr>
      <td>LAO</td>
      <td>ラオス人民民主共和国</td>
      <td>Laos People's Democratic Republic</td>
    </tr>
    <tr>
      <td>LVA</td>
      <td>ラトビア</td>
      <td>Latvia</td>
    </tr>
    <tr>
      <td>LBN</td>
      <td>レバノン</td>
      <td>Lebanon</td>
    </tr>
    <tr>
      <td>LSO</td>
      <td>レソト</td>
      <td>Lesot</td>
    </tr>
    <tr>
      <td>LBR</td>
      <td>リベリア</td>
      <td>Liberia</td>
    </tr>
    <tr>
      <td>LBY</td>
      <td>リビア</td>
      <td>Libya</td>
    </tr>
    <tr>
      <td>LIE</td>
      <td>リヒテンシュタイン</td>
      <td>Liechtenstein</td>
    </tr>
    <tr>
      <td>LTU</td>
      <td>リトアニア</td>
      <td>Lithuania</td>
    </tr>
    <tr>
      <td>LUX</td>
      <td>ルクセンブルク</td>
      <td>Luxembourg</td>
    </tr>
    <tr>
      <td>MAC</td>
      <td>マカオ</td>
      <td>Macau</td>
    </tr>
    <tr>
      <td>MKD</td>
      <td>マケドニア旧ユーゴスラビア共和国</td>
      <td>Former Macedonia Yugoslavia Republic"</td>
    </tr>
    <tr>
      <td>MDG</td>
      <td>マダガスカル</td>
      <td>Madagascar</td>
    </tr>
    <tr>
      <td>MWI</td>
      <td>マラウイ</td>
      <td>Malawi</td>
    </tr>
    <tr>
      <td>MYS</td>
      <td>マレーシア</td>
      <td>Malaysia</td>
    </tr>
    <tr>
      <td>MDV</td>
      <td>モルディブ</td>
      <td>Maldives</td>
    </tr>
    <tr>
      <td>MLI</td>
      <td>マリ</td>
      <td>Mari</td>
    </tr>
    <tr>
      <td>MLT</td>
      <td>マルタ</td>
      <td>Malta</td>
    </tr>
    <tr>
      <td>MHL</td>
      <td>マーシャル諸島</td>
      <td>Marshall Islands</td>
    </tr>
    <tr>
      <td>MTQ</td>
      <td>マルティニーク</td>
      <td>Maltinique</td>
    </tr>
    <tr>
      <td>MRT</td>
      <td>モーリタニア</td>
      <td>Mauritania</td>
    </tr>
    <tr>
      <td>MUS</td>
      <td>モーリシャス</td>
      <td>Mauritius</td>
    </tr>
    <tr>
      <td>MYT</td>
      <td>マヨット</td>
      <td>Mayte</td>
    </tr>
    <tr>
      <td>MEX</td>
      <td>メキシコ</td>
      <td>Mexico</td>
    </tr>
    <tr>
      <td>FSM</td>
      <td>ミクロネシア連邦</td>
      <td>Micronesia Federation</td>
    </tr>
    <tr>
      <td>MDA</td>
      <td>モルドバ共和国</td>
      <td>Moldova Republic</td>
    </tr>
    <tr>
      <td>MCO</td>
      <td>モナコ</td>
      <td>Monaco</td>
    </tr>
    <tr>
      <td>MNG</td>
      <td>モンゴル</td>
      <td>Mongolia</td>
    </tr>
    <tr>
      <td>MNE</td>
      <td>モンテネグロ</td>
      <td>Montenegro</td>
    </tr>
    <tr>
      <td>MSR</td>
      <td>モントセラト</td>
      <td>Montrat</td>
    </tr>
    <tr>
      <td>MAR</td>
      <td>モロッコ</td>
      <td>Morocco</td>
    </tr>
    <tr>
      <td>MOZ</td>
      <td>モザンビーク</td>
      <td>Mozambique</td>
    </tr>
    <tr>
      <td>MMR</td>
      <td>ミャンマー</td>
      <td>Myanmar</td>
    </tr>
    <tr>
      <td>NAM</td>
      <td>ナミビア</td>
      <td>Namibia</td>
    </tr>
    <tr>
      <td>NRU</td>
      <td>ナウル</td>
      <td>Naure</td>
    </tr>
    <tr>
      <td>NPL</td>
      <td>ネパール</td>
      <td>Nepal</td>
    </tr>
    <tr>
      <td>NLD</td>
      <td>オランダ</td>
      <td>Netherlands</td>
    </tr>
    <tr>
      <td>NCL</td>
      <td>ニューカレドニア</td>
      <td>New Caledonia</td>
    </tr>
    <tr>
      <td>NZL</td>
      <td>ニュージーランド</td>
      <td>new zealand</td>
    </tr>
    <tr>
      <td>NIC</td>
      <td>ニカラグア</td>
      <td>Nicaragua</td>
    </tr>
    <tr>
      <td>NER</td>
      <td>ニジェール</td>
      <td>Nigail</td>
    </tr>
    <tr>
      <td>NGA</td>
      <td>ナイジェリア</td>
      <td>Nigeria</td>
    </tr>
    <tr>
      <td>NIU</td>
      <td>ニウエ</td>
      <td>Niiee</td>
    </tr>
    <tr>
      <td>NFK</td>
      <td>ノーフォーク島</td>
      <td>Norfolk Island</td>
    </tr>
    <tr>
      <td>MNP</td>
      <td>北マリアナ諸島</td>
      <td>North Mariana Islands</td>
    </tr>
    <tr>
      <td>NOR</td>
      <td>ノルウェー</td>
      <td>Norway</td>
    </tr>
    <tr>
      <td>OMN</td>
      <td>オマーン</td>
      <td>Oman</td>
    </tr>
    <tr>
      <td>PAK</td>
      <td>パキスタン</td>
      <td>Pakistan</td>
    </tr>
    <tr>
      <td>PLW</td>
      <td>パラオ</td>
      <td>Palao</td>
    </tr>
    <tr>
      <td>PSE</td>
      <td>パレスチナ</td>
      <td>Palestine</td>
    </tr>
    <tr>
      <td>PAN</td>
      <td>パナマ</td>
      <td>Panama</td>
    </tr>
    <tr>
      <td>PNG</td>
      <td>パプアニューギニア</td>
      <td>Papua New Guinea</td>
    </tr>
    <tr>
      <td>PRY</td>
      <td>パラグアイ</td>
      <td>Paraguay</td>
    </tr>
    <tr>
      <td>PER</td>
      <td>ペルー</td>
      <td>Peru</td>
    </tr>
    <tr>
      <td>PHL</td>
      <td>フィリピン</td>
      <td>Philippines</td>
    </tr>
    <tr>
      <td>PCN</td>
      <td>ピトケアン</td>
      <td>Pitcean</td>
    </tr>
    <tr>
      <td>POL</td>
      <td>ポーランド</td>
      <td>Poland</td>
    </tr>
    <tr>
      <td>PRT</td>
      <td>ポルトガル</td>
      <td>Portugal</td>
    </tr>
    <tr>
      <td>PRI</td>
      <td>プエルトリコ</td>
      <td>Puerto Rico</td>
    </tr>
    <tr>
      <td>QAT</td>
      <td>カタール</td>
      <td>Qatar</td>
    </tr>
    <tr>
      <td>ROU</td>
      <td>ルーマニア</td>
      <td>Romania</td>
    </tr>
    <tr>
      <td>RUS</td>
      <td>ロシア連邦</td>
      <td>Russian Federation</td>
    </tr>
    <tr>
      <td>RWA</td>
      <td>ルワンダ</td>
      <td>Rwanda</td>
    </tr>
    <tr>
      <td>REU</td>
      <td>レユニオン</td>
      <td>Reunion</td>
    </tr>
    <tr>
      <td>BLM</td>
      <td>サン・バルテルミー</td>
      <td>Saint Baltermy</td>
    </tr>
    <tr>
      <td>SHN</td>
      <td>セントヘレナ・アセンションおよびトリスタンダクーニャ</td>
      <td>St. Helena Ascension and Tristanda Cuna"</td>
    </tr>
    <tr>
      <td>KNA</td>
      <td>セントクリストファー・ネイビス</td>
      <td>St. Christopher Navis</td>
    </tr>
    <tr>
      <td>LCA</td>
      <td>セントルシア</td>
      <td>St. Lucia</td>
    </tr>
    <tr>
      <td>MAF</td>
      <td>サン・マルタン(フランス領)</td>
      <td>Saint Martin (French territory)"</td>
    </tr>
    <tr>
      <td>SPM</td>
      <td>サンピエール島・ミクロン島</td>
      <td>Sanpierre Island Micron Island"</td>
    </tr>
    <tr>
      <td>VCT</td>
      <td>セントビンセントおよびグレナディーン諸島</td>
      <td>St. Vincent and the Grenadine Islands"</td>
    </tr>
    <tr>
      <td>WSM</td>
      <td>サモア</td>
      <td>Samoa</td>
    </tr>
    <tr>
      <td>SMR</td>
      <td>サンマリノ</td>
      <td>Sun Marino</td>
    </tr>
    <tr>
      <td>STP</td>
      <td>サントメ・プリンシペ</td>
      <td>Santa Principa</td>
    </tr>
    <tr>
      <td>SAU</td>
      <td>サウジアラビア</td>
      <td>Saudi Arabia</td>
    </tr>
    <tr>
      <td>SEN</td>
      <td>セネガル</td>
      <td>Senegal</td>
    </tr>
    <tr>
      <td>SRB</td>
      <td>セルビア</td>
      <td>Serbia</td>
    </tr>
    <tr>
      <td>SYC</td>
      <td>セーシェル</td>
      <td>Saechel</td>
    </tr>
    <tr>
      <td>SLE</td>
      <td>シエラレオネ</td>
      <td>Sierra Leone</td>
    </tr>
    <tr>
      <td>SGP</td>
      <td>シンガポール</td>
      <td>Singapore</td>
    </tr>
    <tr>
      <td>SXM</td>
      <td>シント・マールテン(オランダ領)</td>
      <td>Sint Maruten (Dutch territory)"</td>
    </tr>
    <tr>
      <td>SVK</td>
      <td>スロバキア</td>
      <td>Slovakia</td>
    </tr>
    <tr>
      <td>SVN</td>
      <td>スロベニア</td>
      <td>Slovenia</td>
    </tr>
    <tr>
      <td>SLB</td>
      <td>ソロモン諸島</td>
      <td>Solomon Islands</td>
    </tr>
    <tr>
      <td>SOM</td>
      <td>ソマリア</td>
      <td>Somalia</td>
    </tr>
    <tr>
      <td>ZAF</td>
      <td>南アフリカ</td>
      <td>South Africa</td>
    </tr>
    <tr>
      <td>SGS</td>
      <td>サウスジョージア・サウスサンドウィッチ諸島</td>
      <td>South Georgia South Sandwich Islands"</td>
    </tr>
    <tr>
      <td>SSD</td>
      <td>南スーダン</td>
      <td>South Sudan</td>
    </tr>
    <tr>
      <td>ESP</td>
      <td>スペイン</td>
      <td>Spain</td>
    </tr>
    <tr>
      <td>LKA</td>
      <td>スリランカ</td>
      <td>Sri Lanka</td>
    </tr>
    <tr>
      <td>SDN</td>
      <td>スーダン</td>
      <td>Sudan</td>
    </tr>
    <tr>
      <td>SUR</td>
      <td>スリナム</td>
      <td>Slinum</td>
    </tr>
    <tr>
      <td>SJM</td>
      <td>スヴァールバル諸島およびヤンマイエン島</td>
      <td>Subarbar Islands and Yang Maien Island"</td>
    </tr>
    <tr>
      <td>SWZ</td>
      <td>スワジランド</td>
      <td>Swaji Land</td>
    </tr>
    <tr>
      <td>SWE</td>
      <td>スウェーデン</td>
      <td>Sweden</td>
    </tr>
    <tr>
      <td>CHE</td>
      <td>スイス</td>
      <td>Switzerland</td>
    </tr>
    <tr>
      <td>SYR</td>
      <td>シリア・アラブ共和国</td>
      <td>Syria Arab Republic</td>
    </tr>
    <tr>
      <td>TWN</td>
      <td>台湾</td>
      <td>Taiwan</td>
    </tr>
    <tr>
      <td>TJK</td>
      <td>タジキスタン</td>
      <td>Tajikistan</td>
    </tr>
    <tr>
      <td>TZA</td>
      <td>タンザニア</td>
      <td>Tanzania</td>
    </tr>
    <tr>
      <td>THA</td>
      <td>タイ</td>
      <td>Thailand</td>
    </tr>
    <tr>
      <td>TLS</td>
      <td>東ティモール</td>
      <td>East Timor</td>
    </tr>
    <tr>
      <td>TGO</td>
      <td>トーゴ</td>
      <td>Togo</td>
    </tr>
    <tr>
      <td>TKL</td>
      <td>トケラウ</td>
      <td>Tokerau</td>
    </tr>
    <tr>
      <td>TON</td>
      <td>トンガ</td>
      <td>Tonga</td>
    </tr>
    <tr>
      <td>TTO</td>
      <td>トリニダード・トバゴ</td>
      <td>Republic of Trinidad and Tobago</td>
    </tr>
    <tr>
      <td>TUN</td>
      <td>チュニジア</td>
      <td>Tunisia</td>
    </tr>
    <tr>
      <td>TUR</td>
      <td>トルコ</td>
      <td>Türkiye</td>
    </tr>
    <tr>
      <td>TKM</td>
      <td>トルクメニスタン</td>
      <td>Torque menistan</td>
    </tr>
    <tr>
      <td>TCA</td>
      <td>タークス・カイコス諸島</td>
      <td>Thakus Kaikos Islands</td>
    </tr>
    <tr>
      <td>TUV</td>
      <td>ツバル</td>
      <td>Tsubaru</td>
    </tr>
    <tr>
      <td>UGA</td>
      <td>ウガンダ</td>
      <td>Uganda</td>
    </tr>
    <tr>
      <td>UKR</td>
      <td>ウクライナ</td>
      <td>Ukraine</td>
    </tr>
    <tr>
      <td>ARE</td>
      <td>アラブ首長国連邦</td>
      <td>United Arab Emirates</td>
    </tr>
    <tr>
      <td>GBR</td>
      <td>イギリス</td>
      <td>England</td>
    </tr>
    <tr>
      <td>USA</td>
      <td>アメリカ合衆国</td>
      <td>united states of america</td>
    </tr>
    <tr>
      <td>UMI</td>
      <td>合衆国領有小離島</td>
      <td>US territory small island</td>
    </tr>
    <tr>
      <td>URY</td>
      <td>ウルグアイ</td>
      <td>Uruguay</td>
    </tr>
    <tr>
      <td>UZB</td>
      <td>ウズベキスタン</td>
      <td>Uzbekistan</td>
    </tr>
    <tr>
      <td>VUT</td>
      <td>バヌアツ</td>
      <td>Vanuatsu</td>
    </tr>
    <tr>
      <td>VEN</td>
      <td>ベネズエラ・ボリバル共和国</td>
      <td>Venezuela Bolivar Republic</td>
    </tr>
    <tr>
      <td>VNM</td>
      <td>ベトナム</td>
      <td>Vietnam</td>
    </tr>
    <tr>
      <td>VGB</td>
      <td>イギリス領ヴァージン諸島</td>
      <td>British Virgin Islands</td>
    </tr>
    <tr>
      <td>VIR</td>
      <td>アメリカ領ヴァージン諸島</td>
      <td>American territory Virgin Islands"</td>
    </tr>
    <tr>
      <td>WLF</td>
      <td>ウォリス・フツナ</td>
      <td>Waris Futna</td>
    </tr>
    <tr>
      <td>ESH</td>
      <td>西サハラ</td>
      <td>West Sahara</td>
    </tr>
    <tr>
      <td>YEM</td>
      <td>イエメン</td>
      <td>Yemen</td>
    </tr>
    <tr>
      <td>ZMB</td>
      <td>ザンビア</td>
      <td>Zambia</td>
    </tr>
    <tr>
      <td>ZWE</td>
      <td>ジンバブエ</td>
      <td>Zimbabwe</td>
    </tr>
    <tr>
      <td>ALA</td>
      <td>オーランド諸島</td>
      <td>Orlando Islands</td>
    </tr>
    <tr>
      <td>ZZZ</td>
      <td>不明</td>
      <td>not clear</td>
    </tr>
  </tbody>
</table>
