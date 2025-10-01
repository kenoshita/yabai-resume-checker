# やばい職務経歴書チェッカー（モック）

職務経歴書の“やばポイント”を可視化し、改善ガイド（数値はユーザー入力）を提示する軽量モック。  
静的サイトとして **Render** にデプロイできます。

## ローカルで試す
1. このリポジトリをZIPでダウンロード or クローン
2. `index.html` をブラウザで開くだけ

## Render（Static Site）にデプロイ
1. このフォルダを GitHub に新規リポジトリとしてプッシュ
2. Render ダッシュボード → **New** → **Static Site**
3. Repository: このリポジトリ  
   Build Command: *(空のまま)*  
   Publish Directory: `.`  
4. **Create Static Site** を押すと公開されます

※ `static.json` により、HTMLは no-cache、将来のSPA化もOK。

## 構成
- `index.html` … UIモック本体（アップロード→警告→ガイド）
- `privacy.html` … 簡易プライバシー/免責
- `static.json` … Renderのヘッダー/リライト設定
- `robots.txt` … 検索クローラ向け
- `favicon.svg` … SVGアイコン

## 注意
- 解析ロジックはダミー（`MOCK_ISSUES`）。本実装ではAPI応答に差し替え。
- 数値の自動生成は行いません（ユーザー入力前提）。
