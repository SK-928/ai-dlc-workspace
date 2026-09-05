---
name: aidlc-construction
description: AI-DLC の construction フェーズを実行する。tasks.md のタスクを 1 サイクルずつ実装・テストして完成させる。ユーザーが「/aidlc-construction」と入力したときや、inception を終えて construction に進むときに使用します。
---

tasks.md のタスクを 1 サイクルずつ実装・テストし、全単位を完成させるまでが construction。

## 前提

- `aidlc-docs/inception/` の 3 文書が承認済みであること。なければ `/aidlc-inception` へ戻す
- 進捗表の inception が完了でなければ、先に `/aidlc-gate` へ通す

## サイクル(タスク 1 つぶん)

1. tasks.md から、依存が解けた次の未完了タスクを選ぶ
2. 実装する。design.md に従い、そのタスクの分だけをやる(先回りして作らない)
3. 検証する。tasks.md の検証列(タスクごとに定義)を実行し、通らなければ直してから次へ。手動確認・ユーザーへの提示はその結果を記録する
4. tasks.md の当該タスクを完了に更新し、`audit.md` に 1 行追記する(実装と検証結果)
5. 全タスクが完了するまで繰り返す
6. 完了後、`aidlc-docs/construction/report.md` に実装内容とテスト結果をまとめる

最初のサイクルは、端から端まで動く最小の流れ(骨格)を通す。コードはリポジトリの通常の場所へ置き、aidlc-docs には記録だけを置く。

## 出口

全タスク完了・各タスクの検証列すべて通過・report.md があること。次は `/aidlc-gate` で点検してから operation へ進む。
