# 検体・検査

このページでは、患者の検体情報と各種検査結果を管理します。<br />
検体・検査情報は、診断や治療方針の決定に重要な役割を果たします。<br />
また、経時的な変化の追跡や、他の臨床情報との関連性の分析にも役立ちます。

## 大項目

| 項目名                             | 説明                                                                                   |
| ---------------------------------- | -------------------------------------------------------------------------------------- |
| **[検体採取](#sample_collection)** | 検体採取に関する情報を編集することができます。                                         |
| **[血液検査等](#blood_test)**      | 血液検査等に関する情報を編集することができます。                                       |
| **[その他検査](#other_test)**      | その他検査に関する情報を編集することができます。<br />その他検査は複数登録が可能です。 |

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
      <td>カレンダー選択</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>「{{YYYY}}-{{MM}}-{{DD}}」の形式でjsonに保存される</td>
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
      <td>Array&lt;string|null&gt;</td>
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
      <td>検体種別で「その他」を選択している時のみ入力可（それ以外の場合は非活性）</td>
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
      <td rowspan="3">
        追加ボタンから項目を増やすことが可能。各キーには配列として保存される。
      </td>
    </tr>
    <tr>
      <td><strong>投与経路</strong></td>
      <td>sample_route_of_administration</td>
      <td>Array&lt;string|null&gt;</td>
      <td>セレクトボックス</td>
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
    </tr>
  </tbody>
</table>

## 血液検査等 {: #blood_test}

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
      <td><strong>検査実施日（yyyy/mm/dd）</strong></td>
      <td>sample_test_date</td>
      <td>string|null</td>
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
      <td><strong>白血球数（WBC）</strong></td>
      <td>sample_wbc</td>
      <td>string|null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td rowspan="7">数字以外を入力すると、数字制限アラートが表示される</td>
    </tr>
    <tr>
      <td><strong>赤血球数（RBC）</strong></td>
      <td>sample_rbc</td>
      <td>string|null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>血色素（ヘモグロビン）</strong></td>
      <td>sample_hemoglobin</td>
      <td>string|null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>ヘマトクリット</strong></td>
      <td>sample_hematocrit</td>
      <td>string|null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>血小板数（PLT）</strong></td>
      <td>sample_plt</td>
      <td>string|null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>総タンパク（TP）</strong></td>
      <td>sample_tp</td>
      <td>string|null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>アルブミン（ALB）</strong></td>
      <td>sample_alb</td>
      <td>string|null</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
  </tbody>
</table>

## その他検査 {: #other_test}

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
      <td><strong>検査項目名</strong></td>
      <td>sample_test_item</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="3"><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td rowspan="3">追加ボタンから項目を増やすことが可能。各キーには配列として保存される。</td>
    </tr>
    <tr>
      <td><strong>検査値</strong></td>
      <td>sample_test_value</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>単位</strong></td>
      <td>sample_test_unit</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
  </tbody>
</table>
