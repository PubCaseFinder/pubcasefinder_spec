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
## 民族・出生地（EN: `Etnicity`, KO: `민족・출신지`） {: #etnicity}
## 出生時（EN: `Birth Info`, KO: `출생 정보`） {: #birth-info}
## 生殖補助（EN: `Assisted Reproduction`, KO: `보조 생식`） {: #assisted-reproduction}
## 入力者情報（EN: `Inputter Info`, KO: `입력자 정보`） {: #inputter-info}
