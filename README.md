# AI Context Harness

複数のAIチャット・プロジェクト間で、作業コンテキストを再利用するための共通基盤。

## 基本方針

- GitHub: プロジェクト固有の詳細なコンテキスト・進捗・意思決定を管理
- ChatGPT Memory: 長期的に有効な共通情報のみを管理
- AIは作業開始時に必要なコンテキストを読み、作業終了時に状態を更新する

## 構造

```text
ai-context-harness/
├─ README.md
├─ AGENTS.md
├─ global/
│  ├─ preferences.md
│  └─ principles.md
├─ projects/
│  └─ _template/
│     ├─ CONTEXT.md
│     ├─ STATE.md
│     └─ DECISIONS.md
├─ schemas/
└─ scripts/
```

`_template` は1つだけ保持し、実際のプロジェクトごとに `projects/<project-name>/` を作成する。
