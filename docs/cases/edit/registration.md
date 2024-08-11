
# 登録

## 大項目

| 項目名 | 説明 |
| ---- | ---- |
| **[患者について](#patient-info)** |  |
| **[同意書・アセント](#consent-ascent)** | |

---

## 患者について {: #patient-info}

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
      <td><strong>主病名（疑い病名、症状含む）</strong></td>
      <td>registration_disease_name</td>
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
      <td><strong>未診断 / 既診断 / 非罹患者</strong></td>
      <td>registration_diagnosis_status</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>not_applicable</li>
          <li>undiagnosed</li>
          <li>diagnosed</li>
          <li>non_affected</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>未診断</li>
          <li>既診断</li>
          <li>非罹患者</li>
        </ul>
      </td>
      <td>"not_applicable"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>小児 / 成人</strong></td>
      <td>registration_age_group</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>not_applicable</li>
          <li>child</li>
          <li>adult</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>小児</li>
          <li>成人</li>
        </ul>
      </td>
      <td>"not_applicable"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 同意書・アセント {: #consent-ascent}
