# 遺伝型

## 検査について

<table>
  <thead>
    <tr>
      <th colspan="3">項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="4">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">初期化ボタン</th>
      <th rowspan="2" class="text-vertical-align-middle">削除ボタン</th>
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
      <td><strong>Presence of Genetic Testing</strong></td>
      <td><strong>遺伝学的検査実施の有無</strong></td>
      <td><strong>유전학적 검사 실시 여부</strong></td>
      <td>genotype_presence_of_genetic_testing</td>
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
          <li>Unknown</li>
          <li>Absent</li>
          <li>Present</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>あり</li>
          <li>なし</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>알 수 없음</li>
          <li>없음</li>
          <li>있음</li>
        </ul>
      </td>
      <td>unknown</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Presence of Abnormalities in Genetic Testing</strong></td>
      <td><strong>遺伝学的検査での異常の有無</strong></td>
      <td><strong>유전학적 검사에서 이상 유무</strong></td>
      <td>genotype_presence_of_abnormalities_in_genetic_testing</td>
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
          <li>Unknown</li>
          <li>Absent</li>
          <li>Present</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>あり</li>
          <li>なし</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>알 수 없음</li>
          <li>없음</li>
          <li>있음</li>
        </ul>
      </td>
      <td>unknown</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Genetic Analysis</strong></td>
      <td><strong>遺伝子解析</strong></td>
      <td><strong>유전자 분석</strong></td>
      <td>genotype_analysis</td>
      <td>string</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 検査結果

## 結果詳細