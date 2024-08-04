# 症例基本情報（EN: `Case Info`, KO: `의료사례 기본 정보`） {: #case-info}

## ID（EN: `ID`, KO: `ID`） {: #id}

<table>
  <thead>
    <tr>
      <th colspan="3">項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="4">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">clearボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">deleteボタン</th>
      <th colspan="3">一覧表示/操作</th>
      <th rowspan="2" class="text-vertical-align-middle">備考</th>
    </tr>
    <tr>
      <th>EN</th>
      <th>JA</th>
      <th>KO</th>
      <th>値</th>
      <th>EN</th>
      <th>JA</th>
      <th>KO</th>
      <th>デフォルト表示</th>
      <th>編集可能</th>
      <th>列追加可能</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>PCF No.</strong></td>
      <td><strong>PCF No.</strong></td>
      <td><strong>PCF No.</strong></td>
      <td>PCFNo</td>
      <td>string</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>P + {{作成年}} + {{月}} + {{日}} + {{時間}} + {{秒}} + {{ミリ秒}}</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Case ID</strong></td>
      <td><strong>症例ID</strong></td>
      <td><strong>의료사례 ID</strong></td>
      <td>case_id</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>C + {{表示中の症例の連番7桁}}</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Family ID</strong></td>
      <td><strong>家族ID</strong></td>
      <td><strong>가족 ID</strong></td>
      <td>case_family_id</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>一覧に表示中の家族IDをプルダウンから選択可能</td>
    </tr>
    <tr>
      <td><strong>Group</strong></td>
      <td><strong>グループ名</strong></td>
      <td><strong>그룹명</strong></td>
      <td>case_group</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>一覧に表示中のグループIDをプルダウンから選択可能</td>
    </tr>
  </tbody>
</table>

## 基本情報（EN: `Basic Info`, KO: `기본 정보`） {: #basic-info}
## 民族・出生地（EN: `Etnicity`, KO: `민족・출신지`） {: #etnicity}
## 出生時（EN: `Birth Info`, KO: `출생 정보`） {: #birth-info}
## 生殖補助（EN: `Assisted Reproduction`, KO: `보조 생식`） {: #assisted-reproduction}
## 入力者情報（EN: `Inputter Info`, KO: `입력자 정보`） {: #inputter-info}
