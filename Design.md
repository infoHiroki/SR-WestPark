# ウエストパーク社労士事務所 ウェブサイト設計書

## プロジェクト概要

**サイト名**: ウエストパーク社労士事務所 公式ウェブサイト  
**目的**: DXサポートと助成金申請に特化した社労士事務所のオンライン集客  
**ターゲット**: 福岡地域の中小企業経営者・人事担当者  

## 技術仕様

### フロントエンド
- **HTML5**: セマンティックマークアップ
- **Tailwind CSS**: ユーティリティファーストCSS（CDN版）
- **JavaScript**: EmailJS連携、モバイルサイドバー制御

### 外部サービス
- **EmailJS**: お問い合わせフォーム処理
- **Cloudflare Pages**: ホスティング・CDN
- **GitHub**: リポジトリ管理・自動デプロイ連携
- **独自ドメイン**: Cloudflare経由で設定予定

## サイト構造

### ページ構成
```
/ (index.html)          - ホームページ
/about.html             - 代表挨拶・事務所概要
/services.html          - 事業概要・サービス詳細
/pricing.html           - 料金案内
/subsidies.html         - DX助成金情報
/contact.html           - お問い合わせフォーム
```

### ファイル構造
```
├── docs/
│   ├── index.html
│   ├── about.html
│   ├── services.html
│   ├── pricing.html
│   ├── subsidies.html
│   ├── contact.html
│   └── images/
│       ├── logo-sidebar.png
│       ├── nishi-park-sakura.jpg
│       ├── noguchi-profile.png
│       ├── favicon-32x32.png
│       └── ogp.png
├── 01-representative-greeting.md
├── 02-office-overview.md
├── 03-business-overview.md
├── 04-pricing-guide.md
├── 05-dx-subsidies.md
├── Design.md
└── CLAUDE.md
```

## ページ設計

### 1. ホームページ (index.html)
**構成要素**:
- サイドバーナビゲーション（デスクトップ固定、モバイル開閉式）
- ヒーローセクション：西公園の桜背景画像
- 事務所の特徴（3つの柱）
  - DXサポート
  - 助成金申請代行
  - 労務相談・顧問
- お問い合わせCTA
- フッター

### 2. 代表挨拶・事務所概要 (about.html)
**コンテンツ**:
- 01-representative-greeting.md の内容
- 02-office-overview.md の内容
- 代表者写真エリア（予定）

### 3. サービス詳細 (services.html)
**コンテンツ**:
- 03-business-overview.md の内容
- 各サービスの詳細説明
- 実績・事例（今後追加予定）

### 4. 料金案内 (pricing.html)
**コンテンツ**:
- 04-pricing-guide.md の内容
- 料金表のビジュアル化
- 見積もり依頼CTA

### 5. 助成金情報 (subsidies.html)
**コンテンツ**:
- 05-dx-subsidies.md の内容
- 助成金の種類と申請フロー
- 成功事例（今後追加予定）

### 6. お問い合わせ (contact.html)
**機能**:
- EmailJS連携フォーム
- 事務所情報（住所・電話・営業時間）
- 地図埋め込み（Google Maps）

## デザイン方針

### カラーパレット
- **Primary**: ネイビーブルー (#1e3a8a)
- **Secondary**: ライトブルー (#3b82f6)
- **Accent**: オレンジ (#f59e0b)
- **背景**: ホワイト・グレー (#f9fafb)

### レイアウト構造
- **サイドバーレイアウト**: 左固定サイドバー（デスクトップ: 256px幅）
- **モバイル対応**: ハンバーガーメニュー、オーバーレイ式サイドバー
- **レスポンシブ**: Tailwind CSSのブレークポイント使用
- **最大幅**: 5xl（1280px）でコンテンツ制限

### デザイン特徴
- 西公園の桜をヒーローイメージに使用
- サイドバーに横長ロゴ配置
- ページ内目次機能（長いページ）
- スムーススクロール実装

## 機能要件

### 実装済み機能
- [x] レスポンシブデザイン（サイドバーレイアウト）
- [x] モバイルサイドバー開閉機能
- [x] お問い合わせフォーム（EmailJS）
- [x] スムーススクロール
- [x] SEO最適化（OGPタグ、メタタグ）
- [x] Favicon設定
- [x] ページ内目次ナビゲーション

### 追加機能（将来予定）
- [ ] ブログ機能
- [ ] 事例・実績ページ
- [ ] よくある質問ページ
- [ ] 多言語対応（英語）

## SEO対策

### メタタグ設定
- タイトル：各ページ固有 + 「ウエストパーク社労士事務所 | 福岡」
- ディスクリプション：各ページ120文字程度
- キーワード：「社労士 福岡」「DX 労務」「助成金申請」

### 構造化データ
- LocalBusiness スキーマ
- Organization スキーマ
- ContactPoint スキーマ

### ローカルSEO
- 福岡市中央区の地域キーワード最適化
- Googleマイビジネス連携準備

## デプロイ・運用

### Git管理
- GitHubリポジトリ: `infoHiroki/SR-WestPark`
- main ブランチから Cloudflare Pages 自動デプロイ

### Cloudflare Pages設定
- **ビルド出力ディレクトリ**: `docs`
- **フレームワークプリセット**: None（静的HTML）
- **カスタムドメイン**: 設定予定
- **HTTPS**: 自動設定

### 更新フロー
1. ローカルで編集
2. `git add` → `git commit` → `git push`
3. Cloudflare Pages自動デプロイ
4. 本番確認（数分で反映）

## 連絡先情報

**事務所**: ウエストパーク社労士事務所
**代表**: 野口 聡（のぐち さとる）
**住所**: 〒810-0061 福岡市中央区西公園4-46-304
**電話**: 080-3948-2324
**メール**: westpark-sr@gmail.com
**受付**: 平日 9:00〜17:00

## 開発進捗

1. **Phase 1**: 基本サイト構築（HTML/Tailwind CSS） ✅
2. **Phase 2**: EmailJS フォーム実装 ✅
3. **Phase 3**: デザイン調整・レスポンシブ対応 ✅
4. **Phase 4**: SEO最適化 ✅
5. **Phase 5**: Cloudflare Pagesデプロイ 🔄 進行中
6. **Phase 6**: カスタムドメイン設定 ⏳ 予定