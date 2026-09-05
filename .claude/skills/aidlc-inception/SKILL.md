---
name: aidlc-inception
description: AI-DLC の inception フェーズを実行する。feature brief を要件・設計・計画に展開し、承認を得る。ユーザーが「/aidlc-inception」と入力したときや、ideation を終えて inception に進むときに使用します。
---

feature brief を要件・設計・計画の 3 文書に展開し、承認を得るまでが inception。

## 前提

- `aidlc-docs/ideation/feature-brief.md` があり承認済みであること。なければ `/aidlc-ideation` へ戻す
- 進捗表の ideation が完了でなければ、先に `/aidlc-gate` へ通す

## 手順

1. feature brief を読む。`aidlc-docs/inception/` に既存の成果物があれば続きから始める(`.backup` は参照しない)
2. brownfield なら、既存コードを軽く調べて制約を書き残す
3. requirements.md を作る — brief をテスト可能な要件に分解し、番号を振る(F1, F2, …)
4. design.md を作る — 構成と技術。要件を満たすのに必要な分だけ書く
5. tasks.md を作る — 1 サイクルで完了できる大きさの単位に割る。id(T1, T2, …)と依存関係を書く
6. 1 文書完成ごとに承認を仰ぎ、通ったら次へ進む。決定・承認・成果物の配置はそれぞれ `audit.md` に 1 行ずつ追記する
7. 決められない項目は、仮定・トリガー・期限を添えて記録する(ideation と同じ)

## 出口

requirements.md・design.md・tasks.md がすべて承認済みであること。次は `/aidlc-gate` で点検してから construction へ進む。
