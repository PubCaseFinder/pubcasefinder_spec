# 症例基本情報（EN: `Case Info`, KO: `의료사례 기본 정보`） {: #case-info}

## ID（EN: `ID`, KO: `ID`） {: #id}

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
      <th colspan="3">一覧表示/操作</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
      <th>デフォルト表示</th>
      <th>編集可能</th>
      <th>列追加可能</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>PCF No.</strong></td>
      <td>PCFNo</td>
      <td>string</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>P + {{作成年}} + {{月}} + {{日}} + {{時間}} + {{秒}} + {{ミリ秒}}</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>症例ID</strong></td>
      <td>case_id</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>C + {{表示中の症例の連番7桁}}</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>1</td>
      <td>proband.id. / subject.id / pedigree.persons.individual_id</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>家族ID</strong></td>
      <td>case_family_id</td>
      <td>string</td>
      <td>テキストボックス、セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>1</td>
      <td>id  / pedigree.persons.family_id</td>
      <td>一覧に表示中の家族IDをプルダウンから選択可能</td>
    </tr>
    <tr>
      <td><strong>グループ名</strong></td>
      <td>case_group</td>
      <td>string</td>
      <td>テキストボックス、セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>""</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>1</td>
      <td></td>
      <td>一覧に表示中のグループIDをプルダウンから選択可能</td>
    </tr>
  </tbody>
</table>

