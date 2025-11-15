# 🔧 カスタマイズ早見表

自分専用にアレンジする際の変更箇所一覧です。
`index.html` の各行番号と、変更すべき内容を記載しています。

---

## ⚠️ 必須の変更（やらないとダメ！）

### 1. 受取アドレス（最重要！）

**行番号: 913**

```javascript
const RECIPIENT_ADDRESS = '0x73ddbe4fc933006645c300f7fca724170664d4c6';
```

↓ あなたのウォレットアドレスに変更

```javascript
const RECIPIENT_ADDRESS = '0xあなたのウォレットアドレス';
```

⚠️ これを変更しないと投げ銭が深海このかに送られます！

---

## 🎨 基本情報の変更（推奨）

### 2. プロフィール名

**行番号: 732**

```html
<div class="profile-name">深海このか</div>
```

↓

```html
<div class="profile-name">あなたの名前</div>
```

---

### 3. プロフィール肩書き

**行番号: 735-736**

```html
<span>🎨</span>
<span>イラストレーター</span>
```

↓

```html
<span>🎵</span>  <!-- 好きな絵文字 -->
<span>音楽家</span>  <!-- あなたの職業 -->
```

**絵文字の例:**
- 🎨 イラストレーター
- 🎵 音楽家
- 📝 ライター
- 🎮 配信者
- 📷 写真家
- 💻 開発者

---

### 4. プロフィール画像

**行番号: 726**

```html
<img src="konoka.png" alt="深海このか" class="profile-image">
```

↓ 画像ファイル名とaltテキストを変更

```html
<img src="your-image.png" alt="あなたの名前" class="profile-image">
```

**画像の準備:**
- ファイルをリポジトリにアップロード
- 推奨: 正方形、500x500px以上
- 形式: PNG または JPG

---

### 5. Xシェア用URL

**行番号: 838**

```html
url=https%3A%2F%2Fnounsgirl.github.io%2Fjpyc-tip-jar%2F
```

↓ あなたのGitHub PagesのURLに変更（URLエンコード必須）

```html
url=https%3A%2F%2Fあなたのユーザー名.github.io%2Fリポジトリ名%2F
```

**URLエンコード方法:**
1. あなたのURL: `https://yourname.github.io/jpyc-tipjar/`
2. https://www.urlencoder.org/ でエンコード
3. 結果: `https%3A%2F%2Fyourname.github.io%2Fjpyc-tipjar%2F`

---

### 6. Xシェアメッセージ

**行番号: 838**（同じ行の `text=` 部分）

```
text=%E6%B7%B1%E6%B5%B7%E3%81%93%E3%81%AE%E3%81%8B%E3%82%92...
```

↓ あなた用のメッセージに変更

**エンコード前:**
```
あなたの名前を応援しました！🍀

JPYCで投げ銭できます

#あなたの名前 #JPYC #投げ銭
```

**エンコード後に貼り付け**
- https://www.urlencoder.org/ を使用

---

## 💰 金額設定の変更（任意）

### 7. プリセット金額

**行番号: 755-782**

```html
<!-- 500円ボタン -->
<button class="amount-button" onclick="selectAmount(500, this)">
    <div class="amount-value">¥500</div>
    <div class="amount-currency">JPYC</div>
</button>

<!-- 1000円ボタン -->
<button class="amount-button" onclick="selectAmount(1000, this)">
    <div class="amount-value">¥1,000</div>
    <div class="amount-currency">JPYC</div>
</button>

<!-- 3000円ボタン -->
<button class="amount-button" onclick="selectAmount(3000, this)">
    <div class="amount-value">¥3,000</div>
    <div class="amount-currency">JPYC</div>
</button>

<!-- 5000円ボタン -->
<button class="amount-button" onclick="selectAmount(5000, this)">
    <div class="amount-value">¥5,000</div>
    <div class="amount-currency">JPYC</div>
</button>
```

**変更方法:**
- `selectAmount(500, this)` の数字を変更
- `¥500` の表示も同じ金額に変更

**例: 100円ボタンを追加**
```html
<button class="amount-button" onclick="selectAmount(100, this)">
    <div class="amount-value">¥100</div>
    <div class="amount-currency">JPYC</div>
</button>
```

---

## 🎨 デザインの変更（任意）

### 8. 背景色（グラデーション）

**行番号: 15-20**

```css
body {
    background: linear-gradient(135deg, #1a4d2e 0%, #2d5f3f 50%, #0f3820 100%);
}
```

**カラーパターン例:**

```css
/* ピンク系 */
background: linear-gradient(135deg, #be185d 0%, #ec4899 50%, #9d174d 100%);

/* ブルー系 */
background: linear-gradient(135deg, #1e3a8a 0%, #3b82f6 50%, #1e40af 100%);

/* パープル系 */
background: linear-gradient(135deg, #5b21b6 0%, #8b5cf6 50%, #6d28d9 100%);

/* レッド系 */
background: linear-gradient(135deg, #991b1b 0%, #dc2626 50%, #7f1d1d 100%);

/* オレンジ系 */
background: linear-gradient(135deg, #c2410c 0%, #f97316 50%, #9a3412 100%);

/* イエロー系 */
background: linear-gradient(135deg, #ca8a04 0%, #eab308 50%, #a16207 100%);
```

