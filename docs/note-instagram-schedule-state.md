# note→Instagram定期実行設定（正本同期）

- 同期日時：2026-10-06 11:02 JST
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

GitHub `anyhoe104-spec/ai_yorimichi_master`の`main`ブランチを唯一のGitHub正本として扱う。`instagram_note_monitoring_state.md` と対象資料の処理済み判定・公開状態・投稿内容は、必ず`main`から読み取る。`anyhoe104-spec/yorimichi-editorial-kit`はこのルーティンの照合対象に含めない。Google Drive「AIと寄り道編集部」はミラー（照合・バックアップ・既存素材取得用）であり、Driveだけの内容を正本として確定しない。Driveとの差分があればGitHub`main`を優先し、Driveを同期対象とする。ただしGitHub`main`の必要資料が読めない、または対象資料が`main`にない場合は投稿準備を停止して差分・読取不能・未処理状態を報告する。
