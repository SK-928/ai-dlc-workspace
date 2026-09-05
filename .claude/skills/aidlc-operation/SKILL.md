---
name: aidlc-operation
description: AI-DLC の operation フェーズを実行する。リリースと運用を記録し、次に作るものが見えたら ideation へ戻す。ユーザーが「/aidlc-operation」と入力したときや、construction を終えて運用に入るときに使用します。
---

リリースと運用を記録し続けるのが operation。終わりのないフェーズで、次に作るものが見えたら ideation へ戻る。

## 前提

- 進捗表の construction が完了であること。なければ `/aidlc-gate` へ通す

## 手順

1. リリースのたび、`aidlc-docs/operation/log.md`(なければ作る)に日付・バージョン・内容を 1 行追記し、`audit.md` にも 1 行追記する
2. 運用中の障害や気づきも log.md に追記する。修正を入れるときは construction のサイクルで行う
3. 次に作るもの・直したいものが固まったら、`/aidlc-gate` を通してから ideation へ戻る。進捗表は新しいサイクルへ更新し、`audit.md` に 1 行残す

## 出口

出口はない — 続けるか、ideation へ戻るか。戻り先は新しい feature brief から。