---

### 9. 成功画面のメッセージ

**行番号: 827-832**

```html
<h2 class="success-title">チップを送りました！</h2>
<p class="success-message">
    深海このかへの応援、ありがとうございます！🍀<br>
    あなたの温かいサポートが、<br>
    創作活動の大きな励みになります。
</p>
```

↓ あなた用のメッセージに変更

```html
<h2 class="success-title">チップを送りました！</h2>
<p class="success-message">
    [あなたの名前]への応援、ありがとうございます！🍀<br>
    あなたの温かいサポートが、<br>
    創作活動の大きな励みになります。
</p>
```

---

### 10. フッターメッセージ

**行番号: 850-852**

```html
<p style="font-weight: 600; color: #1a4d2e;">
    いつも応援ありがとうございます！
</p>
```

↓ 好きなメッセージに変更

---

## 📊 変更チェックリスト

コピーして使ってください：

```
[ ] 受取アドレスを変更した（行番号: 913）
[ ] プロフィール名を変更した（行番号: 732）
[ ] プロフィール肩書きを変更した（行番号: 735-736）
[ ] プロフィール画像をアップロードした
[ ] 画像パスを変更した（行番号: 726）
[ ] Xシェア用URLを変更した（行番号: 838）
[ ] Xシェアメッセージを変更した（行番号: 838）
[ ] 金額プリセットを変更した（任意）（行番号: 755-782）
[ ] 背景色を変更した（任意）（行番号: 15-20）
[ ] 成功メッセージを変更した（任意）（行番号: 827-832）
[ ] GitHub Pagesで公開した
[ ] 公開URLで動作確認した
[ ] テスト送金を実施した（1 JPYCなど少額で）
```

---

## 🚨 よくある間違い

### ❌ 間違い 1: クォートを削除してしまう

```javascript
// ❌ ダメな例
const RECIPIENT_ADDRESS = 0x1234567890123456789012345678901234567890;

// ✅ 正しい例
const RECIPIENT_ADDRESS = '0x1234567890123456789012345678901234567890';
                          ↑必ずシングルクォートで囲む↑
```

---

### ❌ 間違い 2: セミコロンを削除してしまう

```javascript
// ❌ ダメな例
const RECIPIENT_ADDRESS = '0x1234567890123456789012345678901234567890'

// ✅ 正しい例
const RECIPIENT_ADDRESS = '0x1234567890123456789012345678901234567890';
                                                                    ↑セミコロン必須↑
```

---

### ❌ 間違い 3: 数字の桁を間違える

```javascript
// ❌ ダメな例（41文字しかない）
const RECIPIENT_ADDRESS = '0x123456789012345678901234567890123456789';

// ✅ 正しい例（42文字）
const RECIPIENT_ADDRESS = '0x1234567890123456789012345678901234567890';
                          ↑0xを含めて42文字↑
```

---

### ❌ 間違い 4: HTMLタグを壊してしまう

```html
<!-- ❌ ダメな例 -->
<div class="profile-name">あなたの名前

<!-- ✅ 正しい例 -->
<div class="profile-name">あなたの名前</div>
                                        ↑閉じタグ必須↑
```

---

## 💡 コピペ用テンプレート

### 受取アドレス変更用

```javascript
const RECIPIENT_ADDRESS = '0x[ここにあなたのアドレス]';
```

### プロフィール情報変更用

```html
<div class="profile-name">[あなたの名前]</div>
<div class="profile-subtitle">
    <span>[絵文字]</span>
    <span>[職業・肩書き]</span>
</div>
```

### 画像パス変更用

```html
<img src="[ファイル名].png" alt="[あなたの名前]" class="profile-image">
```

---

## 🔍 行番号の探し方

### GitHubの編集画面で

1. `Ctrl + F`（Mac: `Cmd + F`）で検索ボックスを開く
2. 検索したいテキストを入力（例: "RECIPIENT_ADDRESS"）
3. Enter で次の結果へジャンプ

### VSCodeなどのエディタで

1. 左側に行番号が表示される
2. `Ctrl + G`（Mac: `Cmd + G`）で行番号ジャンプ
3. 行番号を入力してEnter

---

## 📞 ヘルプ

変更方法がわからない場合：
1. [CUSTOMIZATION_GUIDE.md](CUSTOMIZATION_GUIDE.md) の詳細ガイドを確認
2. [README.md](README.md) のトラブルシューティングを確認
3. GitHubのIssuesで質問

---

**印刷推奨**: このページを印刷して、チェックしながら作業すると便利です！
