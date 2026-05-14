# 🧠 Claude Skills Collection

Claude Code で使用するスキル、エージェント、ルール、コマンド、テンプレートを体系的に管理するコレクションです。

## 📁 フォルダ構成

```
├── skills/          # スキル集（SKILL.md ベース）
│   ├── development/     # 開発系スキル
│   ├── documentation/   # ドキュメント系スキル
│   ├── devops/          # DevOps系スキル
│   └── productivity/    # 生産性向上スキル
│
├── agents/          # エージェント定義
├── rules/           # ルール集（言語・トピック別）
├── commands/        # カスタムスラッシュコマンド
├── templates/       # テンプレート集
└── docs/            # ドキュメント・ガイド
```

## 🚀 クイックスタート

### 1. リポジトリをクローン

```bash
git clone https://github.com/<your-username>/claude-skills-collection.git
```

### 2. プロジェクトにスキルをインストール

#### 方法A: シンボリックリンク（推奨）

プロジェクトの `.claude/skills/` にシンボリックリンクを作成：

```bash
# 特定のスキルをリンク
ln -s /path/to/claude-skills-collection/skills/development/code-review \
      /path/to/your-project/.claude/skills/code-review

# カテゴリごとリンク
ln -s /path/to/claude-skills-collection/skills/development \
      /path/to/your-project/.claude/skills/development
```

#### 方法B: ファイルコピー

必要なスキルをプロジェクトに直接コピー：

```bash
cp -r /path/to/claude-skills-collection/skills/development/code-review \
      /path/to/your-project/.claude/skills/
```

#### 方法C: エージェント・ルールのインストール

```bash
# エージェント定義をコピー
cp /path/to/claude-skills-collection/agents/reviewer.md \
   /path/to/your-project/.claude/agents/

# ルールをコピー
cp /path/to/claude-skills-collection/rules/javascript.md \
   /path/to/your-project/.claude/rules/
```

### 3. 新しいスキルを作成

テンプレートを使って新しいスキルを作成：

```bash
cp -r templates/skill-template skills/<category>/<new-skill-name>
# SKILL.md を編集して内容を記述
```

## 📖 ドキュメント

| ドキュメント | 説明 |
|---|---|
| [導入ガイド](docs/getting-started.md) | 初めての方向けセットアップ手順 |
| [スキル作成ガイド](docs/how-to-create-skill.md) | スキルの作り方 |
| [エージェント作成ガイド](docs/how-to-create-agent.md) | エージェントの作り方 |
| [ベストプラクティス](docs/best-practices.md) | 効果的な活用方法 |
| [FAQ](docs/faq.md) | よくある質問 |

## 📦 コンテンツ一覧

### スキル

| カテゴリ | スキル名 | 説明 |
|---|---|---|
| 🔧 開発 | [code-review](skills/development/code-review/) | コードレビューの自動化 |
| 🔧 開発 | [refactoring](skills/development/refactoring/) | リファクタリング支援 |
| 🔧 開発 | [testing](skills/development/testing/) | テストコード生成 |
| 🔧 開発 | [debugging](skills/development/debugging/) | デバッグ支援 |
| 📝 ドキュメント | [api-docs](skills/documentation/api-docs/) | API ドキュメント生成 |
| 📝 ドキュメント | [readme-generator](skills/documentation/readme-generator/) | README 自動生成 |
| 📝 ドキュメント | [changelog](skills/documentation/changelog/) | CHANGELOG 生成 |
| ⚙️ DevOps | [docker](skills/devops/docker/) | Dockerfile / Compose 作成 |
| ⚙️ DevOps | [ci-cd](skills/devops/ci-cd/) | CI/CD パイプライン構築 |
| ⚙️ DevOps | [aws](skills/devops/aws/) | AWS インフラ構築支援 |
| 🚀 生産性 | [git-workflow](skills/productivity/git-workflow/) | Git ワークフロー最適化 |
| 🚀 生産性 | [project-setup](skills/productivity/project-setup/) | プロジェクト初期セットアップ |

### エージェント

| エージェント | 説明 |
|---|---|
| [reviewer](agents/reviewer.md) | コードレビュー専門 |
| [frontend-dev](agents/frontend-dev.md) | フロントエンド開発 |
| [backend-dev](agents/backend-dev.md) | バックエンド開発 |
| [devops](agents/devops.md) | DevOps・インフラ |

### ルール

| ルール | 対象 |
|---|---|
| [javascript](rules/javascript.md) | JavaScript / TypeScript |
| [python](rules/python.md) | Python |
| [css](rules/css.md) | CSS / スタイリング |
| [security](rules/security.md) | セキュリティ |

## 🤝 コントリビューション

新しいスキルやエージェントの追加は大歓迎です！

1. このリポジトリをフォーク
2. 新しいブランチを作成 (`git checkout -b feature/new-skill`)
3. テンプレートを使ってスキルを追加
4. コミット & プッシュ
5. プルリクエストを作成

## 📄 ライセンス

MIT License - 詳細は [LICENSE](LICENSE) を参照してください。
