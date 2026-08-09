# Luna GitHub Pages 公開用パッケージ

このZIPを展開し、**中身をそのまま GitHub リポジトリのルートへ置いてください。**

## 必要ファイル
- index.html
- config.js
- images/products/（商品画像）
- images/about/S__146366466.jpg
- Luna-product-management.xlsx
- PRODUCT-MAPPING.csv
- README.md

## 正しい商品・画像対応
- luna001 / Snow Drop / S__146358279.jpg
- luna002 / Lumière / S__146358283.jpg
- luna003 / Sage Moon / S__146358278.jpg
- luna004 / Dalmata / S__146358284.jpg
- luna005 / Silver Tide / S__146358289.jpg
- luna006 / Veil Heart / S__146358287.jpg
- luna007 / Nocturne / S__146358277.jpg
- luna008 / Arc Pearl / STYLE 01: S__146358281.jpg / STYLE 02: S__146358280.jpg
- luna010 / Étoile Bow / S__146358288.jpg
- luna009 / Petit Heart / S__146358276.jpg / BRACELET / ¥2,200

Petit Heart はブレスレットで、表示順10＝最後です。

## 最初にGoogleスプレッドシートを合わせる
サイトはGoogleスプレッドシート「商品管理」を唯一の商品データ元として読み込みます。
今回の `Luna-product-management.xlsx` の「商品管理」シートと、現在のGoogleスプレッドシートの内容を同じにしてください。
特に「商品ID」「商品名」「カテゴリー」「メイン画像」「2way画像」を完全一致させてください。

## GitHub Pages
1. Luna-site リポジトリを開く
2. このパッケージの中身をリポジトリ直下へアップロード
3. Settings → Pages
4. Deploy from a branch
5. main / /(root)
6. Save
7. 数分後に公開URLを開く

画像は必ず `images/products/` に置きます。
「新しいフォルダー」など別の場所は使いません。

## Googleスプレッドシート接続
`config.js` には現在の公開CSV URLを設定済みです。

### 価格変更
「価格」セルの数字を変更。

### SOLD OUT
「販売状態」を AVAILABLE → SOLD OUT。
写真と詳細は残り、注文導線が停止します。

### AVAILABLEへ戻す
SOLD OUT → AVAILABLE。

### 商品名・長さ・特徴・おすすめ
該当セルを書き換えるだけです。

### 表示順
「表示順」の数字が小さい順です。

### 新商品追加
1. 新しい画像を `images/products/` にGitHubへ追加
2. 「商品管理」に1行追加
3. 重複しない商品IDを入力
4. 画像ファイル名を完全一致で入力
5. 2wayの場合だけSTYLE 02を「2way画像」に入力
6. AVAILABLE / 表示順 / その他情報を入力
7. サイトを再読み込み

## 2way
Arc Pearlは1商品です。
STYLE 01 = S__146358281.jpg
STYLE 02 = S__146358280.jpg

## 画像名
GitHub Pagesは大文字・小文字を区別します。
スプレッドシートと `images/products/` のファイル名を完全一致させてください。

## ローカル確認
index.htmlをPCでダブルクリックすると、ブラウザの制限でGoogle Sheets取得が失敗する場合があります。
本番確認はGitHub Pagesの https:// 公開URLで行ってください。

## 維持している既存仕様
- Lunaロゴだけのファーストビュー
- ロゴアニメーション
- グレー基調
- Collection基本デザイン
- クリック/タップ商品詳細
- 2way STYLE切替
- SOLD OUT表示
- ABOUTの見出し・文章・画像
- Instagram DM注文
- レスポンシブ対応
