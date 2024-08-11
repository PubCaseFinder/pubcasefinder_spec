
# 検体・検査

## 大項目

| 項目名 | 説明 |
| ---- | ---- |
| **[検体採取](#sample_collection)** |  |
| **[血液検査等](#blood_test)** | |
| **[その他検査](#other_test)** | |

---

## 検体採取 {: #sample_collection}

<table>
  <thead>
    <tr>
      <th rowspan="2">中項目</th>
      <th rowspan="2">小項目</th>
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
      <td><strong>採取時年月日（yyyy/mm/dd）</strong></td>
      <td><strong>-</strong></td>
      <td>sample_sampling_date</td>
      <td>string | null</td>
      <td>日付選択インターフェース</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>検体識別ID</strong></td>
      <td><strong>-</strong></td>
      <td>sample_id</td>
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
      <td><strong>採取時の治療薬の有無</strong></td>
      <td><strong>-</strong></td>
      <td>sample_presense_of_treatment_drug_at_sampling</td>
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
      <td><strong>検体種別</strong></td>
      <td><strong>-</strong></td>
      <td>sample_type</td>
      <td>string | null</td>
      <td>チェックボックス</td>
      <td>
        <ul>
          <li>blood</li>
          <li>tissue</li>
          <li>saliva</li>
          <li>other</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>血液</li>
          <li>組織</li>
          <li>唾液</li>
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
      <td>sample_type_other_detail</td>
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
      <td rowspan="3"><strong>検体採取時の処方内容</strong></td>
      <td><strong>処方内容</strong></td>
      <td>sample_prescription</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>投与経路</strong></td>
      <td>sample_route_of_administration</td>
      <td>Array&lt;string|null&gt;</td>
      <td>プルダウン</td>
      <td>
        <ul>
          <li>oral</li>
          <li>injection</li>
          <li>external</li>
          <li>other</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>内服</li>
          <li>注射</li>
          <li>外用</li>
          <li>その他</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>YJコード</strong></td>
      <td>sample_yj_code</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 血液検査等 {: #blood_test}


## その他検査 {: #other_test}

