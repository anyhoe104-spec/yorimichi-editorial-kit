# note→Instagram定期実行設定（正本同期）

- 同期日時：2026-09-30 22:37 JST
- スケジュールUID：`6BureEJhAgXnWTXsjPDTzA`
- タスク名：AIと寄り道編集部 note新着→Instagram準備（毎日10:00・Lite）
- 状態：有効
- 実行頻度：毎日1回
- 実行時刻：10:00 JST
- タイムゾーン：Asia/Tokyo
- 実行モデル：Lite（`TASK_MODE_LITE`）
- 新規タスク実行：有効（`runAsNewTask: true`）
- cron：`0 0 10 * * *`
- 接続：Instagram、GitHub、Google Workspace

## 同期方針

現在のScheduleTask設定を基準に、`ai_yorimichi_master/instagram_note_monitoring_state.md` と Google Drive「AIと寄り道編集部」の状態記録を同期する。旧来の4本・6時間ごと・同一スレッド継続の記録は現行設定として扱わない。実行時は必要最小限のGitHub/Drive正本を照合し、差分または読取不能があれば投稿準備を停止する。
