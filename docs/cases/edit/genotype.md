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

下記項目群を1つの検査結果とし、複数の検査結果を登録可能。<br>
検査結果はボタン操作で「追加」「削除」を行う。

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
      <td><strong>Date of Testing (yyyy/mm/dd)</strong></td>
      <td><strong>検査実施日(yyyy/mm/dd)</strong></td>
      <td><strong>검사 실시일(yyyy/mm/dd)</strong></td>
      <td>genotype_date_of_testing</td>
      <td>Array&lt;string|null&gt;</td>
      <td>カレンダー選択</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>値の持ち方は、YYYY-MM-DD形式</td>
    </tr>
    <tr>
      <td><strong>Testing Company/Facility Name</strong></td>
      <td><strong>検査会社/施設名</strong></td>
      <td><strong>검사회사/시설명</strong></td>
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
      <td>-</td>
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
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Type of Testing</strong></td>
      <td><strong>検査種別</strong></td>
      <td><strong>검사 종류</strong></td>
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
          <li>G-band method</li>
          <li>Subtelomere FISH</li>
          <li>Microarray</li>
          <li>Others</li>
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
      <td>
        <ul>
          <li>G-band법</li>
          <li>서브테로미어 FISH</li>
          <li>마이크로 어레이</li>
          <li>기타</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Other Details of Testing</strong></td>
      <td><strong>その他詳細</strong></td>
      <td><strong>기타 상세 정보</strong></td>
      <td>genotype_testing_other_details</td>
      <td>Array&lt;string|null&gt;</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td>
        検査種別で「その他」を選択している時のみ入力可<br>
        （それ以外の場合は非活性）
      </td>
    </tr>
    <tr>
      <td><strong>Result of Testing</strong></td>
      <td><strong>検査結果</strong></td>
      <td><strong>검사 결과</strong></td>
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
          <li>Unknown</li>
          <li>Negative</li>
          <li>Positive</li>
          <li>In progress</li>
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
      <td>
        <ul>
          <li>알 수 없음</li>
          <li>음성</li>
          <li>양성</li>
          <li>검사 중</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 結果詳細
