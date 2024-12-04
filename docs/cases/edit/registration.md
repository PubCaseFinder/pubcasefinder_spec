# 登録

このページでは、患者の登録に関する基本的な情報を管理します。<br />
ここで入力される情報は、患者の初期評価や診断プロセスの開始点となります。<br />
主な内容には、患者の主病名、診断状況、同意書の取得状況などが含まれます。<br />

## 大項目

| 項目名                                  | 説明                                                         |
| --------------------------------------- | ------------------------------------------------------------ |
| **[患者について](#patient-info)**       | 患者に関する主病名、診断状況を編集することができます。       |
| **[同意書・アセント](#consent-ascent)** | 患者に関する同意書・アセントの詳細を編集することができます。 |

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
    <tr>
      <td><strong>遺伝性疾患 / 非遺伝性疾患</strong></td>
      <td>registration_genetic_status</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>not_applicable</li>
          <li>genetic</li>
          <li>non_genetic</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>遺伝性疾患</li>
          <li>非遺伝性疾患</li>
        </ul>
      </td>
      <td>"not_applicable"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>罹患有無</strong></td>
      <td>registration_affection</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>not_applicable</li>
          <li>affected</li>
          <li>not_affected</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>罹患</li>
          <li>非罹患</li>
        </ul>
      </td>
      <td>"not_applicable"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>備考</strong></td>
      <td>registration_note</td>
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
  </tbody>
</table>

## 同意書・アセント {: #consent-ascent}

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
      <td><strong>同意書の種別</strong></td>
      <td>registration_consent_form_type</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>not_applicable</li>
          <li>initial_consent</li>
          <li>re_consent</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>初回同意</li>
          <li>再同意</li>
        </ul>
      </td>
      <td>"not_applicable"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>同意取得者</strong></td>
      <td>registration_consent_acquirer</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>not_applicable</li>
          <li>patient</li>
          <li>proxy</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>本人</li>
          <li>代諾者等</li>
        </ul>
      </td>
      <td>"not_applicable"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>同意取得 代諾者等の続柄</strong></td>
      <td>registration_proxy_relation</td>
      <td>string | null</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>father</li>
          <li>mother</li>
          <li>grandfather</li>
          <li>grandmother</li>
          <li>spouse</li>
          <li>child</li>
          <li>sibling</li>
          <li>uncle</li>
          <li>aunt</li>
          <li>other</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>父</li>
          <li>母</li>
          <li>祖父</li>
          <li>祖母</li>
          <li>配偶者</li>
          <li>子ども</li>
          <li>同胞</li>
          <li>おじ</li>
          <li>おば</li>
          <li>その他</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>同意取得者で「代諾者等」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>その他詳細</strong></td>
      <td>registration_proxy_relation_other</td>
      <td>string | null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>代諾者等の続柄で「その他」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>同意書のバージョン</strong></td>
      <td>registration_consent_form_version</td>
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
      <td><strong>アセントの有無</strong></td>
      <td>registration_ascent</td>
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
      <td><strong>アセントのバージョン</strong></td>
      <td>registration_ascent_version</td>
      <td>string | null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>アセントの有無で「あり」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>同意取得日（yyyy/mm/dd）</strong></td>
      <td>registration_consent_acquisition_date</td>
      <td>string | null</td>
      <td>日付入力インターフェース</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>「{{YYYY}}-{{MM}}-{{DD}}」の形式でjsonに保存される</td>
    </tr>
    <tr>
      <td><strong>同意撤回の有無</strong></td>
      <td>registration_consent_withdrawal</td>
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
      <td><strong>同意撤回者</strong></td>
      <td>registration_consent_withdrawer</td>
      <td>string</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>not_applicable</li>
          <li>patient</li>
          <li>proxy</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>本人</li>
          <li>代諾者等</li>
        </ul>
      </td>
      <td>"not_applicable"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td rowspan="5">同意撤回の有無で「あり」を選択している時のみ入力可（それ以外の場合は非活性）</td>
    </tr>
    <tr>
      <td><strong>同意撤回 代諾者等の続柄</strong></td>
      <td>registration_proxy_relation_withdrawer</td>
      <td>string | null</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>father</li>
          <li>mother</li>
          <li>grandfather</li>
          <li>grandmother</li>
          <li>spouse</li>
          <li>child</li>
          <li>sibling</li>
          <li>uncle</li>
          <li>aunt</li>
          <li>other</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>父</li>
          <li>母</li>
          <li>祖父</li>
          <li>祖母</li>
          <li>配偶者</li>
          <li>子ども</li>
          <li>同胞</li>
          <li>おじ</li>
          <li>おば</li>
          <li>その他</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>その他詳細</strong></td>
      <td>registration_proxy_relation_withdrawer_other_details</td>
      <td>string | null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>同意撤回書のバージョン</strong></td>
      <td>registration_consent_withdrawal_version</td>
      <td>string | null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>同意撤回アセントの有無</strong></td>
      <td>registration_ascent_withdrawer</td>
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
    </tr>
    <tr>
      <td><strong>同意撤回アセントのバージョン</strong></td>
      <td>registration_ascent_withdrawal_version</td>
      <td>string | null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td rowspan="2">同意撤回アセントの有無で「あり」を選択している時のみ入力可（それ以外の場合は非活性）<br>「{{YYYY}}-{{MM}}-{{DD}}」の形式でjsonに保存される</td>
    </tr>
    <tr>
      <td><strong>同意撤回日（yyyy/mm/dd）</strong></td>
      <td>registration_consent_withdrawal_date</td>
      <td>string | null</td>
      <td>日付入力インターフェース</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
  </tbody>
</table>
