# 家系

## 大項目

| 項目名 | 説明 |
| ---- | ---- |
| **[家族歴](#family-history)** |  |
| **[遺伝形式](#mode-of-inheritance)** | |
| **[親族（がん・生活習慣病）](#relatives)** | |
| **[民族](#ethnicity)** | |
| **[近親婚](#consanguinity)** | |
| **[家系図](#pedigree)** | |

---

## 家族歴 {: #family-history}

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
      <td><strong>家族歴</strong></td>
      <td>family_history</td>
      <td>string</td>
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
      <td><strong>家族内発症の有無</strong></td>
      <td>family_presence_of_onset_in_family</td>
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
      <td>unknown</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>その他の罹患近親者</strong></td>
      <td>family_other_affected_relatives</td>
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
      <td>unknown</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>母親の死産・流産の有無</strong></td>
      <td>family_presence_of_miscarriage_or_stillbirth_of_mother</td>
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
      <td>unknown</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>死産の回数</strong></td>
      <td>family_number_of_stillbirth_of_mother</td>
      <td>string</td>
      <td>テキストボックス (数字)</td>
      <td>-</td>
      <td>-</td>
      <td>unknown</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>流産 (自然) の回数</strong></td>
      <td>family_number_of_miscarriage_of_mother</td>
      <td>string</td>
      <td>テキストボックス (数字)</td>
      <td>-</td>
      <td>-</td>
      <td>unknown</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>流産 (人工) の回数</strong></td>
      <td>family_number_of_artificial_abortion_of_mother</td>
      <td>string</td>
      <td>テキストボックス (数字)</td>
      <td>-</td>
      <td>-</td>
      <td>unknown</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 遺伝形式 {: #mode-of-inheritance}

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
      <td><strong>遺伝形式</strong></td>
      <td>family_mode_inheritance</td>
      <td>string</td>
      <td>ラジオボタン（階層あり）</td>
      <td>
        <ul>
          <li>Sporadic</li>
          <li>Autosomal dominant inheritance</li>
          <li>Sex-limited autosomal dominant</li>
          <li>Autosomal dominant somatic cell mutation</li>
          <li>Autosomal dominant contiguous gene syndrome</li>
          <li>Autosomal recessive inheritance</li>
          <li>
            Gonosomal inheritance
            <ul>
              <li>X-linked inheritance</li>
              <li>X-linked dominant inheritance</li>
              <li>X-linked recessive inheritance</li>
              <li>Y-linked inheritance</li>
            </ul>
          </li>
          <li>
            Multifactorial inheritance
            <ul>
              <li>Digenic inheritance</li>
              <li>Oligogenic inheritance</li>
              <li>Polygenic inheritance</li>
            </ul>
          </li>
          <li>Mitochondrial inheritance</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Sporadic</li>
          <li>Autosomal dominant inheritance</li>
          <li>Sex-limited autosomal dominant</li>
          <li>Autosomal dominant somatic cell mutation</li>
          <li>Autosomal dominant contiguous gene syndrome</li>
          <li>Autosomal recessive inheritance</li>
          <li>
            Gonosomal inheritance
            <ul>
              <li>X-linked inheritance</li>
              <li>X-linked dominant inheritance</li>
              <li>X-linked recessive inheritance</li>
              <li>Y-linked inheritance</li>
            </ul>
          </li>
          <li>
            Multifactorial inheritance
            <ul>
              <li>Digenic inheritance</li>
              <li>Oligogenic inheritance</li>
              <li>Polygenic inheritance</li>
            </ul>
          </li>
          <li>Mitochondrial inheritance</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 親族（がん・生活習慣病） {: #relatives}

## 民族 {: #ethnicity}

## 近親婚 {: #consanguinity}

## 家系図 {: #pedigree}
