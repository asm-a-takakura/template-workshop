# coen エンジニアコミュニティ — ポートフォリオテンプレート

coen エンジニアコミュニティのワークショップ用ポートフォリオテンプレートです。
`data/portfolio.ts` を編集するだけで、自分だけのポートフォリオサイトが完成します。

**技術スタック:** Next.js / React / TypeScript / Tailwind CSS / Vercel

---

## セットアップ

```bash
npm install      # 依存パッケージのインストール
npm run dev      # 開発サーバー起動 → http://localhost:3000
npm run build    # 本番ビルド確認
```

---

## 使い方

### 1. `data/portfolio.ts` を編集する（必須）

自分の情報を書き換えるだけでポートフォリオが完成します。

```ts
export const profile = {
  name: "あなたの名前",
  role: "Webエンジニア",
  bio: "自己紹介文をここに書いてください。",
  avatarUrl: "/images/avatar.jpg",
};

export const skills = [
  { name: "JavaScript", level: "学習中" },
  { name: "React", level: "学習中" },
];

export const projects = [
  {
    title: "プロジェクト名",
    description: "どんなものを作ったか、簡単な説明",
    techStack: ["Next.js", "TypeScript"],
    url: "https://github.com/あなたのユーザー名/リポジトリ名",
  },
];

export const contact = {
  github: "https://github.com/あなたのユーザー名",
  email: "あなたのメールアドレス（任意）",
};
```

### 2. プロフィール画像を差し替える（任意）

`public/images/avatar.jpg` を自分の写真に差し替えてください。
ファイル名を変えた場合は `portfolio.ts` の `avatarUrl` も更新してください。

### 3. デザインをカスタマイズする（任意・挑戦枠）

`src/components/` 内のファイルを編集してデザインを変更できます。

---

## プロジェクト構成

```
├── data/
│   └── portfolio.ts           # ★ メイン編集ファイル
├── public/
│   └── images/                # プロフィール画像を置く場所
├── src/
│   ├── app/
│   │   ├── layout.tsx         # 共通レイアウト
│   │   ├── page.tsx           # トップページ
│   │   └── globals.css        # グローバルスタイル
│   └── components/
│       ├── Profile.tsx        # プロフィールセクション
│       ├── Skills.tsx         # スキル一覧セクション
│       ├── Projects.tsx       # プロジェクト一覧セクション
│       └── Contact.tsx        # 連絡先セクション
```

---

## ブランチ運用

| ブランチ | 用途 |
|:---|:---|
| `main` | 公開用（直接コミット禁止） |
| `feature/名前-portfolio` | 各自の作業ブランチ |

```bash
# 作業ブランチを作成（名前は自分の名前に変えてください）
git checkout -b feature/tanaka-portfolio
```

作業が完了したら `main` への Pull Request を作成してください。

---

## デプロイ

PR が `main` にマージされると Vercel が自動でデプロイします。
手動デプロイしたい場合は [Vercel](https://vercel.com) にサインインし、このリポジトリをインポートしてください。

---

## 困ったときは

- coen エンジニアコミュニティの Slack チャンネルで質問
- 運営メンバーに直接連絡
- エラーが出た場合はスクリーンショットと一緒に共有してください
