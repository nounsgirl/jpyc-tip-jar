# 📖 初心者向け完全カスタマイズガイド

このガイドでは、プログラミング経験がない方でも、自分専用の投げ銭ページを作成できるよう、画面付きで詳しく説明します。

## 📝 目次

1. [事前準備](#事前準備)
2. [Step 1: GitHubアカウント作成](#step-1-githubアカウント作成)
3. [Step 2: リポジトリをフォーク](#step-2-リポジトリをフォーク)
4. [Step 3: 受取アドレスの変更（最重要！）](#step-3-受取アドレスの変更最重要)
5. [Step 4: プロフィール情報の変更](#step-4-プロフィール情報の変更)
6. [Step 5: プロフィール画像のアップロード](#step-5-プロフィール画像のアップロード)
7. [Step 6: GitHub Pagesで公開](#step-6-github-pagesで公開)
8. [Step 7: Xシェア設定](#step-7-xシェア設定)
9. [オプション: さらなるカスタマイズ](#オプションさらなるカスタマイズ)

---

## 事前準備

### 必要なもの

✅ **ウォレットアドレス**
- MetaMaskなどのウォレットアドレス（0xから始まる42文字）
- Polygon Networkに対応している必要があります
- 例: `0x1234567890123456789012345678901234567890`

✅ **プロフィール画像**（任意）
- 正方形の画像（推奨: 500x500px以上）
- PNG または JPG形式
- ファイルサイズ: 1MB以下推奨

✅ **GitHubアカウント**
- まだ持っていない場合は、これから作成します

⚠️ **注意**: ウォレットアドレスは絶対に間違えないように、コピー＆ペーストしてください！

---

## Step 1: GitHubアカウント作成

### すでにアカウントがある場合
→ このステップはスキップして、[Step 2](#step-2-リポジトリをフォーク) へ

### アカウントを持っていない場合

1. **GitHub公式サイトにアクセス**
   - https://github.com にアクセス

2. **「Sign up」をクリック**
   - 右上の緑色のボタン

3. **アカウント情報を入力**
   - メールアドレス
   - パスワード（強力なものを設定）
   - ユーザー名（例: `yourname123`）
   - ⚠️ ユーザー名は後で変更できないので慎重に！

4. **メール認証**
   - 届いたメールのリンクをクリック

5. **完了！**

---

## Step 2: リポジトリをフォーク

「フォーク」とは、他の人のプロジェクトをあなたのアカウントにコピーすることです。

### 手順

1. **元のリポジトリにアクセス**
   - https://github.com/nounsgirlgirl/jpyc-tipjar

2. **右上の「Fork」ボタンをクリック**
   - 緑色または灰色のボタンです

3. **「Create fork」をクリック**
   - Repository nameはそのままでOK
   - または、好きな名前に変更（例: `my-tipjar`）

4. **完了！**
   - あなたのアカウントに `jpyc-tipjar` がコピーされました
   - URL: `https://github.com/あなたのユーザー名/jpyc-tipjar`

---

## Step 3: 受取アドレスの変更（最重要！）

⚠️ **超重要**: これを変更しないと、投げ銭が深海このかに送られます！

### 手順

1. **`index.html` ファイルを開く**
   - あなたのリポジトリで `index.html` をクリック

2. **編集ボタンをクリック**
   - 右上の鉛筆マーク（✏️）をクリック

3. **913行目を探す**
   - `Ctrl + F`（Macは `Cmd + F`）で検索
   - 「RECIPIENT_ADDRESS」と入力して検索
   - 以下の行が見つかります：

```javascript
const RECIPIENT_ADDRESS = '0x73ddbe4fc933006645c300f7fca724170664d4c6';
```

4. **アドレスを変更**
   - シングルクォート `'` の中身だけを変更
   - あなたのウォレットアドレスに置き換え

**変更前:**
```javascript
const RECIPIENT_ADDRESS = '0x73ddbe4fc933006645c300f7fca724170664d4c6';
```

**変更後（例）:**
```javascript
const RECIPIENT_ADDRESS = '0x1234567890123456789012345678901234567890';
                          ↑あなたのアドレス↑
```

5. **確認**
   - ✅ `0x` から始まっているか
   - ✅ 全部で42文字（0xを含む）か
   - ✅ シングルクォート `'` で囲まれているか
   - ✅ セミコロン `;` があるか

6. **保存**
   - 下にスクロールして「Commit changes」をクリック
   - Commit message: `Change recipient address` (または日本語で「受取アドレスを変更」)
   - 「Commit changes」をクリック

🎉 **完了！** 投げ銭があなたのアドレスに届くようになりました。

---

## Step 4: プロフィール情報の変更

### 4-1. 名前を変更

1. **`index.html` を編集**
   - 再度 `index.html` を開いて編集（鉛筆マーク）

2. **732行目を探す**
   - `Ctrl + F` で「profile-name」を検索
   - 以下の行が見つかります：

```html
<div class="profile-name">深海このか</div>
```

3. **名前を変更**

**変更前:**
```html
<div class="profile-name">深海このか</div>
```

**変更後（例）:**
```html
<div class="profile-name">あなたの名前</div>
```

### 4-2. 肩書きを変更

1. **736行目を探す**
   - `Ctrl + F` で「イラストレーター」を検索

```html
<span>イラストレーター</span>
```

2. **肩書きを変更**

**例:**
```html
<span>漫画家</span>
<span>音楽家</span>
<span>配信者</span>
<span>クリエイター</span>
```

### 4-3. 絵文字を変更

1. **735行目の絵文字を変更**

```html
<span>🎨</span>  <!-- 元の絵文字 -->
```

**例:**
```html
<span>🎵</span>  <!-- 音楽家 -->
<span>📝</span>  <!-- ライター -->
<span>🎮</span>  <!-- ゲーム配信者 -->
<span>📷</span>  <!-- カメラマン -->
```

💡 絵文字を探すには: https://emojipedia.org/

### 4-4. 保存

- 「Commit changes」をクリック
- Commit message: `Update profile information`

---

## Step 5: プロフィール画像のアップロード

### 5-1. 画像を準備

- **推奨サイズ**: 500x500px 〜 1000x1000px
- **形式**: PNG または JPG
- **ファイル名**: `konoka.png` に変更（または好きな名前）

💡 **画像を正方形にする方法**
- オンラインツール: https://crop-circle.imageonline.co/
- または: Canvaなどのデザインツール

### 5-2. GitHubにアップロード

1. **リポジトリのトップページに戻る**
   - あなたの `jpyc-tipjar` リポジトリ

2. **「Add file」→「Upload files」をクリック**

3. **画像をドラッグ＆ドロップ**
   - または「choose your files」でファイルを選択

4. **「Commit changes」をクリック**
   - Commit message: `Add profile image`

### 5-3. 画像パスを確認・変更

異なるファイル名を使用した場合:

1. **`index.html` を編集**

2. **726行目を探す**
```html
<img src="konoka.png" alt="深海このか" class="profile-image">
```

3. **ファイル名を変更**
```html
<img src="your-image.png" alt="あなたの名前" class="profile-image">
```

4. **保存**

---

## Step 6: GitHub Pagesで公開

### 手順

1. **Settings に移動**
   - リポジトリの上部メニューから「Settings」をクリック

2. **Pages を選択**
   - 左メニューから「Pages」をクリック

3. **ソースを設定**
   - **Source**: `Deploy from a branch` を選択
   - **Branch**: `main` または `master` を選択
   - **Folder**: `/ (root)` のまま
   - 「Save」をクリック

4. **数分待つ**
   - デプロイには2〜5分かかります

5. **URLを確認**
   - ページ上部に緑色のボックスが表示されます
   - "Your site is live at https://あなたのユーザー名.github.io/jpyc-tipjar/"

6. **アクセスして確認！**
   - URLをクリックして動作を確認

🎉 **公開完了！** このURLをシェアすれば、誰でもアクセスできます。

---

## Step 7: Xシェア設定

### URLをエンコード

XシェアボタンのURLを、あなたのページに変更します。

#### 7-1. あなたのURLをエンコード

1. **エンコードサイトにアクセス**
   - https://www.urlencoder.org/

2. **URLを入力**
   - 例: `https://yourname.github.io/jpyc-tipjar/`

3. **「ENCODE」をクリック**
   - 結果: `https%3A%2F%2Fyourname.github.io%2Fjpyc-tipjar%2F`

4. **結果をコピー**

#### 7-2. HTMLを編集

1. **`index.html` を編集**

2. **838行目を探す**
   - `Ctrl + F` で「url=https%3A%2F」を検索

```html
url=https%3A%2F%2Fnounsgirl.github.io%2Fjpyc-tip-jar%2F
```

3. **URLを置き換え**

**変更前:**
```html
url=https%3A%2F%2Fnounsgirl.github.io%2Fjpyc-tip-jar%2F
```

**変更後（例）:**
```html
url=https%3A%2F%2Fyourname.github.io%2Fjpyc-tipjar%2F
```

4. **保存**

#### 7-3. メッセージも変更（任意）

同じく838行目の `text=` の部分も変更できます。

**変更前:**
```
text=%E6%B7%B1%E6%B5%B7%E3%81%93%E3%81%AE%E3%81%8B%E3%82%92%E5%BF%9C%E6%8F%B4%E3%81%97%E3%81%BE%E3%81%97%E3%81%9F%EF%BC%81
```

**変更方法:**

1. 新しいメッセージを作成
```
あなたの名前を応援しました！🍀

JPYCで投げ銭できます

#あなたの名前 #JPYC #投げ銭
```

2. エンコードサイトでエンコード
   - https://www.urlencoder.org/

3. 結果を `text=` の後に貼り付け

---

## オプション: さらなるカスタマイズ

### 金額のプリセットを変更

**755〜782行目**を編集:

```html
<!-- 500円ボタン -->
<button class="amount-button" onclick="selectAmount(500, this)">
    <div class="amount-value">¥500</div>
    <div class="amount-currency">JPYC</div>
</button>
```

数字を変更するだけ：
```html
<!-- 100円に変更 -->
<button class="amount-button" onclick="selectAmount(100, this)">
    <div class="amount-value">¥100</div>
    <div class="amount-currency">JPYC</div>
</button>
```

### カラーテーマを変更

**15〜20行目**を編集:

```css
body {
    background: linear-gradient(135deg, #1a4d2e 0%, #2d5f3f 50%, #0f3820 100%);
}
```

**色の例:**

```css
/* ピンク系 */
background: linear-gradient(135deg, #be185d 0%, #ec4899 50%, #9d174d 100%);

/* ブルー系 */
background: linear-gradient(135deg, #1e3a8a 0%, #3b82f6 50%, #1e40af 100%);

/* パープル系 */
background: linear-gradient(135deg, #5b21b6 0%, #8b5cf6 50%, #6d28d9 100%);

/* オレンジ系 */
background: linear-gradient(135deg, #c2410c 0%, #f97316 50%, #9a3412 100%);
```

💡 色を探すには: https://colorhunt.co/

---

## ✅ チェックリスト

カスタマイズが完了したら、以下を確認してください：

- [ ] `RECIPIENT_ADDRESS` を自分のアドレスに変更した
- [ ] プロフィール名を変更した
- [ ] プロフィール画像をアップロードした（任意）
- [ ] GitHub Pagesで公開した
- [ ] 公開URLにアクセスして動作確認した
- [ ] テスト送金を行い、自分のウォレットに届くか確認した

⚠️ **重要**: 本番運用前に、必ず少額（例: 1 JPYC）でテスト送金してください！

---

## 🆘 困ったときは

### エラーが出る場合

1. **ブラウザのキャッシュをクリア**
   - `Ctrl + F5`（Mac: `Cmd + Shift + R`）

2. **変更が反映されない**
   - GitHub Pagesの更新には5分程度かかります
   - 少し待ってから再度アクセス

3. **構文エラー**
   - クォート `'` や `"` を削除していないか確認
   - セミコロン `;` が残っているか確認

### よくある間違い

❌ **間違い例 1: クォートを削除**
```javascript
const RECIPIENT_ADDRESS = 0x1234567890123456789012345678901234567890;
                          ↑クォートがない！
```

✅ **正しい例:**
```javascript
const RECIPIENT_ADDRESS = '0x1234567890123456789012345678901234567890';
                          ↑クォート必須↑
```

❌ **間違い例 2: セミコロンを削除**
```javascript
const RECIPIENT_ADDRESS = '0x1234567890123456789012345678901234567890'
                                                                    ↑セミコロンがない！
```

✅ **正しい例:**
```javascript
const RECIPIENT_ADDRESS = '0x1234567890123456789012345678901234567890';
                                                                    ↑セミコロン必須↑
```

---

## 📞 サポート

このガイドで解決しない問題がある場合：

1. GitHubのIssuesタブで質問
2. README.mdの「トラブルシューティング」セクションを確認

---

**🎉 お疲れ様でした！**

これであなた専用の投げ銭ページが完成しました。
たくさんのサポートが集まりますように！🍀
