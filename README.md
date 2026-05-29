# Task Manager

Claude Code エージェントが毎朝 9時（JST）に自動で以下を実行します：

- `tasks.json` を読み込み、締切・優先度を分析
- 今日やるべきタスクを割り出し
- `reports/YYYY-MM-DD.md` に日次レポートを生成・コミット

## tasks.json の書き方

| フィールド | 説明 | 値 |
|---|---|---|
| `id` | タスクID（ユニーク） | 整数 |
| `title` | タスク名 | 文字列 |
| `description` | 詳細 | 文字列 |
| `deadline` | 締切日 | `YYYY-MM-DD` |
| `priority` | 優先度 | `high` / `medium` / `low` |
| `status` | ステータス | `todo` / `in_progress` / `done` |
| `progress` | 進捗率 | `0` 〜 `100` |
