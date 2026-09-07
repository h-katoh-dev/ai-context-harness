# Projects Registry

AI Context Harness が管理する Public プロジェクトの対応表です。

## Purpose

AI が作業対象の Public プロジェクトと Context の対応を解決できるようにします。

## Project Registry

| Project ID | GitHub Repository | Visibility | Purpose | Context |
|---|---|---|---|---|
| dev-standard | `h-katoh-dev/dev-standard` | Public | 開発標準化 | `projects/dev-standard/` |
| architecture-playbook | `h-katoh-dev/architecture-playbook` | Public | システムアーキテクチャ学習・判断基準 | `projects/architecture-playbook/` |

## Private Project Context

個人の職務経歴、転職活動、投資、取引、事業アイデア、個人開発などの Private プロジェクトは、この Public Registry に登録しません。

Private プロジェクトの Context は、別の Private リポジトリまたはローカル環境で管理します。

## AI Resolution Rule

1. 作業対象の GitHub リポジトリを特定する。
2. この表から対応する Public Project ID を解決する。
3. `projects/<Project ID>/CONTEXT.md` を読む。
4. `projects/<Project ID>/STATE.md` を読む。
5. 必要に応じて `DECISIONS.md` を読む。
6. 実際の対象リポジトリのコード・README・Issues 等を最新の事実として扱う。
7. Context の保存・更新時は `global/repository-policy.md` の公開境界を適用する。

## Repository-side Pointer

各 Public 対象リポジトリ側には、可能であればルートに `AI_CONTEXT.md` を置きます。

- Project ID
- AI Context Harness の対応パス
- Context との関係

これにより、対象リポジトリ → Context Harness → 継続状態を解決できます。
