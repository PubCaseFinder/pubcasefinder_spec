# 項目

Casesでは下記の項目を扱うことができます。

## 大項目

- **[症例基本情報](#case-info)**
- **[診療](#medical)**
- **[表現型](#phenotype)**
- **[遺伝型](#genotype)**
- **[家系](#family)**
- **[検体・検査](#sample)**
- **[登録](#registration)**

---

### 症例基本情報 {: #case-info}
各項目の編集については[こちら](/cases/edit/case-basic-information)

<!-- TODO: 編集モーダルとの違いを列追加 -->

<table>
  <thead>
    <tr>
      <th rowspan="2" class="text-vertical-align-middle">項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th colspan="3">一覧表</th>
      <th rowspan="2" class="text-vertical-align-middle">編集モーダル表示</th>
      <th rowspan="2" class="text-vertical-align-middle">備考</th>
    </tr>
    <tr>
      <th>表示可能</th>
      <th>デフォルト表示</th>
      <th>編集可能</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>PCF No.</strong></td>
      <td>PCFNo</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>症例ID</strong></td>
      <td>case_id</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>家族ID</strong></td>
      <td>case_family_id</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>グループ名</strong></td>
      <td>case_group</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>続柄</strong></td>
      <td>case_relationship</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>血縁者の本研究参加の有無</strong></td>
      <td>case_participation_of_relatives_in_this_study</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>性別</strong></td>
      <td>case_sex</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>性別 その他詳細</strong></td>
      <td>case_sex_details</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>発症の有無</strong></td>
      <td>case_presence_or_absence_of_onset</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>状態</strong></td>
      <td>case_life_status</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>生年月 (yyyy/mm)</strong></td>
      <td>case_birth</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>登録時年齢 (YMD)</strong></td>
      <td>case_age</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>診察時年齢 (YMD)</strong></td>
      <td>case_age_on_examination</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>没年月 (yyyy/mm)</strong></td>
      <td>case_death</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>死因</strong></td>
      <td>case_cause_of_death</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>当該疾患以外のときの死因詳細</strong></td>
      <td>case_cause_of_death_details</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>死因ICD-11コード</strong></td>
      <td>case_icd_11_code_of_cause_of_death</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>最終生存確認日 (yyyy/mm/dd)</strong></td>
      <td>case_last_date_of_confirmation_of_survival</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>民族 / 集団</strong></td>
      <td>case_ethnicity_group</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>自由記載</strong></td>
      <td>case_free_comment_about_ethnicity_group</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>国</strong></td>
      <td>case_country_of_birth</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>都道府県</strong></td>
      <td>case_state_of_birth</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>市区町村</strong></td>
      <td>case_city_of_birth</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>自由記載</strong></td>
      <td>case_free_comment_about_birth</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>出生前（胎児）の異常の有無</strong></td>
      <td>case_presence_of_prenatal_abnormalities</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>異常（黄疸等）の有無</strong></td>
      <td>case_presence_of_abnormalities_at_birth</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>医療介助の有無（出産時）</strong></td>
      <td>case_presence_of_medical_assistance_at_birth</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>在胎週数 (週)</strong></td>
      <td>case_gestational_age_at_birth</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>母親の年齢 (YMD)</strong></td>
      <td>case_age_of_mother_at_birth</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>父親の年齢 (YMD)</strong></td>
      <td>case_age_of_father_at_birth</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>生殖補助医療の有無</strong></td>
      <td>case_presence_of_assisted_reproductive_technology</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>生殖補助医療の種類</strong></td>
      <td>case_type_of_assisted_reproductive_technology</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>調査実施日 (yyyy/mm/dd)</strong></td>
      <td>case_date_of_survey</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>診察日 (yyyy/mm/dd)</strong></td>
      <td>case_examination_day</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>施設名</strong></td>
      <td>case_name_of_facility</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>施設コード</strong></td>
      <td>case_code_of_facility</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>担当医師名（姓）</strong></td>
      <td>case_family_name_of_doctor_in_charge</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>担当医師名（名）</strong></td>
      <td>case_first_name_of_doctor_in_charge</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>入力者名（姓）</strong></td>
      <td>case_family_name_of_inputter</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>入力者名（名）</strong></td>
      <td>case_first_name_of_inputter</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>備考</strong></td>
      <td>case_note</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>作成日時</strong></td>
      <td>case_created_at</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>更新日時</strong></td>
      <td>case_updated_at</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
  </tbody>
</table>

### 診療 {: #medical}

### 表現型 {: #phenotype}

### 遺伝型 {: #genotype}

### 家系 {: #family}

### 検体・検査 {: #sample}

### 登録 {: #registration}
