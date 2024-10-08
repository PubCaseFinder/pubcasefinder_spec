# 遺伝型 {: #genotype}

遺伝型（ジェノタイプ）のページでは、患者の遺伝学的検査に関する情報を管理します。<br />
これらの情報を体系的に記録することで、患者の遺伝的背景を把握し、適切な診断や治療方針の決定に役立てることができます。<br />
また、家族歴との関連性の分析や、将来的な遺伝カウンセリングの基礎資料としても活用できます。

## 大項目

| 項目名 | 説明 |
| ---- | ---- |
| **[検査について](#about-testing)** | 遺伝学的検査についての情報を編集することができます。 |
| **[検査結果](#testing-result)** | 検査結果についての情報を編集することができます。<br>検査結果は複数登録が可能です。 |
| **[結果詳細](#details-of-result)** | 検査結果の詳細についての情報を編集することができます。<br>検査結果の詳細は複数登録が可能です。 |

---

### 検査について {: #about-testing}

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
      <td><strong>遺伝学的検査実施の有無</strong></td>
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
          <li>不明</li>
          <li>あり</li>
          <li>なし</li>
        </ul>
      </td>
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>遺伝学的検査での異常の有無</strong></td>
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
          <li>不明</li>
          <li>あり</li>
          <li>なし</li>
        </ul>
      </td>
      <td>"unknown"</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>遺伝子解析</strong></td>
      <td>genotype_analysis</td>
      <td>string</td>
      <td>テキストエリア</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.interpretation.interpretation</td>
      <td></td>
    </tr>
  </tbody>
</table>

### 検査結果 {: #testing-result}

- 下記項目群を1つの検査結果とし、複数の検査結果を登録可能
    - 各項目のデータは検査結果の登録数分の配列
        - 例）1つ目の検査結果は各項目の配列の0番目
- 検査結果はボタン操作で「追加」「削除」が可能
    - 「削除」ボタン押下時は下記文言の確認アラートを表示し、「OK」押下時のみ実行
        - 「削除しますか？」

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
      <td><strong>検査実施日(yyyy/mm/dd)</strong></td>
      <td>genotype_date_of_testing</td>
      <td>Array&lt;string|null&gt;</td>
      <td>カレンダー選択</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>値の持ち方は、yyyy-MM-dd形式</td>
    </tr>
    <tr>
      <td><strong>検査会社/施設名</strong></td>
      <td>genotype_testing_company_name</td>
      <td>Array&lt;string|null&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>SRL</li>
          <li>かずさDNA研究所</li>
          <li>FALCOバイオシステムズ</li>
          <li>BML</li>
          <li>保健科学研究所</li>
          <li>ラボコープ・ジャパン</li>
          <li>LSI メディエンス</li>
          <li>学術研究</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>SRL</li>
          <li>かずさDNA研究所</li>
          <li>FALCOバイオシステムズ</li>
          <li>BML</li>
          <li>保健科学研究所</li>
          <li>ラボコープ・ジャパン</li>
          <li>LSI メディエンス</li>
          <li>学術研究</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>検査種別</strong></td>
      <td>genotype_type_of_testing</td>
      <td>Array&lt;string|null&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>g_band_method</li>
          <li>subtelomere_fish</li>
          <li>microarray</li>
          <li>others</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>G-band法</li>
          <li>サブテロメアFISH</li>
          <li>マイクロアレイ</li>
          <li>その他</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>その他詳細</strong></td>
      <td>genotype_testing_other_details</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td>
        検査種別で「その他」を選択している時のみ入力可<br>
        （それ以外の場合は非活性）
      </td>
    </tr>
    <tr>
      <td><strong>検査結果</strong></td>
      <td>genotype_result_of_testing</td>
      <td>Array&lt;string|null&gt;</td>
      <td>ラジオボタン</td>
      <td>
        <ul>
          <li>unknown</li>
          <li>negative</li>
          <li>positive</li>
          <li>in_progress</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>陰性</li>
          <li>陽性</li>
          <li>検査中</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

### 結果詳細 {: #details-of-result}

- 下記項目群を1つの結果詳細とし、複数の結果詳細を登録可能
    - 各項目のデータは結果詳細の登録数分の配列
        - 例）1つ目の結果詳細は各項目の配列の0番目
- 結果詳細はボタン操作で「追加」「削除」が可能
    - 「削除」ボタン押下時は下記文言の確認アラートを表示し、「OK」押下時のみ実行
        - 「削除しますか？」

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
      <td><strong>Gene symbol</strong></td>
      <td>genotype_gene</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.interpretation.diagnosis.genomic_interpretations[i]<br>.gene.symbol</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>NCBI Gene ID</strong></td>
      <td>genotype_ncbi_gene_id</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Ensemble ID</strong></td>
      <td>genotype_ensembl_id</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Interpretation Status</strong></td>
      <td>genotype_status</td>
      <td>Array&lt;string|null&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>Unknown Status</li>
          <li>Rejected</li>
          <li>Candidate</li>
          <li>Contributory</li>
          <li>Causative</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Unknown Status</li>
          <li>Rejected</li>
          <li>Candidate</li>
          <li>Contributory</li>
          <li>Causative</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.interpretation.diagnosis.genomic_interpretations[i]<br>.interpretationStatus</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>cDNA Change</strong></td>
      <td>genotype_cdna_change</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>
        proband.interpretation.diagnosis.genomic_interpretations[i]<br>.call.variation_descriptor.expressions.valueのkey名<br><br>
        ※key名に対する値はgenotype_transcript
      </td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Pathogenicity</strong></td>
      <td>genotype_pathogenicity</td>
      <td>Array&lt;string|null&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>NOT_PROVIDED</li>
          <li>BENIGN</li>
          <li>LIKELY_BENIGN</li>
          <li>UNCERTAIN_SIGNIFICANCE</li>
          <li>LIKELY_PATHOGENIC</li>
          <li>PATHOGENIC</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>NOT_PROVIDED</li>
          <li>BENIGN</li>
          <li>LIKELY_BENIGN</li>
          <li>UNCERTAIN_SIGNIFICANCE</li>
          <li>LIKELY_PATHOGENIC</li>
          <li>PATHOGENIC</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>proband.interpretation.diagnosis.genomic_interpretations[i]<br>.variantInterpretation.acmgPathogenicityClassification</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Genotype</strong></td>
      <td>genotype_allelic_state</td>
      <td>Array&lt;string|null&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>heterozygous</li>
          <li>homozygous</li>
          <li>hemizygous</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>heterozygous</li>
          <li>homozygous</li>
          <li>hemizygous</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>
        proband.interpretation.diagnosis.genomic_interpretations[i]<br>.call.variation_descriptor.allelic_state<br><br>
        ※下記objectで格納<br>
        { id: xxx, label: genotype_allelic_state }<br>
        →idのxxx部分はgenotype_allelic_stateの値によって下記対応する値<br>
        <ul>
          <li>heterozygous: GENO:0000135</li>
          <li>homozygous: GENO:0000136</li>
          <li>hemizygous: GENO:0000134</li>
        </ul>
      </td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Reference</strong></td>
      <td>genotype_reference</td>
      <td>Array&lt;string|null&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>GRCh37 (hg19)</li>
          <li>GRCh38 (hg38)</li>
          <li>GRCh36 (hg18)</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>GRCh37 (hg19)</li>
          <li>GRCh38 (hg38)</li>
          <li>GRCh36 (hg18)</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Chr:Position</strong></td>
      <td>genotype_chr_position</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Transcript</strong></td>
      <td>genotype_transcript</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>
        proband.interpretation.diagnosis.genomic_interpretations[i]<br>.call.variation_descriptor.expressions.valueのkeyに対する値<br><br>
        ※key名はgenotype_cdna_change
      </td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Protein Charge</strong></td>
      <td>genotype_protein_charge</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Annotation</strong></td>
      <td>genotype_annotation</td>
      <td>Array&lt;string|null&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>frameshift deletion</li>
          <li>frameshift insertion</li>
          <li>frameshift substitution</li>
          <li>nonframeshift deletion</li>
          <li>nonframeshift insertion</li>
          <li>nonframeshift substitution</li>
          <li>synonymous SNV</li>
          <li>nonsynonymous SNV</li>
          <li>stopgain SNV</li>
          <li>stoploss SNV</li>
          <li>stopgain</li>
          <li>stoploss</li>
          <li>splicing</li>
          <li>other</li>
          <li>unknown</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>frameshift deletion</li>
          <li>frameshift insertion</li>
          <li>frameshift substitution</li>
          <li>nonframeshift deletion</li>
          <li>nonframeshift insertion</li>
          <li>nonframeshift substitution</li>
          <li>synonymous SNV</li>
          <li>nonsynonymous SNV</li>
          <li>stopgain SNV</li>
          <li>stoploss SNV</li>
          <li>stopgain</li>
          <li>stoploss</li>
          <li>splicing</li>
          <li>other</li>
          <li>unknown</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Inheritance</strong></td>
      <td>genotype_inheritance</td>
      <td>Array&lt;string|null&gt;</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>autosomal recessive - compound heterozygous</li>
          <li>autosomal recessive - homozygous</li>
          <li>autosomal dominant</li>
          <li>autosomal dominant - new mutation</li>
          <li>autosomal dominant - Inherited mutation</li>
          <li>x-linked recessive</li>
          <li>x-linked dominant</li>
          <li>paternal imprinting</li>
          <li>maternal imprinting</li>
          <li>other</li>
          <li>unknown</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>autosomal recessive - compound heterozygous</li>
          <li>autosomal recessive - homozygous</li>
          <li>autosomal dominant</li>
          <li>autosomal dominant - new mutation</li>
          <li>autosomal dominant - Inherited mutation</li>
          <li>x-linked recessive</li>
          <li>x-linked dominant</li>
          <li>paternal imprinting</li>
          <li>maternal imprinting</li>
          <li>other</li>
          <li>unknown</li>
        </ul>
      </td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Comments</strong></td>
      <td>genotype_comments</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>[]</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>
