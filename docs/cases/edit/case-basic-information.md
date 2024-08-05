# 症例基本情報（EN: `Case Info`, KO: `의료사례 기본 정보`） {: #case-info}

## ID（EN: `ID`, KO: `ID`） {: #id}

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
      <th colspan="3">一覧表示/操作</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
      <th>デフォルト表示</th>
      <th>編集可能</th>
      <th>列追加可能</th>
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
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>P + {{作成年}} + {{月}} + {{日}} + {{時間}} + {{秒}} + {{ミリ秒}}</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
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
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>C + {{表示中の症例の連番7桁}}</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>1</td>
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
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>1</td>
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
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>1</td>
      <td></td>
      <td>一覧に表示中のグループIDをプルダウンから選択可能</td>
    </tr>
  </tbody>
</table>

## 基本情報（EN: `Basic Info`, KO: `기본 정보`） {: #basic-info}

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
      <th colspan="3">一覧表示/操作</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
      <th>デフォルト表示</th>
      <th>編集可能</th>
      <th>列追加可能</th>
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
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
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
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
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
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
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
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
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
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
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
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
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
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
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
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
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
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
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
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
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
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>当該疾患以外のときの死因詳細</strong></td>
      <td>case_cause_of_death_details</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>死因ICD-11コード</strong></td>
      <td>case_icd_11_code_of_cause_of_death</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>最終生存確認日 (yyyy/mm/dd)</strong></td>
      <td>case_last_date_of_confirmation_of_survival</td>
      <td>string</td>
      <td>日付選択インターフェース</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 民族・出生地（EN: `Etnicity`, KO: `민족・출신지`） {: #etnicity}
## 出生時（EN: `Birth Info`, KO: `출생 정보`） {: #birth-info}
## 生殖補助（EN: `Assisted Reproduction`, KO: `보조 생식`） {: #assisted-reproduction}
## 入力者情報（EN: `Inputter Info`, KO: `입력자 정보`） {: #inputter-info}
