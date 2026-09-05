---
name: aidlc-init
description: AI-DLC の土台(aidlc-docs/ の作業棚・進捗状態・監査台帳)をカレントプロジェクトに初期化する。ユーザーが「/aidlc-init」と入力したときや、AI-DLC の記録基盤を整えたいときに使用します。
---

AI-DLC の機構の土台だけを作る。

## 作るもの

```
aidlc-docs/
├── aidlc-state.md   ← 進捗表。続きからの再開用
├── audit.md         ← 全判断の時刻付き台帳
├── ideation/
├── inception/
├── construction/
└── operation/
```

## 手順

1. `aidlc-docs/` が既にあれば初期化せず、中身を報告して中断する
2. リポジトリを軽く調べ、greenfield(新規)/ brownfield(既存コードあり)を判定する
3. 上記の構成を作る。`aidlc-state.md` の初期内容:

```markdown
# aidlc-state

- project: <プロジェクト名>
- workspace: <greenfield|brownfield>(<根拠一言>)
- updated: <ISO 8601>

## 進捗表

| phase | stage | status |
|---|---|---|
| ideation | — | 未着手 |
| inception | — | 未着手 |
| construction | — | 未着手 |
| operation | — | 未着手 |
```

4. `audit.md` の初期内容:

```markdown
# audit

- <ISO 8601> init workspace=<判定>
```

初期化後の運用は、プロジェクト CLAUDE.md の「AI-DLC の運用」に従う。
