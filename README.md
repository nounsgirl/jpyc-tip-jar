# 🍀 JPYC Tip Jar

**深海このか専用 JPYC投げ銭システム**

Polygon Network上でJPYC（日本円ステーブルコイン）を使った投げ銭（チップ）を簡単に受け取れるWebアプリケーションです。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Network: Polygon](https://img.shields.io/badge/Network-Polygon-8247e5)](https://polygon.technology/)
[![Token: JPYC](https://img.shields.io/badge/Token-JPYC-10b981)](https://jpyc.jp/)

## 🌟 特徴

- ✅ **簡単な操作** - ウォレット接続後、3クリックで投げ銭完了
- 💰 **JPYC対応** - 日本円ステーブルコイン（1 JPYC = 1円）
- 🟣 **Polygon Network** - 低ガス代で高速トランザクション
- 📱 **モバイル対応** - スマホからでも簡単に送金可能
- 🔗 **複数ウォレット対応** - MetaMask、Rainbow、Trust Wallet等
- 𝕏 **Xシェア機能** - 投げ銭後にXでシェア可能
- 🎨 **カスタマイズ可能** - 簡単に自分専用にアレンジ可能

## 📸 スクリーンショット

### メイン画面
金額選択とウォレット接続

### 送信確認画面
トランザクション詳細の確認

### 完了画面
Xシェアボタン付き成功画面

## 🚀 デモ

👉 **[ライブデモを見る](https://nounsgirl.github.io/jpyc-tip-jar/)**

※ デモモードで各画面をプレビューできます

## 📋 必要なもの

### 送る側（支援者）
- Web3ウォレット（MetaMask推奨）
- Polygon Network上のJPYC残高
- 少額のMATIC（ガス代用、約0.001 MATIC）

### 受け取る側（クリエイター）
- Polygon Networkのウォレットアドレス
- GitHubアカウント（GitHub Pagesで公開する場合）

## 🎯 使い方

### 支援者側

1. **ウォレットを準備**
   - MetaMaskをインストール
   - Polygon Networkに切り替え
   - JPYCを購入・準備

2. **投げ銭ページにアクセス**
   - サイトを開く
   - 「接続する」ボタンをクリック

3. **金額を選択**
   - プリセット金額（500円〜）を選択
   - またはカスタム金額を入力

4. **送信**
   - 「投げ銭を送る」ボタンをクリック
   - ウォレットで承認

5. **完了！**
   - Xでシェア（任意）

### クリエイター側

このプロジェクトをフォークして、あなた専用の投げ銭ページを作成できます。

## 🛠️ 自分専用にカスタマイズする方法

### ステップ1: リポジトリをフォーク

1. このリポジトリの右上の「Fork」ボタンをクリック
2. あなたのGitHubアカウントにコピーされます

### ステップ2: 必須の変更点

#### 2-1. 受取アドレスを変更（最重要！）

`index.html` の **913行目** を編集：

```javascript
// ❌ 変更前
const RECIPIENT_ADDRESS = '0x73ddbe4fc933006645c300f7fca724170664d4c6';

// ✅ 変更後（あなたのウォレットアドレスに変更）
const RECIPIENT_ADDRESS = '0xあなたのウォレットアドレス';
```

⚠️ **超重要**: これを変更しないと、投げ銭が深海このかに送られます！

#### 2-2. プロフィール情報を変更

`index.html` の **726〜745行目** を編集：

```html
<!-- プロフィール画像 -->
<img src="konoka.png" alt="あなたの名前" class="profile-image">

<!-- 名前 -->
<div class="profile-name">あなたの名前</div>

<!-- サブタイトル -->
<div class="profile-subtitle">
    <span>🎨</span>
    <span>イラストレーター</span> <!-- あなたの職業 -->
</div>
```

#### 2-3. プロフィール画像を追加

1. あなたのプロフィール画像を用意（推奨: 正方形、500x500px以上）
2. ファイル名を `konoka.png` に変更
3. リポジトリのルートにアップロード

または、`index.html` の画像パスを変更：

```html
<img src="your-image.png" alt="あなたの名前" class="profile-image">
```

#### 2-4. Xシェア用URLを変更

`index.html` の **838行目** のURLを編集：

```html
<!-- 変更前 -->
url=https%3A%2F%2Fnounsgirl.github.io%2Fjpyc-tip-jar%2F

<!-- 変更後（あなたのGitHub PagesのURLに変更） -->
url=https%3A%2F%2Fあなたのユーザー名.github.io%2Fリポジトリ名%2F
```

💡 URLエンコードが必要です。以下のサイトで変換できます：
- https://www.urlencoder.org/

例：
- 元のURL: `https://yourname.github.io/jpyc-tip/`
- エンコード後: `https%3A%2F%2Fyourname.github.io%2Fjpyc-tip%2F`

### ステップ3: オプションのカスタマイズ

#### 3-1. 金額のプリセットを変更

`index.html` の **755〜782行目** を編集：

```html
<!-- 例: 金額を変更 -->
<button class="amount-button" onclick="selectAmount(100, this)">
    <div class="amount-value">¥100</div>
    <div class="amount-currency">JPYC</div>
</button>
```

#### 3-2. カラーテーマを変更

`index.html` の **15〜20行目** のグラデーションを編集：

```css
body {
    /* グリーン系から別の色に変更可能 */
    background: linear-gradient(135deg, #1a4d2e 0%, #2d5f3f 50%, #0f3820 100%);
}
```

カラー例：
- ピンク系: `#be185d 0%, #ec4899 50%, #9d174d 100%`
- ブルー系: `#1e3a8a 0%, #3b82f6 50%, #1e40af 100%`
- パープル系: `#5b21b6 0%, #8b5cf6 50%, #6d28d9 100%`

#### 3-3. Xシェアのメッセージを変更

`index.html` の **838行目** のテキスト部分を編集：

```html
<!-- エンコード前の元のテキスト -->
深海このかを応援しました！🍀

JPYCで投げ銭できます

#深海このか #JPYC #投げ銭

<!-- ↓ あなた用に変更 -->
[あなたの名前]を応援しました！

JPYCで投げ銭できます

#あなたの名前 #JPYC #投げ銭
```

変更後、必ずURLエンコードしてください。

#### 3-4. 成功画面のメッセージを変更

`index.html` の **827〜832行目** を編集：

```html
<h2 class="success-title">チップを送りました！</h2>
<p class="success-message">
    あなたの名前への応援、ありがとうございます！🍀<br>
    あなたの温かいサポートが、<br>
    創作活動の大きな励みになります。
</p>
```

### ステップ4: GitHub Pagesで公開

1. リポジトリの「Settings」を開く
2. 左メニューから「Pages」を選択
3. Source: `Deploy from a branch` を選択
4. Branch: `main` または `master` を選択
5. 「Save」をクリック

数分後、以下のURLで公開されます：
```
https://あなたのユーザー名.github.io/リポジトリ名/
```

## ⚙️ 技術仕様

### 対応ネットワーク
- **Polygon Mainnet** (Chain ID: 137)

### 対応トークン
- **JPYC** (ERC-20)
  - Contract: `0xE7C3D8C9a439feDe00D2600032D5dB0Be71C3c29`
  - Decimals: 18

### 対応ウォレット
- MetaMask（推奨）
- Rainbow Wallet
- Trust Wallet
- Coinbase Wallet
- その他EIP-1193対応ウォレット

### 使用技術
- HTML5 / CSS3 / JavaScript (ES6+)
- ethers.js v5.7.2
- Web3 Provider (EIP-1193)

## 🔒 セキュリティ

- ✅ トランザクションはすべてユーザーのウォレットで実行
- ✅ 秘密鍵はブラウザから送信されない
- ✅ スマートコントラクトは使用せず、直接転送
- ✅ オープンソースで監査可能

### セキュリティのベストプラクティス

1. **受取アドレスの確認**
   - 必ず自分のアドレスに変更したか確認
   - テスト送金で動作確認

2. **GitHubの設定**
   - リポジトリを公開する場合、秘密鍵等は含めない
   - `.env`ファイルは絶対にコミットしない

3. **定期的な確認**
   - Polygonscanで受け取ったJPYCを確認
   - 不審なトランザクションがないかチェック

## 📱 モバイル対応

### PCブラウザ
- Chrome（推奨）
- Firefox
- Edge
- Safari

### スマートフォン
- **推奨**: MetaMaskアプリ内ブラウザで開く
- または: 通常のブラウザで開き、「接続する」ボタンからMetaMaskアプリを起動

#### スマホでの使い方
1. MetaMaskアプリを開く
2. メニュー → ブラウザ
3. あなたの投げ銭ページのURLを入力
4. そのまま操作可能

## 🐛 トラブルシューティング

### Q: 「ネットワークが正しくありません」と表示される
**A:** MetaMaskをPolygon Networkに切り替えてください。

### Q: 「JPYC残高が不足しています」と表示される
**A:** Polygon Network上でJPYCを購入・準備してください。
- [JPYC公式サイト](https://jpyc.jp/)

### Q: 投げ銭が自分に届かない
**A:** `RECIPIENT_ADDRESS` を自分のアドレスに変更しましたか？

### Q: スマホでXシェアボタンが動かない
**A:** 最新版では修正済みです。`index.html`を更新してください。

### Q: プロフィール画像が表示されない
**A:** 
- 画像ファイルがリポジトリにアップロードされているか確認
- ファイル名とHTMLのパスが一致しているか確認
- 画像形式が対応しているか確認（PNG, JPG推奨）

## 📊 JPYCについて

**JPYC（JPY Coin）**は、日本円と1:1で連動するステーブルコインです。

### 特徴
- 🇯🇵 日本円建て（1 JPYC = 1円）
- 🔐 資金移動業者として正式登録
- 💱 取引所で購入可能
- 🌐 複数のブロックチェーンに対応

### JPYCの入手方法

1. **取引所で購入**
   - SBI VCトレード
   - ビットバンク
   - その他対応取引所

2. **公式サイトで購入**
   - https://jpyc.jp/

3. **ブリッジを使用**
   - Ethereumから他のチェーンへブリッジ

## 🤝 コントリビューション

プルリクエストを歓迎します！

1. このリポジトリをフォーク
2. 機能ブランチを作成 (`git checkout -b feature/amazing-feature`)
3. 変更をコミット (`git commit -m 'Add some amazing feature'`)
4. ブランチにプッシュ (`git push origin feature/amazing-feature`)
5. プルリクエストを作成

## 📜 ライセンス

このプロジェクトは MIT ライセンスの下で公開されています。

## 🙏 謝辞

- [JPYC](https://jpyc.jp/) - 日本円ステーブルコインの提供
- [Polygon](https://polygon.technology/) - 高速・低コストなネットワーク
- [ethers.js](https://docs.ethers.org/) - Web3ライブラリ
- [MetaMask](https://metamask.io/) - ウォレットインターフェース

## 💬 サポート

質問や問題がある場合は、以下の方法でお問い合わせください：

- **Issues**: GitHubのIssuesタブで報告
- **X (Twitter)**: @あなたのアカウント

## 🔗 リンク

- [JPYC公式サイト](https://jpyc.jp/)
- [Polygon公式サイト](https://polygon.technology/)
- [MetaMask](https://metamask.io/)
- [ethers.js ドキュメント](https://docs.ethers.org/)

---

**Made with 🍀 for クリエイターの応援**

このテンプレートを使って、あなただけの投げ銭システムを作りましょう！
