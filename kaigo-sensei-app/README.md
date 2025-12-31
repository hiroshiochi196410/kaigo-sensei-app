# 🏥 Kaigo Sensei - 修正版デプロイパッケージ

## ✅ このパッケージは動作確認済みです

---

## 🚀 デプロイ手順（5分）

### ステップ1：Claude APIキーを取得

1. https://console.anthropic.com にアクセス
2. アカウント作成 & ログイン
3. 「API Keys」→「Create Key」
4. APIキーをコピー（`sk-ant-api03-xxxxx`）
5. $5〜$20をチャージ

---

### ステップ2：Vercelにデプロイ

#### 方法A：新規プロジェクト（推奨）

1. https://vercel.com にログイン
2. 「Add New」→「Project」
3. `kaigo-sensei-deploy-fixed`フォルダをドラッグ&ドロップ
4. 「Deploy」をクリック

#### 方法B：既存プロジェクトを削除して再作成

1. 古いプロジェクト「kaigo-sensei-deploy-q9ns」を削除
2. 上記の方法Aで新規作成

---

### ステップ3：環境変数を設定

1. デプロイ完了後、「Settings」
2. 「Environment Variables」
3. 追加：
   ```
   Name:  ANTHROPIC_API_KEY
   Value: sk-ant-api03-xxxxx（あなたのAPIキー）
   ```
4. 「Save」

---

### ステップ4：再デプロイ

1. 「Deployments」タブ
2. 最新デプロイの「...」→「Redeploy」
3. 完了を待つ

---

### ステップ5：動作確認

1. 「Visit」ボタンをクリック
2. Kaigo Sensei V4が表示される！
3. 翻訳・練習・ロールプレイを試す

---

## 📁 ファイル構成

```
kaigo-sensei-deploy-fixed/
├── api/
│   └── chat.js          # サーバーレス関数
├── index.html           # V4アプリ（ルート配置）
├── vercel.json          # シンプルな設定
└── README.md            # このファイル
```

**重要：**
- `index.html`はルート直下に配置
- `public`フォルダは不要
- vercel.jsonは最小限の設定

---

## 💡 トラブルシューティング

### 404エラーが出る
- 環境変数を設定しましたか？
- 再デプロイしましたか？
- ブラウザで強制リロード（Ctrl+Shift+R）

### APIエラーが出る
- 環境変数名が正確か確認（`ANTHROPIC_API_KEY`）
- APIキーが正しいか確認
- Anthropicでクレジットがあるか確認

---

## 🎯 完了！

デプロイが成功したら：
- URLをシェア
- ユーザーにテストしてもらう
- フィードバックを収集

**次のステップ：営業資料作成 → B2B営業開始！**

---

**最終更新: 2024年12月30日**
