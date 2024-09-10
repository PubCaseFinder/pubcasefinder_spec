# 表現型 {: #phenotype}

表現型（フェノタイプ）は、個体の観察可能な特徴や性質を指します。<br />
遺伝子型（ジェノタイプ）が遺伝的な構成を表すのに対し、表現型はその遺伝的構成が外部に現れた結果を示します。<br />
医療や遺伝学の文脈では、表現型は患者の症状、身体的特徴、生理学的特性などを包括的に指します。

## 大項目

| 項目名                                 | 説明                                                                                                                       |
| -------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **[臨床症状](#clinical-symptom)**      | 患者の兆候または症状を入力して、症状一覧に追加することができます。<br />臨床症状は入力内容をもとにサジェストを表示します。 |
| **[症状一覧](#clinical-symptom-list)** | 臨床症状から追加された症状を一覧で表示することができます。<br /> 詳細の表示や絞り込み検索ができます。                      |

## 臨床症状 {: #clinical-symptom}

<img style="border: 1px solid #ccc;" src="../../../assets/images/cases_edit_phenotype_form.png">

### 機能一覧

<!-- prettier-ignore -->
| 番号 | 機能 | 詳細 |
| ---- | ---- | ---- |
| 1 | 症状入力欄 | 入力した文言に応じて、データベースに保存されているHPO（Human Phenotype Ontology）症状がサジェストとして表示され、症状を選択すると入力を確定し、タグとして表示されます。<br /> タグの機能の詳細は「[タグ機能の詳細](#tag-detail)」を参照してください。 |
| 2 | 文章から症状を自動抽出 | ボタンをクリックすると文章入力欄が表示されます。文章入力欄に入力した内容から症状を推測して表示し、症状入力欄に追加することができます。 |
| 3 | 設定 | タグサイズ、クエリー言語を設定することができます。クエリー言語とはjsonに保存される値の言語のことです。 |
| 4 | 症状の分類わけ | 症状を現病歴、既往歴、経過、家族歴のいずれかに分類することができます。 |
| 5 | 症状一括削除 | 入力した症状を一括削除することができます。 |
| 6 | 一覧に追加 | 入力した症状を一覧に追加することができます。 |

### タグ機能の詳細 {: #tag-detail}

タグを押すと、症状詳細表示モーダル・上位概念モーダル・下位概念モーダルが表示されます。

#### 症状詳細表示モーダル

初期表示では選択したタグの症状詳細が表示されます。
上位概念モーダル・下位概念モーダルで症状を選択した場合、症状詳細表示モーダルの内容は選択した症状詳細に置き換わります。

| 番号 | 機能         | 詳細                                                                                   |
| ---- | ------------ | -------------------------------------------------------------------------------------- |
| 1    | 追加         | モーダル内に表示されている症状を症状入力欄にタグとして追加します。                     |
| 2    | 置換         | 初期表示で選択していたタグを、現在モーダル内に表示されている症状のタグに置き換えます。 |
| 3    | コピー       | クリップボードに「{{ HPO ID }},{{ 症状(日) }},{{ 症状(英) }}」の形式でコピーします。   |
| 4    | 言語切り替え | モーダル内の言語をセレクトボックスで選択した言語に切り替えます。                       |

表示される症状詳細の項目は、以下の通りです。

| 項目名     | 詳細                                                                                    |
| ---------- | --------------------------------------------------------------------------------------- |
| 症状の有無 | 症状の有無を選択することができます。json での phenotype_excluded に相当します。         |
| HPO ID     | 症状の HPO ID が表示されます。json での phenotype_hpo_id に相当します。                 |
| 症状(日)   | 症状の日本語名が表示されます。json での phenotype_hpo_label.name_ja に相当します。      |
| 症状(英)   | 症状の英語名が表示されます。json での phenotype_hpo_label.name_en に相当します。        |
| 症状定義   | 症状の定義が表示されます。json には保存されない値です。                                 |
| コメント   | 入力した症状を一覧に追加することができます。json での phenotype_comments に相当します。 |
| 同義語     | 入力した症状を一覧に追加することができます。json には保存されない値です。               |

#### 上位概念モーダル

#### 下位概念モーダル

### 項目詳細

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
      <td rowspan="2">テキストボックス</td>
      <td rowspan="2">-</td>
      <td rowspan="2">-</td>
      <td>[]</td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" checked/></td>
      <td rowspan="2"><input type="checkbox" class="readonly-input" /></td>
      <td>proband.phenotypic_features.type.id</td>
      <td rowspan="2">
        <ul>
          <li>テキストボックスに入力する度に「/tokeninput_hpo」エンドポイントを呼ぶことで、独自のデータベースからHPOデータを取得しサジェストとして表示する</li>
          <li>phenotype_hpo_labelの値は設定のクエリー言語で選択した言語で保存される</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>phenotype_hpo_label</td>
      <td>Array&lt;{ <br />&nbsp name_en: string, <br />&nbsp name_ja: string, <br />&nbsp name_ko: string, <br />&nbsp name_zh: string, <br />&nbsp name_zhcht: string <br /> }&gt;</td>
      <td>[]</td>
      <td>proband.phenotypic_features.type.label</td>
    </tr>
  </tbody>
</table>

## 症状一覧 {: #clinical-symptom-list}

<img style="border: 1px solid #ccc" src="../../../assets/images/cases_edit_phenotype_list.png">

### 機能一覧

<!-- prettier-ignore -->
| 番号 | 機能 | 詳細 |
| ---- | ---- | ---- |
| 1 | 症状詳細表示 | 症状詳細を表示することができます。 |
| 2 | HPO詳細表示 | HPO詳細を表示することができます。 |
| 3 | 症状削除 | 症状を削除することができます。 |
| 4 | 常に症状詳細を表示 | 症状詳細表示ボタンを押さなくても、症状詳細を常に表示状態にします。 |
| 5 | 症状絞り込み検索 | 症状の詳細で絞り込み検索ができます。 |

### 各症状毎の項目詳細

<table>
  <thead>
    <tr>
      <th rowspan="2" class="text-vertical-align-middle">項目名</th>
      <th rowspan="2" class="text-vertical-align-middle">ID</th>
      <th rowspan="2" class="text-vertical-align-middle">型定義</th>
      <th rowspan="2" class="text-vertical-align-middle">入力形式</th>
      <th colspan="2">選択肢</th>
      <th rowspan="2" class="text-vertical-align-middle">初期値</th>
      <th rowspan="2" class="text-vertical-align-middle">各症状の初期値</th>
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
      <td>現病歴</td>
      <td>phenotype_medical_current_history</td>
      <td>Array&lt;string&gt;</td>
      <td>チェックボックス</td>
      <td>
        <ul>
          <li>無</li>
          <li>有</li>
        </ul>
      </td>
      <td>-</td>
      <td>[]</td>
      <td>"無"</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>既往歴</td>
      <td>phenotype_medical_previous_history</td>
      <td>Array&lt;string&gt;</td>
      <td>チェックボックス</td>
      <td>
        <ul>
          <li>無</li>
          <li>有</li>
        </ul>
      </td>
      <td>-</td>
      <td>[]</td>
      <td>"無"</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>経過</td>
      <td>phenotype_process</td>
      <td>Array&lt;string&gt;</td>
      <td>チェックボックス</td>
      <td>
        <ul>
          <li>無</li>
          <li>有</li>
        </ul>
      </td>
      <td>-</td>
      <td>[]</td>
      <td>"無"</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>家族歴</td>
      <td>phenotype_family_history</td>
      <td>Array&lt;string&gt;</td>
      <td>チェックボックス</td>
      <td>
        <ul>
          <li>無</li>
          <li>有</li>
        </ul>
      </td>
      <td>-</td>
      <td>[]</td>
      <td>"無"</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>症状の有無</td>
      <td>phenotype_excluded</td>
      <td>Array&lt;string&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>症状あり</li>
          <li>症状なし</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>yes</li>
          <li>no</li>
        </ul>
      </td>
      <td>[]</td>
      <td>"no"</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.phenotypic_features.excluded</td>
      <td></td>
    </tr>
    <tr>
      <td>重要性</td>
      <td>phenotype_clinical_relevance</td>
      <td>Array&lt;string&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>通常</li>
          <li>高い</li>
          <li>低い</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>normal</li>
          <li>distinctive</li>
          <li>minor</li>
        </ul>
      </td>
      <td>[]</td>
      <td>"normal"</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.phenotypic_features.modifiers</td>
      <td></td>
    </tr>
    <tr>
      <td>重症度</td>
      <td>phenotype_severity</td>
      <td>Array&lt;string&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>境界域</li>
          <li>重度</li>
          <li>最重度</li>
          <li>中等度</li>
          <li>軽度</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>borderline</li>
          <li>severe</li>
          <li>profound</li>
          <li>moderate</li>
          <li>mild</li>
        </ul>
      </td>
      <td>[]</td>
      <td>"borderline"</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.phenotypic_features.severity</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3">発症年齢 (YMD)</td>
      <td rowspan="3">phenotype_age_onset</td>
      <td rowspan="3">Array&lt;string&gt;</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td rowspan="3">[]</td>
      <td rowspan="3">""</td>
      <td rowspan="3"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="3"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="3">proband.phenotypic_features.onset</td>
      <td rowspan="3">「{{yy}} + Y + {{mm}} + M + {{dd}} + D」の形式でjsonに保存される</td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>0 ~ 11</td>
      <td>0 ~ 11</td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>1 ~ 31</td>
      <td>1 ~ 31</td>
    </tr>
    <tr>
      <td>発症パターン</td>
      <td>phenotype_temporal_pattern</td>
      <td>Array&lt;string&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>unknown</li>
          <li>recurrent</li>
          <li>subacute</li>
          <li>fluctuating</li>
          <li>migratory</li>
          <li>diurnal</li>
          <li>stable</li>
          <li>insidious</li>
          <li>prolonged</li>
          <li>nocturnal</li>
          <li>chronic</li>
          <li>transient</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Unknown</li>
          <li>Recurrent Acute</li>
          <li>Subacute</li>
          <li>Fluctuating</li>
          <li>Migratory</li>
          <li>Diurnal</li>
          <li>Stable</li>
          <li>Insidious onset</li>
          <li>Prolonged</li>
          <li>Nocturnal</li>
          <li>Chronic</li>
          <li>Transient</li>
        </ul>
      </td>
      <td>[]</td>
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>進行速度</td>
      <td>phenotype_pace_progression</td>
      <td>Array&lt;string&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>Unknown</li>
          <li>Progressive</li>
          <li>Variable progression rate</li>
          <li>Slowly progressive</li>
          <li>Nonprogressive</li>
          <li>Rapidly progressive</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Unknown</li>
          <li>Progressive</li>
          <li>Variable progression rate</li>
          <li>Slowly progressive</li>
          <li>Nonprogressive</li>
          <li>Rapidly progressive</li>
        </ul>
      </td>
      <td>[]</td>
      <td>"Unknown"</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3">消失年齢 (YMD)</td>
      <td rowspan="3">phenotype_resolution</td>
      <td rowspan="3">Array&lt;string&gt;</td>
      <td>テキストボックス（数字）</td>
      <td>-</td>
      <td>-</td>
      <td rowspan="3">[]</td>
      <td rowspan="3">""</td>
      <td rowspan="3"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="3"><input type="checkbox" class="readonly-input" /></td>
      <td rowspan="3">proband.phenotypic_features.resolution</td>
      <td rowspan="3">「{{yy}} + Y + {{mm}} + M + {{dd}} + D」の形式でjsonに保存される</td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>0 ~ 11</td>
      <td>0 ~ 11</td>
    </tr>
    <tr>
      <td>セレクトボックス</td>
      <td>1 ~ 31</td>
      <td>1 ~ 31</td>
    </tr>
    <tr>
      <td>コメント</td>
      <td>phenotype_comments</td>
      <td>Array&lt;string&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.phenotypic_features.description</td>
      <td></td>
    </tr>
  </tbody>
</table>
