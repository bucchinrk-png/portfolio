# Noriaki Portfolio Site

クラウドワークス案件獲得用のポートフォリオページ（1ファイル完結）。

## ファイル構成

```
portfolio-site/
├── index.html   # ポートフォリオ本体（単一HTML）
└── README.md    # このファイル
```

外部依存はすべて CDN 経由（Tailwind CSS / Google Fonts / Lucide Icons）。npmインストール・ビルド工程は不要。

## ローカルプレビュー方法

`index.html` をダブルクリックでブラウザが開きます。または：

```bash
# Python が入っていれば
cd portfolio-site
python -m http.server 8000
# → http://localhost:8000

# Node が入っていれば
npx serve portfolio-site
```

## 無料公開方法（おすすめ順）

### A. GitHub Pages（一番ラク）

1. GitHub に新規リポジトリを作成（例: `portfolio`）
2. このフォルダの中身を push
3. リポジトリの Settings → Pages → Source を「main / root」に設定
4. `https://<your-username>.github.io/portfolio/` で公開される

### B. Vercel（独自ドメイン使いたいなら）

1. https://vercel.com で GitHub 連携
2. リポジトリを import するだけで自動デプロイ
3. 無料プランでも独自ドメイン設定可能

### C. Netlify Drop（GitHubなしで一発）

1. https://app.netlify.com/drop にこのフォルダをドラッグ&ドロップ
2. 即時公開

## 公開前にやること

1. **連絡先URLを入れる**
   - `index.html` の検索: `お気軽にご相談ください` セクション
   - クラウドワークスのプロフィールURL: `<a href="#"` の `#` をクラウドワークスのURLに置換
   - メールアドレス: `<a href="mailto:"` を `mailto:bucchi.nrk@gmail.com` などに置換（公開メールアドレスを使うか検討）

2. **OGP画像を追加**（必須ではないが推奨）
   - SNS共有時に表示される画像を追加すると刺さりが強くなる
   - `<head>` に以下を追記:
     ```html
     <meta property="og:title" content="Noriaki｜AI支援開発者" />
     <meta property="og:description" content="劇場運営の現場 × AI活用で、Web制作・業務自動化を承ります" />
     <meta property="og:image" content="https://your-domain.com/ogp.png" />
     ```

3. **favicon を追加**（任意）
   - `<head>` に `<link rel="icon" href="/favicon.png" />` を追記

## デザインの調整ポイント

- **色味**: 現在は `slate`（グレー）ベース + `amber`（オレンジ）アクセント
  - もう少し落ち着いた印象にしたい場合: `amber` → `emerald` or `sky` に置換
  - もっとモダンに: `bg-slate-50` → `bg-zinc-50` に変更
- **キャッチコピー**: `<h1>` タグ内の文言を好みで調整
- **実績の機能カード**: 6個ありますが、増やしたい場合は同じ構造のdivをコピーすれば追加可能

## クラウドワークスからの動線

クラウドワークスのプロフィールに「ポートフォリオサイト」欄があるので、
公開後のURLをそこに記載すると応募時の信用度が上がります。
