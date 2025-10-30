# ウエストパーク社労士事務所 ウェブサイト

## 開発原則
- **KISS** (Keep It Simple, Stupid) - シンプルで理解しやすいコード
- **YAGNI** (You Aren't Gonna Need It) - 必要な機能のみ実装
- **DRY** (Don't Repeat Yourself) - 重複を避ける

## プロジェクト概要
福岡市中央区の社労士事務所「ウエストパーク社労士事務所」の公式ウェブサイト

## 技術構成
- **フロントエンド**: HTML5, Tailwind CSS (CDN), JavaScript
- **デザイン**: サイドバーレイアウト、レスポンシブ対応
- **フォーム**: EmailJS
- **ホスティング**: Cloudflare Pages

## ファイル構成
- `docs/` - 公開用HTMLファイル群（Cloudflare Pages用）
  - `index.html` - ホームページ
  - `about.html` - 事務所案内
  - `services.html` - 業務内容
  - `pricing.html` - 料金案内
  - `subsidies.html` - 助成金情報
  - `contact.html` - お問い合わせ
  - `images/` - 画像ファイル
- `Design.md` - ウェブサイト設計書
- `01-05-*.md` - コンテンツファイル（分割済み）

## EmailJS設定
以下の値を実際のEmailJS設定に変更：
- `YOUR_EMAILJS_USER_ID`
- `YOUR_SERVICE_ID` 
- `YOUR_TEMPLATE_ID`

## コミット規則
- 絵文字を使用（📝 ✨ 🐛 🎨 等）

## 連絡先
- **代表**: 野口 聡（のぐち さとる）（特定社会保険労務士）
- **電話**: 080-3948-2324
- **メール**: westpark-sr@gmail.com
