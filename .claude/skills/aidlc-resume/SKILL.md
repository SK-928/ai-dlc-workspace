---
name: aidlc-resume
description: AI-DLC の土台(aidlc-docs/)を読んで現在地を報告し、続きから始める。ユーザーが「/aidlc-resume」と入力したときや、AI-DLC 管理下のプロジェクトでセッションを開始するときに使用します。
---

aidlc-docs/ から現在地を復元し、続きから始める。

## 手順

1. `aidlc-docs/` がなければ未初期化として報告し、中断する
2. `aidlc-state.md` から project / workspace / 進捗表を読む
3. `audit.md` の末尾から直近の判断を読む
4. フェーズディレクトリの実態と進捗表を突き合わせる。ズレていれば `aidlc-state.md` を実態に合わせ、`audit.md` に 1 行追記する
5. 現在地が construction なら、design.md の共通契約・tasks.md・次のタスクの `construction/design-T<N>.md` を読む
6. 次を報告し、ユーザーの指示を仰ぐ:
   - 現在地(どのフェーズのどこか)
   - 直近の判断(audit の末尾)
   - 次にやることの提案
