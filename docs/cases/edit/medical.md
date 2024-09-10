# 診療 {: #medical-examination}

このセクションでは、患者の医療情報を体系的に管理します。<br />
体系的に管理された情報は、長期的な治療計画の立案や、疾患の傾向分析にも役立ちます。<br />
また、医療従事者間での情報共有が容易になり、効率的な診療支援と包括的な患者ケアが可能となります。<br />

## 大項目

| 項目名                                                                       | 説明                                                                                                                                               |
| ---------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **[病歴・生活歴](#medical-and-life-history)**                                | 患者の病歴・生活歴を編集することができます。<br />既往歴疾患名、合併症疾患名は入力内容をもとにサジェストを表示します。                             |
| **[身体情報・所見](#physical-information-and-findings)**                     | 患者の身体情報・所見を編集することができます。                                                                                                     |
| **[常用薬・アレルギー・嗜好品](#regular-medications-allergies-preferences)** | 患者が服用している常用薬、アレルギー情報、飲酒・喫煙など嗜好品に関する情報を編集することができます。                                               |
| **[疑い病名](#suspected-case)**                                              | 患者の疑い病名を編集することができます。<br />疑い病名は入力内容をもとにサジェストを表示します。                                                   |
| **[遺伝性疾患と考える根拠](#genetic-disease-rationale)**                     | 患者に遺伝性疾患の可能性がある場合、その根拠を編集することができます。                                                                             |
| **[診断](#diagnosis)**                                                       | 患者の診断状況を編集することができます。<br />臨床診断、確定診断は入力内容をもとにサジェストを表示します。                                         |
| **[指定難病](#designated-intractable-disease)**                              | 患者の指定難病に関する認定状況や申請情報を編集することができます。<br />申請した指定難病は入力内容をもとにサジェストを表示します。                 |
| **[小児慢性特定疾病](#chronic-pediatric-disease)**                           | 患者の小児慢性特定疾病に関する認定状況や申請情報を編集することができます。<br />申請した小児慢性特定疾病は入力内容をもとにサジェストを表示します。 |

---

## 病歴・生活歴 {: #medical-and-life-history}

<table>
  <thead>
    <tr>
      <th rowspan="2" class="text-vertical-align-middle">大項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">中項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">小項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">clearボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">deleteボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">Phenopackets</th>
      <th rowspan="2" class="text-vertical-align-middle">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="6"><strong>現病歴</strong></td>
      <td rowspan="3"><strong>発症年齢 (YMD)</strong></td>
      <td rowspan="3"><strong>-</strong></td>
      <td rowspan="3">medical_age_onset</td>
      <td rowspan="3">string | null</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td rowspan="3">null</td>
      <td rowspan="3"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="3"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="3"></td>
      <td rowspan="3">
        「{{yyyy}} + Y + {{mm}} + M + {{dd}} + D」の形式でjsonに保存される
      </td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>-</td>
      <td>-</td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>-</td>
      <td>-</td>
    </tr>
    <tr>
      <td><strong>主訴</strong></td>
      <td><strong>-</strong></td>
      <td>medical_chief_complaint</td>
      <td>string | null</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>経過</strong></td>
      <td><strong>-</strong></td>
      <td>medical_process</td>
      <td>string | null</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>現病歴</strong></td>
      <td><strong>-</strong></td>
      <td>medical_current_history</td>
      <td>string | null</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="5"><strong>既往歴</strong></td>
      <td><strong>既往歴の有無</strong></td>
      <td><strong>-</strong></td>
      <td>medical_presence_of_previous_history</td>
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
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>既往歴疾患名</strong></td>
      <td><strong>疾患名</strong></td>
      <td>medical_disease_of_previous_history_name</td>
      <td>Array&lt;string | null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[null]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td>
        <ul>
          <li>テキストボックスに入力した値を「/static/data/icd10_utf8.tsv」から該当する疾患を検索し、サジェストとして表示する</li>
          <li>追加ボタンから複数登録が可能</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>既往歴疾患名_備考</strong></td>
      <td><strong>-</strong></td>
      <td>medical_note_of_previous_history</td>
      <td>string | null</td>
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
      <td><strong>既往歴</strong></td>
      <td><strong>-</strong></td>
      <td>medical_previous_history</td>
      <td>string | null</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>出生前および周産期の病歴</strong></td>
      <td><strong>-</strong></td>
      <td>medical_prenatal_perinatal_history</td>
      <td>string | null</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="4"><strong>合併病歴</strong></td>
      <td><strong>合併症の有無</strong></td>
      <td><strong>-</strong></td>
      <td>medical_presence_of_complications</td>
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
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>合併症疾患名</strong></td>
      <td><strong>疾患名</strong></td>
      <td>medical_complication_history_name</td>
      <td>Array&lt;string | null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[null]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td>
        <ul>
          <li>テキストボックスに入力した値を「/static/data/icd10_utf8.tsv」から該当する疾患を検索し、サジェストとして表示する</li>
          <li>追加ボタンから複数登録が可能</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>合併症疾患名_備考</strong></td>
      <td><strong>-</strong></td>
      <td>medical_note_of_complications</td>
      <td>string | null</td>
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
      <td><strong>合併症歴</strong></td>
      <td><strong>-</strong></td>
      <td>medical_complication_history</td>
      <td>string | null</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="13"><strong>妊娠・出産情報</strong></td>
      <td><strong>妊娠の有無</strong></td>
      <td><strong>-</strong></td>
      <td>medical_presence_of_pregnancy</td>
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
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>妊娠回数（回）</strong></td>
      <td rowspan="2"><strong>-</strong></td>
      <td rowspan="2">medical_number_of_pregnancy</td>
      <td rowspan="2">string | null</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"></td>
      <td rowspan="2">
        <ul>
          <li>「妊娠の有無」で「あり」を選択している時のみ入力可（それ以外の場合は非活性）</li>
          <li>「不明」にチェックすると、「妊娠回数（回）」の入力欄が非活性になり、入力した値をクリア</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>チェックボックス</td>
      <td>-</td>
      <td>-</td>
      <td>false</td>
    </tr>
    <tr>
      <td><strong>出産の有無</strong></td>
      <td><strong>-</strong></td>
      <td>medical_presence_of_childbirth</td>
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
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>出産回数 (回)</strong></td>
      <td rowspan="2"><strong>-</strong></td>
      <td rowspan="2">medical_number_of_childbirth</td>
      <td rowspan="2">string | null</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"></td>
      <td rowspan="2">
        <ul>
          <li>「出産の有無」で「あり」を選択している時のみ入力可（それ以外の場合は非活性）</li>
          <li>「不明」にチェックすると、「出産回数 (回)」の入力欄が非活性になり、入力した値をクリア</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>チェックボックス</td>
      <td>-</td>
      <td>-</td>
      <td>false</td>
    </tr>
    <tr>
      <td><strong>死産・流産の有無</strong></td>
      <td><strong>-</strong></td>
      <td>medical_presence_of_stillbirth_miscarriage</td>
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
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>死産の回数 (回)</strong></td>
      <td rowspan="2"><strong>-</strong></td>
      <td rowspan="2">medical_number_of_stillbirth</td>
      <td rowspan="2">string | null</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"></td>
      <td rowspan="6">
        <ul>
          <li>「死産・流産の有無」で「あり」を選択している時のみ入力可（それ以外の場合は非活性）</li>
          <li>「不明」にチェックすると、各項目の入力欄が非活性になり、入力した値をクリア</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>チェックボックス</td>
      <td>-</td>
      <td>-</td>
      <td>false</td>
    </tr>
    <tr>
      <td rowspan="2"><strong>流産 (自然)の回数 (回)</strong></td>
      <td rowspan="2"><strong>-</strong></td>
      <td rowspan="2">medical_number_of_miscarriage</td>
      <td rowspan="2">string | null</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"></td>
    </tr>
    <tr>
      <td>チェックボックス</td>
      <td>-</td>
      <td>-</td>
      <td>false</td>
    </tr>
    <tr>
      <td rowspan="2"><strong>流産 (人工)の回数 (回)</strong></td>
      <td rowspan="2"><strong>-</strong></td>
      <td rowspan="2">medical_number_of_artificial_abortion</td>
      <td rowspan="2">string | null</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"></td>
    </tr>
    <tr>
      <td>チェックボックス</td>
      <td>-</td>
      <td>-</td>
      <td>false</td>
    </tr>
    <tr>
      <td rowspan="5"><strong>教育歴・社会歴</strong></td>
      <td><strong>生育歴および教育歴</strong></td>
      <td><strong>-</strong></td>
      <td>medical_early_developmental_and_schooling_history</td>
      <td>string | null</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>就労の有無</strong></td>
      <td><strong>-</strong></td>
      <td>medical_presence_of_employment</td>
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
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>職業分類</strong></td>
      <td><strong>-</strong></td>
      <td>medical_occupational_classification</td>
      <td>Array&lt;string | null&gt;</td>
      <td>チェックボックス</td>
      <td>
        <ul>
          <li>managerial_occupation</li>
          <li>professional_technical_occupation</li>
          <li>clerical_occupation</li>
          <li>sales_occupation</li>
          <li>service_occupation</li>
          <li>security_occupation</li>
          <li>agriculture_forestry_fishing_occupation</li>
          <li>production_process_occupation</li>
          <li>transportation_machine_operation_occupation</li>
          <li>construction_mining_occupation</li>
          <li>transportation_cleaning_packaging_occupation</li>
          <li>others</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>管理的職業</li>
          <li>専門的・技術的職業</li>
          <li>事務的職業</li>
          <li>販売の職業</li>
          <li>サービスの職業</li>
          <li>保安の職業</li>
          <li>農林漁業の職業</li>
          <li>生産工程の職業</li>
          <li>輸送・機械運転の職業</li>
          <li>建設・採掘の職業</li>
          <li>運輸・清掃・包装の職業</li>
          <li>その他</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>その他詳細</strong></td>
      <td><strong>-</strong></td>
      <td>medical_occupational_classification_other_details</td>
      <td>string | null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>「職業分類」で「その他」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>社会歴</strong></td>
      <td><strong>-</strong></td>
      <td>medical_social_history</td>
      <td>string | null</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>渡航歴・予防接種歴</strong></td>
      <td><strong>渡航歴</strong></td>
      <td><strong>-</strong></td>
      <td>medical_travel_history</td>
      <td>string | null</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>予防接種歴</strong></td>
      <td><strong>-</strong></td>
      <td>medical_vaccination_history</td>
      <td>string | null</td>
      <td>テキストエリア</td>
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

## 身体情報・所見 {: #physical-information-and-findings}

<table>
  <thead>
    <tr>
      <th rowspan="2" class="text-vertical-align-middle">中項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">小項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">clearボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">deleteボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">Phenopackets</th>
      <th rowspan="2" class="text-vertical-align-middle">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3"><strong>出生時身体情報</strong></td>
      <td><strong>身長 (cm)</strong></td>
      <td>medical_body_height_at_birth</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>体重 (g)</strong></td>
      <td>medical_body_weight_at_birth</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>頭囲 (cm)</strong></td>
      <td>medical_head_circumference_at_birth</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="5"><strong>登録時身体情報</strong></td>
      <td><strong>身長 (cm)</strong></td>
      <td>medical_body_height_at_registration</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>体重 (kg)</strong></td>
      <td>medical_body_height_at_registration</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>頭囲 (cm)</strong></td>
      <td>medical_head_circumference_at_registration</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>測定時年齢 (YM)</strong></td>
      <td rowspan="2">medical_age_at_measurement</td>
      <td rowspan="2">string</td>
      <td>テキストボックス (数字)</td>
      <td>-</td>
      <td>-</td>
      <td rowspan="2">""</td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"></td>
      <td rowspan="2">
        「{{yyyy}} + Y + {{mm}} + M」の形式でjsonに保存される
      </td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>0~11</td>
      <td>0~11</td>
    </tr>
    <tr>
      <td rowspan="4"><strong>診察時身体情報</strong></td>
      <td><strong>日付(yyyy/mm/dd)</strong></td>
      <td>medical_body_info_date_at_examination</td>
      <td>Array&lt;string | null&gt;</td>
      <td>カレンダー選択</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td rowspan="4">追加ボタンから複数登録が可能</td>
    </tr>
    <tr>
      <td><strong>身長 (cm)</strong></td>
      <td>medical_body_height_at_examination</td>
      <td>Array&lt;string&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>体重 (kg)</strong></td>
      <td>medical_body_weight_at_examination</td>
      <td>Array&lt;string&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>頭囲 (cm)</strong></td>
      <td>medical_head_circumference_at_examination</td>
      <td>Array&lt;string&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>身体所見</strong></td>
      <td>-</td>
      <td>medical_physical_findings</td>
      <td>string</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>検査初見</strong></td>
      <td>-</td>
      <td>medical_examination_findings</td>
      <td>string</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 常用薬・アレルギー・嗜好品 {: #regular-medications-allergies-preferences}

<table>
  <thead>
    <tr>
      <th rowspan="2" class="text-vertical-align-middle">項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">clearボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">deleteボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">Phenopackets</th>
      <th rowspan="2" class="text-vertical-align-middle">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>常用薬</strong></td>
      <td>medical_medications</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>アレルギー</strong></td>
      <td>medical_allergies</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>飲酒習慣の有無</strong></td>
      <td>medical_presence_of_drinking_habits</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>Unknown</li>
          <li>Absent</li>
          <li>Present</li>
          <li>Present before, but currently absent</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>なし</li>
          <li>あり</li>
          <li>過去はあり、現在はなし</li>
        </ul>
      </td>
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>飲酒量</strong></td>
      <td>medical_drinking</td>
      <td>number | null</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>「飲酒習慣の有無」で「あり」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>喫煙習慣の有無</strong></td>
      <td>medical_presence_of_smoking_habits</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>Unknown</li>
          <li>Absent</li>
          <li>Present</li>
          <li>Present before, but currently absent</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>なし</li>
          <li>あり</li>
          <li>過去はあり、現在はなし</li>
        </ul>
      </td>
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>本数 (本/日)</strong></td>
      <td>medical_number_of_smoking</td>
      <td>number | null</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>「喫煙習慣の有無」で「あり」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>喫煙年数（年）</strong></td>
      <td>medical_years_of_smoking</td>
      <td>number | null</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>「喫煙習慣の有無」で「あり」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
  </tbody>
</table>

## 疑い病名 {: #suspected-case}

<table>
  <thead>
    <tr>
      <th rowspan="2" class="text-vertical-align-middle">中項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">小項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">clearボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">deleteボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">Phenopackets</th>
      <th rowspan="2" class="text-vertical-align-middle">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3"><strong>疑い病名</strong></td>
      <td><strong>疾患名</strong></td>
      <td>medical_suspected_disease_name</td>
      <td>Array&lt;string&gt;</td>
      <td>テキストボックス（サジェスト機能付き）</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td>
        <ul>
          <li>テキストボックスに入力した値を「/static/data/mondo_utf8.tsv」から該当する疾患を検索し、サジェストとして表示する</li>
          <li>追加ボタンから複数登録が可能</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## 遺伝性疾患と考える根拠 {: #rationale-for-considering-it-a-genetic-disease}

<table>
  <thead>
    <tr>
      <th rowspan="2" class="text-vertical-align-middle">項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">clearボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">deleteボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">Phenopackets</th>
      <th rowspan="2" class="text-vertical-align-middle">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>遺伝性疾患の疑い</strong></td>
      <td>medical_suspection_of_genetic_disease</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>Unknown</li>
          <li>Absent</li>
          <li>Present</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>なし</li>
          <li>あり</li>
        </ul>
      </td>
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>家族性への該当の有無</strong></td>
      <td>medical_presence_of_familiality</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>Unknown</li>
          <li>Absent</li>
          <li>Present</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>なし</li>
          <li>あり</li>
        </ul>
      </td>
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>家系内に関連する症状等</strong></td>
      <td>medical_symptoms_related_within_family_lineage</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>「家族性への該当の有無」で「あり」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>多系統疾患への該当の有無</strong></td>
      <td>presence_of_multisystem_disorder</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>Unknown</li>
          <li>Absent</li>
          <li>Present</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>なし</li>
          <li>あり</li>
        </ul>
      </td>
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>疾患領域</strong></td>
      <td>medical_disease_area</td>
      <td>Array&lt;string&gt;</td>
      <td>チェックボックス</td>
      <td>
        <ul>
          <li>Congenital abnormality</li>
          <li>Facial abnormality</li>
          <li>Nerve and muscle</li>
          <li>Kidney and urinary tract</li>
          <li>Respiratory system</li>
          <li>Circulatory system</li>
          <li>Bone and cartilage</li>
          <li>Blood</li>
          <li>Endocrine and metabolism</li>
          <li>Liver biliary spleen</li>
          <li>Digestive system</li>
          <li>Skin</li>
          <li>Ear nose throat</li>
          <li>Eye</li>
          <li>Limbs</li>
          <li>Mental</li>
          <li>Other</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>先天異常</li>
          <li>顔貌異常</li>
          <li>神経・筋</li>
          <li>腎・泌尿器</li>
          <li>呼吸器</li>
          <li>循環器</li>
          <li>骨・軟骨</li>
          <li>血液</li>
          <li>内分泌・代謝</li>
          <li>肝胆脾</li>
          <li>消化器</li>
          <li>皮膚</li>
          <li>耳鼻咽喉</li>
          <li>眼</li>
          <li>四肢</li>
          <li>精神</li>
          <li>その他</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>「多系統疾患への該当の有無」で「あり」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>その他詳細</strong></td>
      <td>medical_disease_area_details</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>「疾患領域」で「その他」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
  </tbody>
</table>

## 診断 {: #diagnosis}

<table>
  <thead>
    <tr>
      <th rowspan="2" class="text-vertical-align-middle">中項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">小項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">clearボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">deleteボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">Phenopackets</th>
      <th rowspan="2" class="text-vertical-align-middle">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>-</strong></td>
      <td><strong>診断状況</strong></td>
      <td>medical_case_solved</td>
      <td>string | null</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>UNKNOWN_PROGRESS</li>
          <li>IN_PROGRESS</li>
          <li>COMPLETED</li>
          <li>SOLVED</li>
          <li>UNSOLVED</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>進行状況不明</li>
          <li>進行中</li>
          <li>完了</li>
          <li>解決済み</li>
          <li>未解決</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>-</strong></td>
      <td><strong>臨床診断名確定の有無</strong></td>
      <td>medical_confirmation_of_clinical_diagnosis</td>
      <td>string | null</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>Unknown</li>
          <li>Absent</li>
          <li>Present</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>なし</li>
          <li>あり</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>臨床診断</strong></td>
      <td><strong>疾患名</strong></td>
      <td>medical_clinical_diagnosis_name</td>
      <td>Array&lt;string&gt;</td>
      <td>テキストボックス（サジェスト機能付き）</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td>
        <ul>
          <li>テキストボックスに入力した値を「/static/data/mondo_icd10_utf8.tsv」から該当する疾患を検索し、サジェストとして表示する</li>
          <li>追加ボタンから複数登録が可能</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>診断年月（yyyy/mm/dd）</strong></td>
      <td>medical_clinical_diagnosis_date</td>
      <td>Array&lt;string&gt;</td>
      <td>カレンダー選択</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td></td>
      <td>追加ボタンから複数登録が可能</td>
    </tr>
    <tr>
      <td rowspan="2"><strong>確定診断</strong></td>
      <td><strong>疾患名</strong></td>
      <td>medical_final_diagnosis_name</td>
      <td>Array&lt;string&gt;</td>
      <td>テキストボックス（サジェスト機能付き）</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td>
        <ul>
          <li>テキストボックスに入力した値を「/static/data/mondo_icd10_utf8.tsv」から該当する疾患を検索し、サジェストとして表示する</li>
          <li>追加ボタンから複数登録が可能</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>診断年月（yyyy/mm/dd）</strong></td>
      <td>medical_final_diagnosis_date</td>
      <td>Array&lt;string&gt;</td>
      <td>カレンダー選択</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td></td>
      <td>追加ボタンから複数登録が可能</td>
    </tr>
  </tbody>
</table>

## 指定難病 {: #designated-incurable-disease}

<table>
  <thead>
    <tr>
      <th rowspan="2" class="text-vertical-align-middle">中項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">小項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">clearボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">deleteボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">Phenopackets</th>
      <th rowspan="2" class="text-vertical-align-middle">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>-</strong></td>
      <td><strong>指定難病認定の有無</strong></td>
      <td>medical_presence_of_designated_intractable_disease_certification</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>not_applied</li>
          <li>in_progress</li>
          <li>approved</li>
          <li>not_approved</li>
          <li>other</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>未申請</li>
          <li>申請中</li>
          <li>認定</li>
          <li>非認定</li>
        </ul>
      </td>
      <td>"not_applied"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>申請した指定難病</strong></td>
      <td><strong>疾患名</strong></td>
      <td>medical_applied_intractable_disease_name</td>
      <td>Array&lt;string&gt;</td>
      <td>テキストボックス（サジェスト機能付き）</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td>
        <ul>
          <li>テキストボックスに入力した値を元に「/static/data/nando_utf8.tsv」から該当する疾患を検索し、サジェストとして表示する</li>
          <li>追加ボタンから複数登録が可能</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## 小児慢性特定疾病 {: #chronic-childhood-diseases}

<table>
  <thead>
    <tr>
      <th rowspan="2" class="text-vertical-align-middle">中項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">小項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">clearボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">deleteボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">Phenopackets</th>
      <th rowspan="2" class="text-vertical-align-middle">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>-</strong></td>
      <td><strong>小児慢性特定疾病認定の有無</strong></td>
      <td>medical_presence_of_pediatric_chronic_specific_disease_certification</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>not_applied</li>
          <li>in_progress</li>
          <li>approved</li>
          <li>not_approved</li>
          <li>other</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>未申請</li>
          <li>申請中</li>
          <li>認定</li>
          <li>非認定</li>
        </ul>
      </td>
      <td>"not_applied"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>申請した小児慢性特定疾病</strong></td>
      <td><strong>疾患名</strong></td>
      <td>medical_applied_pediatric_disease_name</td>
      <td>Array&lt;string&gt;</td>
      <td>テキストボックス（サジェスト機能付き）</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td>
        <ul>
          <li>テキストボックスに入力した値を元に「/static/data/nando_utf8.tsv」から該当する疾患を検索し、サジェストとして表示する</li>
          <li>追加ボタンから複数登録が可能</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
