# 📦 スキル集

Claude Code で使用するスキルをカテゴリ別に管理しています。

## カテゴリ一覧

| カテゴリ | 説明 | スキル数 |
|---|---|---|
| 🔧 [development/](development/) | 開発系スキル（レビュー、リファクタ、テスト、デバッグ） | 4 |
| 📝 [documentation/](documentation/) | ドキュメント系スキル（API docs、README、CHANGELOG） | 3 |
| ⚙️ [devops/](devops/) | DevOps系スキル（Docker、CI/CD、AWS） | 3 |
| 🚀 [productivity/](productivity/) | 生産性向上スキル（Git ワークフロー、プロジェクトセットアップ） | 2 |

## スキルの使い方

### 自動トリガー

Claude Code はタスクの内容に基づいて、該当するスキルを自動的に読み込みます。
`SKILL.md` の `description` フィールドが一致判定に使用されます。

### 手動呼び出し

```
/<skill-name>
```

### プロジェクトへのインストール

```bash
# シンボリックリンクで追加
ln -s /path/to/claude-skills-collection/skills/<category>/<skill-name> \
      /path/to/your-project/.claude/skills/<skill-name>
```

## 新しいスキルの追加

1. 適切なカテゴリディレクトリに新しいディレクトリを作成
2. `SKILL.md` を作成（[テンプレート](../templates/skill-template/SKILL.md) を参照）
3. 必要に応じて `references/` ディレクトリにサポートファイルを配置
