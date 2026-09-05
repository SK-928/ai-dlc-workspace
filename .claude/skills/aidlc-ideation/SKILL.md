---
name: aidlc-ideation
description: AI-DLC の ideation フェーズを実行する。何を作るかを1枚の文書(feature brief)にまとめ、承認を得る。ユーザーが「/aidlc-ideation」と入力したときや、ideation フェーズを開始するときに使用します。
---

何を作るかを1枚の文書(feature brief)にまとめ、承認を得るまでが ideation。

## 手順

1. `aidlc-docs/ideation/` に feature-brief.md があれば読み、続きから始める(`.backup` は参照しない)
2. ユーザーとの対話で次を埋める:
   - 誰の・何を解決するか
   - 使い方の核(最主要の流れを 1 つ)
   - 成功条件(どうなったら完成か)
   - スコープ外(今回やらないこと)
3. 決められない項目は、雑に答えたり空欄にせず、仮定・トリガー・期限を添えて記録する
4. 質問への回答や決定のたびに `audit.md` に 1 行追記する
5. 全項目埋まったらユーザーの承認を仰ぐ
6. 承認されたら `aidlc-docs/ideation/feature-brief.md` に置き、進捗表の ideation を「着手」に更新する

## 出口

feature-brief.md が承認済みであること。次は `/aidlc-gate` で点検してから inception へ進む。
