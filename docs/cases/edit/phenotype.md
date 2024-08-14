# 表現型 {: #phenotype}

## 大項目

| 項目名                            | 説明                                             |
| --------------------------------- | ------------------------------------------------ |
| **[臨床症状](#clinical-symptom)** | 臨床症状についての情報を編集することができます。 |

## 臨床症状 {: #clinical-symptom}

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
      <td rowspan="5">臨床症状</td>
      <td>phenotype_hpo_id</td>
      <td>Array&lt;string&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" checked/></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>phenotype_hpo_label</td>
      <td>Array&lt;{ <br />&nbsp name_en: string, <br />&nbsp name_ja: string, <br />&nbsp name_ko: string, <br />&nbsp name_zh: string, <br />&nbsp name_zhcht: string <br /> }&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" checked/></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>phenotype_medical_current_history</td>
    </tr>
    <tr>
      <td>phenotype_process</td>
    </tr>
    <tr>
      <td>phenotype_family_history</td>
    </tr>
  </tbody>
</table>