## 基本情報（EN: `Basic Info`, KO: `기본 정보`） {: #basic-info}

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
      <th colspan="3">一覧表示/操作</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
      <th>デフォルト表示</th>
      <th>編集可能</th>
      <th>列追加可能</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>続柄</strong></td>
      <td>case_relationship</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>proband_individual</li>
          <li>father</li>
          <li>mother</li>
          <li>parent_unknown</li>
          <li>spouse_proband</li>
          <li>spouse_child</li>
          <li>spouse_sibling</li>
          <li>spouse_uncle_aunt</li>
          <li>sibling</li>
          <li>child</li>
          <li>grandparent_paternal</li>
          <li>grandparent_maternal</li>
          <li>grandparent_unknown</li>
          <li>uncle_paternal</li>
          <li>uncle_maternal</li>
          <li>aunt_paternal</li>
          <li>aunt_maternal</li>
          <li>nephew_niece</li>
          <li>grandchild</li>
          <li>cousin</li>
          <li>unknown</li>
          <li>other_paternal</li>
          <li>other_maternal</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>発端者（本人）</li>
          <li>父</li>
          <li>母</li>
          <li>親（詳細不明）</li>
          <li>本人の配偶者</li>
          <li>子どもの配偶者</li>
          <li>兄弟の配偶者</li>
          <li>おじおばの配偶者</li>
          <li>同胞</li>
          <li>子ども</li>
          <li>祖父母（父方）</li>
          <li>祖父母（母方）</li>
          <li>祖父母（詳細不明）</li>
          <li>おじ（父方）</li>
          <li>おじ（母方）</li>
          <li>おば（父方）</li>
          <li>おば（母方）</li>
          <li>甥姪</li>
          <li>孫</li>
          <li>いとこ</li>
          <li>不明</li>
          <li>その他（父方）</li>
          <li>その他（母方）</li>
        </ul>
      </td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>血縁者の本研究参加の有無</strong></td>
      <td>case_participation_of_relatives_in_this_study</td>
      <td>string</td>
      <td>ラジオボタン        </td>
      <td>
        <ul>
          <li>not_applicable</li>
          <li>not_participated</li>
          <li>already_participated</li>
          <li>plan_to_participate</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>該当なし</li>
          <li>なし</li>
          <li>あり</li>
          <li>参加予定</li>
        </ul>
      </td>
      <td>not_applicable</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>性別</strong></td>
      <td>case_sex</td>
      <td>string</td>
      <td>ラジオボタン        </td>
      <td>
        <ul>
          <li>unknown</li>
          <li>male</li>
          <li>female</li>
          <li>other</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>男性</li>
          <li>女性</li>
          <li>その他</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>proband.subject.sex</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>性別 その他詳細</strong></td>
      <td>case_sex_details</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>発症の有無</strong></td>
      <td>case_presence_or_absence_of_onset</td>
      <td>string</td>
      <td>ラジオボタン        </td>
      <td>
        <ul>
          <li>unknown</li>
          <li>onset</li>
          <li>asymptomatic</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>発症</li>
          <li>未発症</li>
        </ul>
      </td>
      <td>unkown</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>pedigree.persons.affectedStatus</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>状態</strong></td>
      <td>case_life_status</td>
      <td>string</td>
      <td>ラジオボタン        </td>
      <td>
        <ul>
          <li>unknown</li>
          <li>alive</li>
          <li>deceased</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>不明</li>
          <li>生存</li>
          <li>故人</li>
        </ul>
      </td>
      <td>unkown</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>proband.subject.vitalStatus.status</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>生年月 (yyyy/mm)</strong></td>
      <td>case_birth</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>1800〜現在の年</li>
          <li>1~12</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>1800〜現在の年</li>
          <li>1~12</li>
        </ul>
      </td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>登録時年齢 (YMD)</strong></td>
      <td>case_age</td>
      <td>string</td>
      <td>テキストボックス (数字)、セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>診察時年齢 (YMD)</strong></td>
      <td>case_age_on_examination</td>
      <td>string</td>
      <td>テキストボックス (数字)、セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td>proband.subject.timeAtLastEncounter.age.iso8601duration</td>
      <td></td>
    </tr>
    <tr>
      <td><strong>没年月 (yyyy/mm)</strong></td>
      <td>case_death</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>死因</strong></td>
      <td>case_cause_of_death</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>concerned_disease</li>
          <li>other_disease</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>当該疾患</li>
          <li>当該疾患以外</li>
        </ul>
      </td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>当該疾患以外のときの死因詳細</strong></td>
      <td>case_cause_of_death_details</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>死因ICD-11コード</strong></td>
      <td>case_icd_11_code_of_cause_of_death</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>最終生存確認日 (yyyy/mm/dd)</strong></td>
      <td>case_last_date_of_confirmation_of_survival</td>
      <td>string</td>
      <td>日付選択インターフェース</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td>-</td>
      <td>-</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 民族・出生地（EN: `Etnicity`, KO: `민족・출신지`） {: #etnicity}

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
      <th colspan="3">一覧表示/操作</th>
      <th rowspan="2">Phenopackets</th>
      <th rowspan="2">備考</th>
    </tr>
    <tr>
      <th>値</th>
      <th>ラベル</th>
      <th>デフォルト表示</th>
      <th>編集可能</th>
      <th>列追加可能</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>民族 / 集団</strong></td>
      <td>case_ethnicity_group</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>アフガニスタン (AFG)</li>
          <li>アルバニア (ALB)</li>
          <li>アルジェリア (DZA)</li>
          <li>アメリカ領サモア (ASM)</li>
          <li>アンドラ (AND)</li>
          <li>アンゴラ (AGO)</li>
          <li>アンギラ (AIA)</li>
          <li>南極 (ATA)</li>
          <li>アンティグア・バーブーダ (ATG)</li>
          <li>アルゼンチン (ARG)</li>
          <li>アルメニア (ARM)</li>
          <li>アルバ (ABW)</li>
          <li>オーストラリア (AUS)</li>
          <li>オーストリア (AUT)</li>
          <li>アゼルバイジャン (AZE)</li>
          <li>バハマ (BHS)</li>
          <li>バーレーン (BHR)</li>
          <li>バングラデシュ (BGD)</li>
          <li>バルバドス (BRB)</li>
          <li>ベラルーシ (BLR)</li>
          <li>ベルギー (BEL)</li>
          <li>ベリーズ (BLZ)</li>
          <li>ベナン (BEN)</li>
          <li>バミューダ (BMU)</li>
          <li>ブータン (BTN)</li>
          <li>ボリビア多民族国 (BOL)</li>
          <li>ボネール、シント・ユースタティウスおよびサバ (BES)</li>
          <li>ボスニア・ヘルツェゴビナ (BIH)</li>
          <li>ボツワナ (BWA)</li>
          <li>ブーベ島 (BVT)</li>
          <li>ブラジル (BRA)</li>
          <li>イギリス領インド洋地域 (IOT)</li>
          <li>ブルネイ・ダルサラーム (BRN)</li>
          <li>ブルガリア (BGR)</li>
          <li>ブルキナファソ (BFA)</li>
          <li>ブルンジ (BDI)</li>
          <li>カンボジア (KHM)</li>
          <li>カメルーン (CMR)</li>
          <li>カナダ (CAN)</li>
          <li>カーボベルデ (CPV)</li>
          <li>ケイマン諸島 (CYM)</li>
          <li>中央アフリカ共和国 (CAF)</li>
          <li>チャド (TCD)</li>
          <li>チリ (CHL)</li>
          <li>中華人民共和国 (CHN)</li>
          <li>クリスマス島 (CXR)</li>
          <li>ココス(キーリング)諸島 (CCK)</li>
          <li>コロンビア (COL)</li>
          <li>コモロ (COM)</li>
          <li>コンゴ共和国 (COG)</li>
          <li>コンゴ民主共和国 (COD)</li>
          <li>クック諸島 (COK)</li>
          <li>コスタリカ (CRI)</li>
          <li>クロアチア (HRV)</li>
          <li>キューバ (CUB)</li>
          <li>キュラソー (CUW)</li>
          <li>キプロス (CYP)</li>
          <li>チェコ (CZE)</li>
          <li>コートジボワール (CIV)</li>
          <li>デンマーク (DNK)</li>
          <li>ジブチ (DJI)</li>
          <li>ドミニカ国 (DMA)</li>
          <li>ドミニカ共和国 (DOM)</li>
          <li>エクアドル (ECU)</li>
          <li>エジプト (EGY)</li>
          <li>エルサルバドル (SLV)</li>
          <li>赤道ギニア (GNQ)</li>
          <li>エリトリア (ERI)</li>
          <li>エストニア (EST)</li>
          <li>エチオピア (ETH)</li>
          <li>フォークランド(マルビナス)諸島 (FLK)</li>
          <li>フェロー諸島 (FRO)</li>
          <li>フィジー (FJI)</li>
          <li>フィンランド (FIN)</li>
          <li>フランス (FRA)</li>
          <li>フランス領ギアナ (GUF)</li>
          <li>フランス領ポリネシア (PYF)</li>
          <li>フランス領南方・南極地域 (ATF)</li>
          <li>ガボン (GAB)</li>
          <li>ガンビア (GMB)</li>
          <li>ジョージア (GEO)</li>
          <li>ドイツ (DEU)</li>
          <li>ガーナ (GHA)</li>
          <li>ジブラルタル (GIB)</li>
          <li>ギリシャ (GRC)</li>
          <li>グリーンランド (GRL)</li>
          <li>グレナダ (GRD)</li>
          <li>グアドループ (GLP)</li>
          <li>グアム (GUM)</li>
          <li>グアテマラ (GTM)</li>
          <li>ガーンジー (GGY)</li>
          <li>ギニア (GIN)</li>
          <li>ギニアビサウ (GNB)</li>
          <li>ガイアナ (GUY)</li>
          <li>ハイチ (HTI)</li>
          <li>ハード島とマクドナルド諸島 (HMD)</li>
          <li>バチカン市国 (VAT)</li>
          <li>ホンジュラス (HND)</li>
          <li>香港 (HKG)</li>
          <li>ハンガリー (HUN)</li>
          <li>アイスランド (ISL)</li>
          <li>インド (IND)</li>
          <li>インドネシア (IDN)</li>
          <li>イラン・イスラム共和国 (IRN)</li>
          <li>イラク (IRQ)</li>
          <li>アイルランド (IRL)</li>
          <li>マン島 (IMN)</li>
          <li>イスラエル (ISR)</li>
          <li>イタリア (ITA)</li>
          <li>ジャマイカ (JAM)</li>
          <li>日本 (JPN)</li>
          <li>ジャージー (JEY)</li>
          <li>ヨルダン (JOR)</li>
          <li>カザフスタン (KAZ)</li>
          <li>ケニア (KEN)</li>
          <li>キリバス (KIR)</li>
          <li>朝鮮民主主義人民共和国 (PRK)</li>
          <li>大韓民国 (KOR)</li>
          <li>クウェート (KWT)</li>
          <li>キルギス (KGZ)</li>
          <li>ラオス人民民主共和国 (LAO)</li>
          <li>ラトビア (LVA)</li>
          <li>レバノン (LBN)</li>
          <li>レソト (LSO)</li>
          <li>リベリア (LBR)</li>
          <li>リビア (LBY)</li>
          <li>リヒテンシュタイン (LIE)</li>
          <li>リトアニア (LTU)</li>
          <li>ルクセンブルク (LUX)</li>
          <li>マカオ (MAC)</li>
          <li>マケドニア旧ユーゴスラビア共和国 (MKD)</li>
          <li>マダガスカル (MDG)</li>
          <li>マラウイ (MWI)</li>
          <li>マレーシア (MYS)</li>
          <li>モルディブ (MDV)</li>
          <li>マリ (MLI)</li>
          <li>マルタ (MLT)</li>
          <li>マーシャル諸島 (MHL)</li>
          <li>マルティニーク (MTQ)</li>
          <li>モーリタニア (MRT)</li>
          <li>モーリシャス (MUS)</li>
          <li>マヨット (MYT)</li>
          <li>メキシコ (MEX)</li>
          <li>ミクロネシア連邦 (FSM)</li>
          <li>モルドバ共和国 (MDA)</li>
          <li>モナコ (MCO)</li>
          <li>モンゴル (MNG)</li>
          <li>モンテネグロ (MNE)</li>
          <li>モントセラト (MSR)</li>
          <li>モロッコ (MAR)</li>
          <li>モザンビーク (MOZ)</li>
          <li>ミャンマー (MMR)</li>
          <li>ナミビア (NAM)</li>
          <li>ナウル (NRU)</li>
          <li>ネパール (NPL)</li>
          <li>オランダ (NLD)</li>
          <li>ニューカレドニア (NCL)</li>
          <li>ニュージーランド (NZL)</li>
          <li>ニカラグア (NIC)</li>
          <li>ニジェール (NER)</li>
          <li>ナイジェリア (NGA)</li>
          <li>ニウエ (NIU)</li>
          <li>ノーフォーク島 (NFK)</li>
          <li>北マリアナ諸島 (MNP)</li>
          <li>ノルウェー (NOR)</li>
          <li>オマーン (OMN)</li>
          <li>パキスタン (PAK)</li>
          <li>パラオ (PLW)</li>
          <li>パレスチナ (PSE)</li>
          <li>パナマ (PAN)</li>
          <li>パプアニューギニア (PNG)</li>
          <li>パラグアイ (PRY)</li>
          <li>ペルー (PER)</li>
          <li>フィリピン (PHL)</li>
          <li>ピトケアン (PCN)</li>
          <li>ポーランド (POL)</li>
          <li>ポルトガル (PRT)</li>
          <li>プエルトリコ (PRI)</li>
          <li>カタール (QAT)</li>
          <li>ルーマニア (ROU)</li>
          <li>ロシア連邦 (RUS)</li>
          <li>ルワンダ (RWA)</li>
          <li>レユニオン (REU)</li>
          <li>サン・バルテルミー (BLM)</li>
          <li>セントヘレナ・アセンションおよびトリスタンダクーニャ (SHN)</li>
          <li>セントクリストファー・ネイビス (KNA)</li>
          <li>セントルシア (LCA)</li>
          <li>サン・マルタン(フランス領) (MAF)</li>
          <li>サンピエール島・ミクロン島 (SPM)</li>
          <li>セントビンセントおよびグレナディーン諸島 (VCT)</li>
          <li>サモア (WSM)</li>
          <li>サンマリノ (SMR)</li>
          <li>サントメ・プリンシペ (STP)</li>
          <li>サウジアラビア (SAU)</li>
          <li>セネガル (SEN)</li>
          <li>セルビア (SRB)</li>
          <li>セーシェル (SYC)</li>
          <li>シエラレオネ (SLE)</li>
          <li>シンガポール (SGP)</li>
          <li>シント・マールテン(オランダ領) (SXM)</li>
          <li>スロバキア (SVK)</li>
          <li>スロベニア (SVN)</li>
          <li>ソロモン諸島 (SLB)</li>
          <li>ソマリア (SOM)</li>
          <li>南アフリカ (ZAF)</li>
          <li>サウスジョージア・サウスサンドウィッチ諸島 (SGS)</li>
          <li>南スーダン (SSD)</li>
          <li>スペイン (ESP)</li>
          <li>スリランカ (LKA)</li>
          <li>スーダン (SDN)</li>
          <li>スリナム (SUR)</li>
          <li>スヴァールバル諸島およびヤンマイエン島 (SJM)</li>
          <li>スワジランド (SWZ)</li>
          <li>スウェーデン (SWE)</li>
          <li>スイス (CHE)</li>
          <li>シリア・アラブ共和国 (SYR)</li>
          <li>台湾 (TWN)</li>
          <li>タジキスタン (TJK)</li>
          <li>タンザニア (TZA)</li>
          <li>タイ (THA)</li>
          <li>東ティモール (TLS)</li>
          <li>トーゴ (TGO)</li>
          <li>トケラウ (TKL)</li>
          <li>トンガ (TON)</li>
          <li>トリニダード・トバゴ (TTO)</li>
          <li>チュニジア (TUN)</li>
          <li>トルコ (TUR)</li>
          <li>トルクメニスタン (TKM)</li>
          <li>タークス・カイコス諸島 (TCA)</li>
          <li>ツバル (TUV)</li>
          <li>ウガンダ (UGA)</li>
          <li>ウクライナ (UKR)</li>
          <li>アラブ首長国連邦 (ARE)</li>
          <li>イギリス (GBR)</li>
          <li>アメリカ合衆国 (USA)</li>
          <li>合衆国領有小離島 (UMI)</li>
          <li>ウルグアイ (URY)</li>
          <li>ウズベキスタン (UZB)</li>
          <li>バヌアツ (VUT)</li>
          <li>ベネズエラ・ボリバル共和国 (VEN)</li>
          <li>ベトナム (VNM)</li>
          <li>イギリス領ヴァージン諸島 (VGB)</li>
          <li>アメリカ領ヴァージン諸島 (VIR)</li>
          <li>ウォリス・フツナ (WLF)</li>
          <li>西サハラ (ESH)</li>
          <li>イエメン (YEM)</li>
          <li>ザンビア (ZMB)</li>
          <li>ジンバブエ (ZWE)</li>
          <li>オーランド諸島 (ALA)</li>
          <li>不明 (ZZZ)</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>アフガニスタン (AFG)</li>
          <li>アルバニア (ALB)</li>
          <li>アルジェリア (DZA)</li>
          <li>アメリカ領サモア (ASM)</li>
          <li>アンドラ (AND)</li>
          <li>アンゴラ (AGO)</li>
          <li>アンギラ (AIA)</li>
          <li>南極 (ATA)</li>
          <li>アンティグア・バーブーダ (ATG)</li>
          <li>アルゼンチン (ARG)</li>
          <li>アルメニア (ARM)</li>
          <li>アルバ (ABW)</li>
          <li>オーストラリア (AUS)</li>
          <li>オーストリア (AUT)</li>
          <li>アゼルバイジャン (AZE)</li>
          <li>バハマ (BHS)</li>
          <li>バーレーン (BHR)</li>
          <li>バングラデシュ (BGD)</li>
          <li>バルバドス (BRB)</li>
          <li>ベラルーシ (BLR)</li>
          <li>ベルギー (BEL)</li>
          <li>ベリーズ (BLZ)</li>
          <li>ベナン (BEN)</li>
          <li>バミューダ (BMU)</li>
          <li>ブータン (BTN)</li>
          <li>ボリビア多民族国 (BOL)</li>
          <li>ボネール、シント・ユースタティウスおよびサバ (BES)</li>
          <li>ボスニア・ヘルツェゴビナ (BIH)</li>
          <li>ボツワナ (BWA)</li>
          <li>ブーベ島 (BVT)</li>
          <li>ブラジル (BRA)</li>
          <li>イギリス領インド洋地域 (IOT)</li>
          <li>ブルネイ・ダルサラーム (BRN)</li>
          <li>ブルガリア (BGR)</li>
          <li>ブルキナファソ (BFA)</li>
          <li>ブルンジ (BDI)</li>
          <li>カンボジア (KHM)</li>
          <li>カメルーン (CMR)</li>
          <li>カナダ (CAN)</li>
          <li>カーボベルデ (CPV)</li>
          <li>ケイマン諸島 (CYM)</li>
          <li>中央アフリカ共和国 (CAF)</li>
          <li>チャド (TCD)</li>
          <li>チリ (CHL)</li>
          <li>中華人民共和国 (CHN)</li>
          <li>クリスマス島 (CXR)</li>
          <li>ココス(キーリング)諸島 (CCK)</li>
          <li>コロンビア (COL)</li>
          <li>コモロ (COM)</li>
          <li>コンゴ共和国 (COG)</li>
          <li>コンゴ民主共和国 (COD)</li>
          <li>クック諸島 (COK)</li>
          <li>コスタリカ (CRI)</li>
          <li>クロアチア (HRV)</li>
          <li>キューバ (CUB)</li>
          <li>キュラソー (CUW)</li>
          <li>キプロス (CYP)</li>
          <li>チェコ (CZE)</li>
          <li>コートジボワール (CIV)</li>
          <li>デンマーク (DNK)</li>
          <li>ジブチ (DJI)</li>
          <li>ドミニカ国 (DMA)</li>
          <li>ドミニカ共和国 (DOM)</li>
          <li>エクアドル (ECU)</li>
          <li>エジプト (EGY)</li>
          <li>エルサルバドル (SLV)</li>
          <li>赤道ギニア (GNQ)</li>
          <li>エリトリア (ERI)</li>
          <li>エストニア (EST)</li>
          <li>エチオピア (ETH)</li>
          <li>フォークランド(マルビナス)諸島 (FLK)</li>
          <li>フェロー諸島 (FRO)</li>
          <li>フィジー (FJI)</li>
          <li>フィンランド (FIN)</li>
          <li>フランス (FRA)</li>
          <li>フランス領ギアナ (GUF)</li>
          <li>フランス領ポリネシア (PYF)</li>
          <li>フランス領南方・南極地域 (ATF)</li>
          <li>ガボン (GAB)</li>
          <li>ガンビア (GMB)</li>
          <li>ジョージア (GEO)</li>
          <li>ドイツ (DEU)</li>
          <li>ガーナ (GHA)</li>
          <li>ジブラルタル (GIB)</li>
          <li>ギリシャ (GRC)</li>
          <li>グリーンランド (GRL)</li>
          <li>グレナダ (GRD)</li>
          <li>グアドループ (GLP)</li>
          <li>グアム (GUM)</li>
          <li>グアテマラ (GTM)</li>
          <li>ガーンジー (GGY)</li>
          <li>ギニア (GIN)</li>
          <li>ギニアビサウ (GNB)</li>
          <li>ガイアナ (GUY)</li>
          <li>ハイチ (HTI)</li>
          <li>ハード島とマクドナルド諸島 (HMD)</li>
          <li>バチカン市国 (VAT)</li>
          <li>ホンジュラス (HND)</li>
          <li>香港 (HKG)</li>
          <li>ハンガリー (HUN)</li>
          <li>アイスランド (ISL)</li>
          <li>インド (IND)</li>
          <li>インドネシア (IDN)</li>
          <li>イラン・イスラム共和国 (IRN)</li>
          <li>イラク (IRQ)</li>
          <li>アイルランド (IRL)</li>
          <li>マン島 (IMN)</li>
          <li>イスラエル (ISR)</li>
          <li>イタリア (ITA)</li>
          <li>ジャマイカ (JAM)</li>
          <li>日本 (JPN)</li>
          <li>ジャージー (JEY)</li>
          <li>ヨルダン (JOR)</li>
          <li>カザフスタン (KAZ)</li>
          <li>ケニア (KEN)</li>
          <li>キリバス (KIR)</li>
          <li>朝鮮民主主義人民共和国 (PRK)</li>
          <li>大韓民国 (KOR)</li>
          <li>クウェート (KWT)</li>
          <li>キルギス (KGZ)</li>
          <li>ラオス人民民主共和国 (LAO)</li>
          <li>ラトビア (LVA)</li>
          <li>レバノン (LBN)</li>
          <li>レソト (LSO)</li>
          <li>リベリア (LBR)</li>
          <li>リビア (LBY)</li>
          <li>リヒテンシュタイン (LIE)</li>
          <li>リトアニア (LTU)</li>
          <li>ルクセンブルク (LUX)</li>
          <li>マカオ (MAC)</li>
          <li>マケドニア旧ユーゴスラビア共和国 (MKD)</li>
          <li>マダガスカル (MDG)</li>
          <li>マラウイ (MWI)</li>
          <li>マレーシア (MYS)</li>
          <li>モルディブ (MDV)</li>
          <li>マリ (MLI)</li>
          <li>マルタ (MLT)</li>
          <li>マーシャル諸島 (MHL)</li>
          <li>マルティニーク (MTQ)</li>
          <li>モーリタニア (MRT)</li>
          <li>モーリシャス (MUS)</li>
          <li>マヨット (MYT)</li>
          <li>メキシコ (MEX)</li>
          <li>ミクロネシア連邦 (FSM)</li>
          <li>モルドバ共和国 (MDA)</li>
          <li>モナコ (MCO)</li>
          <li>モンゴル (MNG)</li>
          <li>モンテネグロ (MNE)</li>
          <li>モントセラト (MSR)</li>
          <li>モロッコ (MAR)</li>
          <li>モザンビーク (MOZ)</li>
          <li>ミャンマー (MMR)</li>
          <li>ナミビア (NAM)</li>
          <li>ナウル (NRU)</li>
          <li>ネパール (NPL)</li>
          <li>オランダ (NLD)</li>
          <li>ニューカレドニア (NCL)</li>
          <li>ニュージーランド (NZL)</li>
          <li>ニカラグア (NIC)</li>
          <li>ニジェール (NER)</li>
          <li>ナイジェリア (NGA)</li>
          <li>ニウエ (NIU)</li>
          <li>ノーフォーク島 (NFK)</li>
          <li>北マリアナ諸島 (MNP)</li>
          <li>ノルウェー (NOR)</li>
          <li>オマーン (OMN)</li>
          <li>パキスタン (PAK)</li>
          <li>パラオ (PLW)</li>
          <li>パレスチナ (PSE)</li>
          <li>パナマ (PAN)</li>
          <li>パプアニューギニア (PNG)</li>
          <li>パラグアイ (PRY)</li>
          <li>ペルー (PER)</li>
          <li>フィリピン (PHL)</li>
          <li>ピトケアン (PCN)</li>
          <li>ポーランド (POL)</li>
          <li>ポルトガル (PRT)</li>
          <li>プエルトリコ (PRI)</li>
          <li>カタール (QAT)</li>
          <li>ルーマニア (ROU)</li>
          <li>ロシア連邦 (RUS)</li>
          <li>ルワンダ (RWA)</li>
          <li>レユニオン (REU)</li>
          <li>サン・バルテルミー (BLM)</li>
          <li>セントヘレナ・アセンションおよびトリスタンダクーニャ (SHN)</li>
          <li>セントクリストファー・ネイビス (KNA)</li>
          <li>セントルシア (LCA)</li>
          <li>サン・マルタン(フランス領) (MAF)</li>
          <li>サンピエール島・ミクロン島 (SPM)</li>
          <li>セントビンセントおよびグレナディーン諸島 (VCT)</li>
          <li>サモア (WSM)</li>
          <li>サンマリノ (SMR)</li>
          <li>サントメ・プリンシペ (STP)</li>
          <li>サウジアラビア (SAU)</li>
          <li>セネガル (SEN)</li>
          <li>セルビア (SRB)</li>
          <li>セーシェル (SYC)</li>
          <li>シエラレオネ (SLE)</li>
          <li>シンガポール (SGP)</li>
          <li>シント・マールテン(オランダ領) (SXM)</li>
          <li>スロバキア (SVK)</li>
          <li>スロベニア (SVN)</li>
          <li>ソロモン諸島 (SLB)</li>
          <li>ソマリア (SOM)</li>
          <li>南アフリカ (ZAF)</li>
          <li>サウスジョージア・サウスサンドウィッチ諸島 (SGS)</li>
          <li>南スーダン (SSD)</li>
          <li>スペイン (ESP)</li>
          <li>スリランカ (LKA)</li>
          <li>スーダン (SDN)</li>
          <li>スリナム (SUR)</li>
          <li>スヴァールバル諸島およびヤンマイエン島 (SJM)</li>
          <li>スワジランド (SWZ)</li>
          <li>スウェーデン (SWE)</li>
          <li>スイス (CHE)</li>
          <li>シリア・アラブ共和国 (SYR)</li>
          <li>台湾 (TWN)</li>
          <li>タジキスタン (TJK)</li>
          <li>タンザニア (TZA)</li>
          <li>タイ (THA)</li>
          <li>東ティモール (TLS)</li>
          <li>トーゴ (TGO)</li>
          <li>トケラウ (TKL)</li>
          <li>トンガ (TON)</li>
          <li>トリニダード・トバゴ (TTO)</li>
          <li>チュニジア (TUN)</li>
          <li>トルコ (TUR)</li>
          <li>トルクメニスタン (TKM)</li>
          <li>タークス・カイコス諸島 (TCA)</li>
          <li>ツバル (TUV)</li>
          <li>ウガンダ (UGA)</li>
          <li>ウクライナ (UKR)</li>
          <li>アラブ首長国連邦 (ARE)</li>
          <li>イギリス (GBR)</li>
          <li>アメリカ合衆国 (USA)</li>
          <li>合衆国領有小離島 (UMI)</li>
          <li>ウルグアイ (URY)</li>
          <li>ウズベキスタン (UZB)</li>
          <li>バヌアツ (VUT)</li>
          <li>ベネズエラ・ボリバル共和国 (VEN)</li>
          <li>ベトナム (VNM)</li>
          <li>イギリス領ヴァージン諸島 (VGB)</li>
          <li>アメリカ領ヴァージン諸島 (VIR)</li>
          <li>ウォリス・フツナ (WLF)</li>
          <li>西サハラ (ESH)</li>
          <li>イエメン (YEM)</li>
          <li>ザンビア (ZMB)</li>
          <li>ジンバブエ (ZWE)</li>
          <li>オーランド諸島 (ALA)</li>
          <li>不明 (ZZZ)</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>自由記載</strong></td>
      <td>case_free_comment_about_ethnicity_group</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>出生地 国</strong></td>
      <td>case_country_of_birth</td>
      <td>string</td>
      <td>セレクトボックス</td>
      <td>
        <ul>
          <li>アフガニスタン (AFG)</li>
          <li>アルバニア (ALB)</li>
          <li>アルジェリア (DZA)</li>
          <li>アメリカ領サモア (ASM)</li>
          <li>アンドラ (AND)</li>
          <li>アンゴラ (AGO)</li>
          <li>アンギラ (AIA)</li>
          <li>南極 (ATA)</li>
          <li>アンティグア・バーブーダ (ATG)</li>
          <li>アルゼンチン (ARG)</li>
          <li>アルメニア (ARM)</li>
          <li>アルバ (ABW)</li>
          <li>オーストラリア (AUS)</li>
          <li>オーストリア (AUT)</li>
          <li>アゼルバイジャン (AZE)</li>
          <li>バハマ (BHS)</li>
          <li>バーレーン (BHR)</li>
          <li>バングラデシュ (BGD)</li>
          <li>バルバドス (BRB)</li>
          <li>ベラルーシ (BLR)</li>
          <li>ベルギー (BEL)</li>
          <li>ベリーズ (BLZ)</li>
          <li>ベナン (BEN)</li>
          <li>バミューダ (BMU)</li>
          <li>ブータン (BTN)</li>
          <li>ボリビア多民族国 (BOL)</li>
          <li>ボネール、シント・ユースタティウスおよびサバ (BES)</li>
          <li>ボスニア・ヘルツェゴビナ (BIH)</li>
          <li>ボツワナ (BWA)</li>
          <li>ブーベ島 (BVT)</li>
          <li>ブラジル (BRA)</li>
          <li>イギリス領インド洋地域 (IOT)</li>
          <li>ブルネイ・ダルサラーム (BRN)</li>
          <li>ブルガリア (BGR)</li>
          <li>ブルキナファソ (BFA)</li>
          <li>ブルンジ (BDI)</li>
          <li>カンボジア (KHM)</li>
          <li>カメルーン (CMR)</li>
          <li>カナダ (CAN)</li>
          <li>カーボベルデ (CPV)</li>
          <li>ケイマン諸島 (CYM)</li>
          <li>中央アフリカ共和国 (CAF)</li>
          <li>チャド (TCD)</li>
          <li>チリ (CHL)</li>
          <li>中華人民共和国 (CHN)</li>
          <li>クリスマス島 (CXR)</li>
          <li>ココス(キーリング)諸島 (CCK)</li>
          <li>コロンビア (COL)</li>
          <li>コモロ (COM)</li>
          <li>コンゴ共和国 (COG)</li>
          <li>コンゴ民主共和国 (COD)</li>
          <li>クック諸島 (COK)</li>
          <li>コスタリカ (CRI)</li>
          <li>クロアチア (HRV)</li>
          <li>キューバ (CUB)</li>
          <li>キュラソー (CUW)</li>
          <li>キプロス (CYP)</li>
          <li>チェコ (CZE)</li>
          <li>コートジボワール (CIV)</li>
          <li>デンマーク (DNK)</li>
          <li>ジブチ (DJI)</li>
          <li>ドミニカ国 (DMA)</li>
          <li>ドミニカ共和国 (DOM)</li>
          <li>エクアドル (ECU)</li>
          <li>エジプト (EGY)</li>
          <li>エルサルバドル (SLV)</li>
          <li>赤道ギニア (GNQ)</li>
          <li>エリトリア (ERI)</li>
          <li>エストニア (EST)</li>
          <li>エチオピア (ETH)</li>
          <li>フォークランド(マルビナス)諸島 (FLK)</li>
          <li>フェロー諸島 (FRO)</li>
          <li>フィジー (FJI)</li>
          <li>フィンランド (FIN)</li>
          <li>フランス (FRA)</li>
          <li>フランス領ギアナ (GUF)</li>
          <li>フランス領ポリネシア (PYF)</li>
          <li>フランス領南方・南極地域 (ATF)</li>
          <li>ガボン (GAB)</li>
          <li>ガンビア (GMB)</li>
          <li>ジョージア (GEO)</li>
          <li>ドイツ (DEU)</li>
          <li>ガーナ (GHA)</li>
          <li>ジブラルタル (GIB)</li>
          <li>ギリシャ (GRC)</li>
          <li>グリーンランド (GRL)</li>
          <li>グレナダ (GRD)</li>
          <li>グアドループ (GLP)</li>
          <li>グアム (GUM)</li>
          <li>グアテマラ (GTM)</li>
          <li>ガーンジー (GGY)</li>
          <li>ギニア (GIN)</li>
          <li>ギニアビサウ (GNB)</li>
          <li>ガイアナ (GUY)</li>
          <li>ハイチ (HTI)</li>
          <li>ハード島とマクドナルド諸島 (HMD)</li>
          <li>バチカン市国 (VAT)</li>
          <li>ホンジュラス (HND)</li>
          <li>香港 (HKG)</li>
          <li>ハンガリー (HUN)</li>
          <li>アイスランド (ISL)</li>
          <li>インド (IND)</li>
          <li>インドネシア (IDN)</li>
          <li>イラン・イスラム共和国 (IRN)</li>
          <li>イラク (IRQ)</li>
          <li>アイルランド (IRL)</li>
          <li>マン島 (IMN)</li>
          <li>イスラエル (ISR)</li>
          <li>イタリア (ITA)</li>
          <li>ジャマイカ (JAM)</li>
          <li>日本 (JPN)</li>
          <li>ジャージー (JEY)</li>
          <li>ヨルダン (JOR)</li>
          <li>カザフスタン (KAZ)</li>
          <li>ケニア (KEN)</li>
          <li>キリバス (KIR)</li>
          <li>朝鮮民主主義人民共和国 (PRK)</li>
          <li>大韓民国 (KOR)</li>
          <li>クウェート (KWT)</li>
          <li>キルギス (KGZ)</li>
          <li>ラオス人民民主共和国 (LAO)</li>
          <li>ラトビア (LVA)</li>
          <li>レバノン (LBN)</li>
          <li>レソト (LSO)</li>
          <li>リベリア (LBR)</li>
          <li>リビア (LBY)</li>
          <li>リヒテンシュタイン (LIE)</li>
          <li>リトアニア (LTU)</li>
          <li>ルクセンブルク (LUX)</li>
          <li>マカオ (MAC)</li>
          <li>マケドニア旧ユーゴスラビア共和国 (MKD)</li>
          <li>マダガスカル (MDG)</li>
          <li>マラウイ (MWI)</li>
          <li>マレーシア (MYS)</li>
          <li>モルディブ (MDV)</li>
          <li>マリ (MLI)</li>
          <li>マルタ (MLT)</li>
          <li>マーシャル諸島 (MHL)</li>
          <li>マルティニーク (MTQ)</li>
          <li>モーリタニア (MRT)</li>
          <li>モーリシャス (MUS)</li>
          <li>マヨット (MYT)</li>
          <li>メキシコ (MEX)</li>
          <li>ミクロネシア連邦 (FSM)</li>
          <li>モルドバ共和国 (MDA)</li>
          <li>モナコ (MCO)</li>
          <li>モンゴル (MNG)</li>
          <li>モンテネグロ (MNE)</li>
          <li>モントセラト (MSR)</li>
          <li>モロッコ (MAR)</li>
          <li>モザンビーク (MOZ)</li>
          <li>ミャンマー (MMR)</li>
          <li>ナミビア (NAM)</li>
          <li>ナウル (NRU)</li>
          <li>ネパール (NPL)</li>
          <li>オランダ (NLD)</li>
          <li>ニューカレドニア (NCL)</li>
          <li>ニュージーランド (NZL)</li>
          <li>ニカラグア (NIC)</li>
          <li>ニジェール (NER)</li>
          <li>ナイジェリア (NGA)</li>
          <li>ニウエ (NIU)</li>
          <li>ノーフォーク島 (NFK)</li>
          <li>北マリアナ諸島 (MNP)</li>
          <li>ノルウェー (NOR)</li>
          <li>オマーン (OMN)</li>
          <li>パキスタン (PAK)</li>
          <li>パラオ (PLW)</li>
          <li>パレスチナ (PSE)</li>
          <li>パナマ (PAN)</li>
          <li>パプアニューギニア (PNG)</li>
          <li>パラグアイ (PRY)</li>
          <li>ペルー (PER)</li>
          <li>フィリピン (PHL)</li>
          <li>ピトケアン (PCN)</li>
          <li>ポーランド (POL)</li>
          <li>ポルトガル (PRT)</li>
          <li>プエルトリコ (PRI)</li>
          <li>カタール (QAT)</li>
          <li>ルーマニア (ROU)</li>
          <li>ロシア連邦 (RUS)</li>
          <li>ルワンダ (RWA)</li>
          <li>レユニオン (REU)</li>
          <li>サン・バルテルミー (BLM)</li>
          <li>セントヘレナ・アセンションおよびトリスタンダクーニャ (SHN)</li>
          <li>セントクリストファー・ネイビス (KNA)</li>
          <li>セントルシア (LCA)</li>
          <li>サン・マルタン(フランス領) (MAF)</li>
          <li>サンピエール島・ミクロン島 (SPM)</li>
          <li>セントビンセントおよびグレナディーン諸島 (VCT)</li>
          <li>サモア (WSM)</li>
          <li>サンマリノ (SMR)</li>
          <li>サントメ・プリンシペ (STP)</li>
          <li>サウジアラビア (SAU)</li>
          <li>セネガル (SEN)</li>
          <li>セルビア (SRB)</li>
          <li>セーシェル (SYC)</li>
          <li>シエラレオネ (SLE)</li>
          <li>シンガポール (SGP)</li>
          <li>シント・マールテン(オランダ領) (SXM)</li>
          <li>スロバキア (SVK)</li>
          <li>スロベニア (SVN)</li>
          <li>ソロモン諸島 (SLB)</li>
          <li>ソマリア (SOM)</li>
          <li>南アフリカ (ZAF)</li>
          <li>サウスジョージア・サウスサンドウィッチ諸島 (SGS)</li>
          <li>南スーダン (SSD)</li>
          <li>スペイン (ESP)</li>
          <li>スリランカ (LKA)</li>
          <li>スーダン (SDN)</li>
          <li>スリナム (SUR)</li>
          <li>スヴァールバル諸島およびヤンマイエン島 (SJM)</li>
          <li>スワジランド (SWZ)</li>
          <li>スウェーデン (SWE)</li>
          <li>スイス (CHE)</li>
          <li>シリア・アラブ共和国 (SYR)</li>
          <li>台湾 (TWN)</li>
          <li>タジキスタン (TJK)</li>
          <li>タンザニア (TZA)</li>
          <li>タイ (THA)</li>
          <li>東ティモール (TLS)</li>
          <li>トーゴ (TGO)</li>
          <li>トケラウ (TKL)</li>
          <li>トンガ (TON)</li>
          <li>トリニダード・トバゴ (TTO)</li>
          <li>チュニジア (TUN)</li>
          <li>トルコ (TUR)</li>
          <li>トルクメニスタン (TKM)</li>
          <li>タークス・カイコス諸島 (TCA)</li>
          <li>ツバル (TUV)</li>
          <li>ウガンダ (UGA)</li>
          <li>ウクライナ (UKR)</li>
          <li>アラブ首長国連邦 (ARE)</li>
          <li>イギリス (GBR)</li>
          <li>アメリカ合衆国 (USA)</li>
          <li>合衆国領有小離島 (UMI)</li>
          <li>ウルグアイ (URY)</li>
          <li>ウズベキスタン (UZB)</li>
          <li>バヌアツ (VUT)</li>
          <li>ベネズエラ・ボリバル共和国 (VEN)</li>
          <li>ベトナム (VNM)</li>
          <li>イギリス領ヴァージン諸島 (VGB)</li>
          <li>アメリカ領ヴァージン諸島 (VIR)</li>
          <li>ウォリス・フツナ (WLF)</li>
          <li>西サハラ (ESH)</li>
          <li>イエメン (YEM)</li>
          <li>ザンビア (ZMB)</li>
          <li>ジンバブエ (ZWE)</li>
          <li>オーランド諸島 (ALA)</li>
          <li>不明 (ZZZ)</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>アフガニスタン (AFG)</li>
          <li>アルバニア (ALB)</li>
          <li>アルジェリア (DZA)</li>
          <li>アメリカ領サモア (ASM)</li>
          <li>アンドラ (AND)</li>
          <li>アンゴラ (AGO)</li>
          <li>アンギラ (AIA)</li>
          <li>南極 (ATA)</li>
          <li>アンティグア・バーブーダ (ATG)</li>
          <li>アルゼンチン (ARG)</li>
          <li>アルメニア (ARM)</li>
          <li>アルバ (ABW)</li>
          <li>オーストラリア (AUS)</li>
          <li>オーストリア (AUT)</li>
          <li>アゼルバイジャン (AZE)</li>
          <li>バハマ (BHS)</li>
          <li>バーレーン (BHR)</li>
          <li>バングラデシュ (BGD)</li>
          <li>バルバドス (BRB)</li>
          <li>ベラルーシ (BLR)</li>
          <li>ベルギー (BEL)</li>
          <li>ベリーズ (BLZ)</li>
          <li>ベナン (BEN)</li>
          <li>バミューダ (BMU)</li>
          <li>ブータン (BTN)</li>
          <li>ボリビア多民族国 (BOL)</li>
          <li>ボネール、シント・ユースタティウスおよびサバ (BES)</li>
          <li>ボスニア・ヘルツェゴビナ (BIH)</li>
          <li>ボツワナ (BWA)</li>
          <li>ブーベ島 (BVT)</li>
          <li>ブラジル (BRA)</li>
          <li>イギリス領インド洋地域 (IOT)</li>
          <li>ブルネイ・ダルサラーム (BRN)</li>
          <li>ブルガリア (BGR)</li>
          <li>ブルキナファソ (BFA)</li>
          <li>ブルンジ (BDI)</li>
          <li>カンボジア (KHM)</li>
          <li>カメルーン (CMR)</li>
          <li>カナダ (CAN)</li>
          <li>カーボベルデ (CPV)</li>
          <li>ケイマン諸島 (CYM)</li>
          <li>中央アフリカ共和国 (CAF)</li>
          <li>チャド (TCD)</li>
          <li>チリ (CHL)</li>
          <li>中華人民共和国 (CHN)</li>
          <li>クリスマス島 (CXR)</li>
          <li>ココス(キーリング)諸島 (CCK)</li>
          <li>コロンビア (COL)</li>
          <li>コモロ (COM)</li>
          <li>コンゴ共和国 (COG)</li>
          <li>コンゴ民主共和国 (COD)</li>
          <li>クック諸島 (COK)</li>
          <li>コスタリカ (CRI)</li>
          <li>クロアチア (HRV)</li>
          <li>キューバ (CUB)</li>
          <li>キュラソー (CUW)</li>
          <li>キプロス (CYP)</li>
          <li>チェコ (CZE)</li>
          <li>コートジボワール (CIV)</li>
          <li>デンマーク (DNK)</li>
          <li>ジブチ (DJI)</li>
          <li>ドミニカ国 (DMA)</li>
          <li>ドミニカ共和国 (DOM)</li>
          <li>エクアドル (ECU)</li>
          <li>エジプト (EGY)</li>
          <li>エルサルバドル (SLV)</li>
          <li>赤道ギニア (GNQ)</li>
          <li>エリトリア (ERI)</li>
          <li>エストニア (EST)</li>
          <li>エチオピア (ETH)</li>
          <li>フォークランド(マルビナス)諸島 (FLK)</li>
          <li>フェロー諸島 (FRO)</li>
          <li>フィジー (FJI)</li>
          <li>フィンランド (FIN)</li>
          <li>フランス (FRA)</li>
          <li>フランス領ギアナ (GUF)</li>
          <li>フランス領ポリネシア (PYF)</li>
          <li>フランス領南方・南極地域 (ATF)</li>
          <li>ガボン (GAB)</li>
          <li>ガンビア (GMB)</li>
          <li>ジョージア (GEO)</li>
          <li>ドイツ (DEU)</li>
          <li>ガーナ (GHA)</li>
          <li>ジブラルタル (GIB)</li>
          <li>ギリシャ (GRC)</li>
          <li>グリーンランド (GRL)</li>
          <li>グレナダ (GRD)</li>
          <li>グアドループ (GLP)</li>
          <li>グアム (GUM)</li>
          <li>グアテマラ (GTM)</li>
          <li>ガーンジー (GGY)</li>
          <li>ギニア (GIN)</li>
          <li>ギニアビサウ (GNB)</li>
          <li>ガイアナ (GUY)</li>
          <li>ハイチ (HTI)</li>
          <li>ハード島とマクドナルド諸島 (HMD)</li>
          <li>バチカン市国 (VAT)</li>
          <li>ホンジュラス (HND)</li>
          <li>香港 (HKG)</li>
          <li>ハンガリー (HUN)</li>
          <li>アイスランド (ISL)</li>
          <li>インド (IND)</li>
          <li>インドネシア (IDN)</li>
          <li>イラン・イスラム共和国 (IRN)</li>
          <li>イラク (IRQ)</li>
          <li>アイルランド (IRL)</li>
          <li>マン島 (IMN)</li>
          <li>イスラエル (ISR)</li>
          <li>イタリア (ITA)</li>
          <li>ジャマイカ (JAM)</li>
          <li>日本 (JPN)</li>
          <li>ジャージー (JEY)</li>
          <li>ヨルダン (JOR)</li>
          <li>カザフスタン (KAZ)</li>
          <li>ケニア (KEN)</li>
          <li>キリバス (KIR)</li>
          <li>朝鮮民主主義人民共和国 (PRK)</li>
          <li>大韓民国 (KOR)</li>
          <li>クウェート (KWT)</li>
          <li>キルギス (KGZ)</li>
          <li>ラオス人民民主共和国 (LAO)</li>
          <li>ラトビア (LVA)</li>
          <li>レバノン (LBN)</li>
          <li>レソト (LSO)</li>
          <li>リベリア (LBR)</li>
          <li>リビア (LBY)</li>
          <li>リヒテンシュタイン (LIE)</li>
          <li>リトアニア (LTU)</li>
          <li>ルクセンブルク (LUX)</li>
          <li>マカオ (MAC)</li>
          <li>マケドニア旧ユーゴスラビア共和国 (MKD)</li>
          <li>マダガスカル (MDG)</li>
          <li>マラウイ (MWI)</li>
          <li>マレーシア (MYS)</li>
          <li>モルディブ (MDV)</li>
          <li>マリ (MLI)</li>
          <li>マルタ (MLT)</li>
          <li>マーシャル諸島 (MHL)</li>
          <li>マルティニーク (MTQ)</li>
          <li>モーリタニア (MRT)</li>
          <li>モーリシャス (MUS)</li>
          <li>マヨット (MYT)</li>
          <li>メキシコ (MEX)</li>
          <li>ミクロネシア連邦 (FSM)</li>
          <li>モルドバ共和国 (MDA)</li>
          <li>モナコ (MCO)</li>
          <li>モンゴル (MNG)</li>
          <li>モンテネグロ (MNE)</li>
          <li>モントセラト (MSR)</li>
          <li>モロッコ (MAR)</li>
          <li>モザンビーク (MOZ)</li>
          <li>ミャンマー (MMR)</li>
          <li>ナミビア (NAM)</li>
          <li>ナウル (NRU)</li>
          <li>ネパール (NPL)</li>
          <li>オランダ (NLD)</li>
          <li>ニューカレドニア (NCL)</li>
          <li>ニュージーランド (NZL)</li>
          <li>ニカラグア (NIC)</li>
          <li>ニジェール (NER)</li>
          <li>ナイジェリア (NGA)</li>
          <li>ニウエ (NIU)</li>
          <li>ノーフォーク島 (NFK)</li>
          <li>北マリアナ諸島 (MNP)</li>
          <li>ノルウェー (NOR)</li>
          <li>オマーン (OMN)</li>
          <li>パキスタン (PAK)</li>
          <li>パラオ (PLW)</li>
          <li>パレスチナ (PSE)</li>
          <li>パナマ (PAN)</li>
          <li>パプアニューギニア (PNG)</li>
          <li>パラグアイ (PRY)</li>
          <li>ペルー (PER)</li>
          <li>フィリピン (PHL)</li>
          <li>ピトケアン (PCN)</li>
          <li>ポーランド (POL)</li>
          <li>ポルトガル (PRT)</li>
          <li>プエルトリコ (PRI)</li>
          <li>カタール (QAT)</li>
          <li>ルーマニア (ROU)</li>
          <li>ロシア連邦 (RUS)</li>
          <li>ルワンダ (RWA)</li>
          <li>レユニオン (REU)</li>
          <li>サン・バルテルミー (BLM)</li>
          <li>セントヘレナ・アセンションおよびトリスタンダクーニャ (SHN)</li>
          <li>セントクリストファー・ネイビス (KNA)</li>
          <li>セントルシア (LCA)</li>
          <li>サン・マルタン(フランス領) (MAF)</li>
          <li>サンピエール島・ミクロン島 (SPM)</li>
          <li>セントビンセントおよびグレナディーン諸島 (VCT)</li>
          <li>サモア (WSM)</li>
          <li>サンマリノ (SMR)</li>
          <li>サントメ・プリンシペ (STP)</li>
          <li>サウジアラビア (SAU)</li>
          <li>セネガル (SEN)</li>
          <li>セルビア (SRB)</li>
          <li>セーシェル (SYC)</li>
          <li>シエラレオネ (SLE)</li>
          <li>シンガポール (SGP)</li>
          <li>シント・マールテン(オランダ領) (SXM)</li>
          <li>スロバキア (SVK)</li>
          <li>スロベニア (SVN)</li>
          <li>ソロモン諸島 (SLB)</li>
          <li>ソマリア (SOM)</li>
          <li>南アフリカ (ZAF)</li>
          <li>サウスジョージア・サウスサンドウィッチ諸島 (SGS)</li>
          <li>南スーダン (SSD)</li>
          <li>スペイン (ESP)</li>
          <li>スリランカ (LKA)</li>
          <li>スーダン (SDN)</li>
          <li>スリナム (SUR)</li>
          <li>スヴァールバル諸島およびヤンマイエン島 (SJM)</li>
          <li>スワジランド (SWZ)</li>
          <li>スウェーデン (SWE)</li>
          <li>スイス (CHE)</li>
          <li>シリア・アラブ共和国 (SYR)</li>
          <li>台湾 (TWN)</li>
          <li>タジキスタン (TJK)</li>
          <li>タンザニア (TZA)</li>
          <li>タイ (THA)</li>
          <li>東ティモール (TLS)</li>
          <li>トーゴ (TGO)</li>
          <li>トケラウ (TKL)</li>
          <li>トンガ (TON)</li>
          <li>トリニダード・トバゴ (TTO)</li>
          <li>チュニジア (TUN)</li>
          <li>トルコ (TUR)</li>
          <li>トルクメニスタン (TKM)</li>
          <li>タークス・カイコス諸島 (TCA)</li>
          <li>ツバル (TUV)</li>
          <li>ウガンダ (UGA)</li>
          <li>ウクライナ (UKR)</li>
          <li>アラブ首長国連邦 (ARE)</li>
          <li>イギリス (GBR)</li>
          <li>アメリカ合衆国 (USA)</li>
          <li>合衆国領有小離島 (UMI)</li>
          <li>ウルグアイ (URY)</li>
          <li>ウズベキスタン (UZB)</li>
          <li>バヌアツ (VUT)</li>
          <li>ベネズエラ・ボリバル共和国 (VEN)</li>
          <li>ベトナム (VNM)</li>
          <li>イギリス領ヴァージン諸島 (VGB)</li>
          <li>アメリカ領ヴァージン諸島 (VIR)</li>
          <li>ウォリス・フツナ (WLF)</li>
          <li>西サハラ (ESH)</li>
          <li>イエメン (YEM)</li>
          <li>ザンビア (ZMB)</li>
          <li>ジンバブエ (ZWE)</li>
          <li>オーランド諸島 (ALA)</li>
          <li>不明 (ZZZ)</li>
        </ul>
      </td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>都道府県</strong></td>
      <td>case_state_of_birth</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>市区町村</strong></td>
      <td>case_city_of_birth</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>自由記載</strong></td>
      <td>case_free_comment_about_birth</td>
      <td>string</td>
      <td>テキストボックス</td>
      <td>-</td>
      <td>-</td>
      <td>null</td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td><input type="checkbox" class="readonly-input" checked /></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 出生時（EN: `Birth Info`, KO: `출생 정보`） {: #birth-info}
## 生殖補助（EN: `Assisted Reproduction`, KO: `보조 생식`） {: #assisted-reproduction}
## 入力者情報（EN: `Inputter Info`, KO: `입력자 정보`） {: #inputter-info}
