# AI Context Harness

複数のAIチャット・開発セッション・プロジェクト間で、作業コンテキストを再利用するための軽量な管理基盤。

## Purpose

AIによる開発作業では、チャットをまたぐたびに「現在地・前提・判断理由・次の作業」を説明し直す必要があります。

AI Context Harness は、これらを構造化して保存し、作業の再開とAIエージェント間のコンテキスト共有を容易にします。

## Design Principles

- **Current state first** — 現在地と次の一手を明確にする
- **Decision traceability** — 重要な判断理由を残す
- **Minimum context** — 必要な情報だけを読み込む
- **Public / Private separation** — 公開可能な知識と個人・機密コンテキストを分離する
- **Human-in-the-loop** — 人間の確認が必要な箇所を明示する

## Core Structure

```text
ai-context-harness/
├─ README.md
├─ AGENTS.md
├─ AI_CONTEXT.md
├─ global/
│  ├─ ai-work-policy.md
│  ├─ git-work-policy.md
│  ├─ model-and-token-policy.md
│  ├─ principles.md
│  └─ repository-policy.md
├─ projects/
│  ├─ README.md
│  ├─ _template/
│  │  ├─ CONTEXT.md
│  │  ├─ STATE.md
│  │  └─ DECISIONS.md
│  ├─ dev-standard/
│  └─ architecture-playbook/
└─ prompts/
   └─ session-handoff.md
```

## Project Context Model

- `CONTEXT.md` — 長期的に有効な前提・制約・関連情報
- `STATE.md` — 現在の進捗・未完了作業・次のアクション
- `DECISIONS.md` — 重要な意思決定と理由

## Public / Private Boundary

このリポジトリは Public です。

個人情報、認証情報、秘密情報、顧客情報、勤務先の非公開情報、個人プロジェクトの詳細な継続コンテキストは保存しません。

個人的・機密性のある Context は、別の Private リポジトリまたはローカル環境で管理します。

## Example Projects

現在は公開可能な開発標準・アーキテクチャ学習プロジェクトのみをサンプルとして登録しています。

## Session Handoff

`prompts/session-handoff.md` を利用すると、新しいAIセッションから対象プロジェクトの Context / State を確認し、作業を再開できます。
