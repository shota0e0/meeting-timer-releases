# Meeting Timer R5 — Windows Portable

Windows 11 x64向け、インストール不要の会議・面談・タスク用タイマーです。Owner個人の自作アプリを、Ownerの機能確認5/5 PASSと2026年11月10日の公開承認に基づきPublic Pre-releaseとして配布します。誰でも閲覧・ダウンロードできます。会社やMicrosoftの公式製品ではありません。

## ダウンロード

利用前に[利用条件](TERMS.md)と[Microsoft Runtime条件](MICROSOFT_RUNTIME_TERMS.txt)を確認し、同意する場合に利用してください。OSS成分の権利は各ライセンスに従います。

- [R5 WindowsポータブルZIP](https://github.com/shota0e0/meeting-timer-releases/releases/download/v0.5.1-r5/MeetingTimer-R5-Windows-Portable.zip)
- [R5 ZIPのSHA256SUMS.txt](https://github.com/shota0e0/meeting-timer-releases/releases/download/v0.5.1-r5/SHA256SUMS.txt)
- [R5 Releaseページ](https://github.com/shota0e0/meeting-timer-releases/releases/tag/v0.5.1-r5)
- [以前のR4](https://github.com/shota0e0/meeting-timer-releases/releases/tag/v0.5.1-r4)／[R3](https://github.com/shota0e0/meeting-timer-releases/releases/tag/v0.5.1-r3)

ZIP：3,503,834 bytes  
SHA-256：`97877D4BF33DD3E15A64893AB23DBDFF7ED306C1757AA945C978B03A54459BA2`

内包 `MeetingTimer-R5.exe`：9,803,776 bytes  
SHA-256：`44E9821BC5B0C3E53ECFFB967DB8608E2355DBBB39E282817A9CDA6F6794C28A`

2026年11月7日に完成した同一候補ZIPを、そのまま公開しています。**ZIP内の「非公開候補」「Owner評価待ち」「正式公開未承認」等は梱包時点の記録です。今回のOwner確認・公開承認で、その公開待ち状態は解消しました。** 再ビルド・再梱包は行っていません。開発時の未実施試験まで実施済みになったという意味ではありません。利用手順は同梱README／START_HERE／RELEASE_NOTESをご確認ください。

## R5の変更

- 任意の複数行「詳細メモ」を追加。一覧右端からタスク直下へ開閉し、同じダイアログでメモを編集できます。プレーンテキストとして表示し、完了操作と独立しています。
- 完了タスクを「完了済み（件数）」へまとめ、起動時は折り畳みます。履歴内のメモ確認・編集、未完了への再開、既存の明示削除に対応し、自動削除しません。
- 既存タスクのID・期限・分類・完了状態・履歴・任意項目を保持。旧データの欠如した完了日時を架空の日時で補完しません。

R4の小型削除確認、期限順表示、同一会議の再通知重複防止と1回確認、ホームの直近タスク2件を維持しています。通常／ミニの明示切替ではAcrylicを維持する遅延改善を継承し、従来のドラッグ・位置保存・250ms処理を変更していません。

Outlook Classic予定読み取り、次会議のカウントダウン、会議前通知、面談・ピッチ・ストップウォッチ、自分／依頼タスク、浮遊表示・最前面ピン・透明度調整を利用できます。Teams／メールの文面は自動送信しません。

## 起動

Windows 11 x64と利用可能なMicrosoft Edge WebView2 Runtimeが必要です。Runtimeインストーラーは同梱していません。Outlook連携には設定済みのOutlook Classicが必要で、新しいOutlookは対象外です。

旧版をトレイの「Exit」で終了し、ZIPを別フォルダーへ「すべて展開」して `MeetingTimer-R5.exe` を起動します。通常の保存先 `%LOCALAPPDATA%\MeetingTimer` は旧版と共通です。既存データと旧版の控えを残してください。「×」はトレイへ隠す操作で、完全終了ではありません。

## 確認範囲と制限

Ownerの機能確認は5/5 PASS。開発時は既存＋R5のNode試験、Rust34/34、Windows Server2022の背景効果ON/OFF各135/135、Windows 11非管理者の実EXE内蔵自己試験135/135を確認しました。旧データの保持と実native save/load、Nodeの新規ロード再現は確認済みです。

開発環境での実Outlook再取得、新EXEの約50ms安定時間の再計測、保存後の実プロセス冷間再起動、Windows 11手動操作・新規画像による目視確認は未実施です。Ownerの5項目の内容を推測して、これらを実施済みとは扱いません。詳細は同梱R5_TEST_RESULTS.mdをご確認ください。

EXEは未署名です。SmartScreen／Smart App Control等により警告・実行拒否が生じる場合があります。端末の管理方針に従ってください。白い角・角外残像は今回修正していません。終了・スリープ・ロック中の通知、すべてのDPI／複数画面／Outlook構成は保証しません。既存の保存上限は全体1,500,000 bytes、JSON取込は1MiBです。

外部通信ゼロや完全遮断は保証しません。R4の隔離デモ監視では、帰属したWebView2 NetworkServiceの外部TCP/443接続を観測しましたが、目的・内容や予定情報の意図しない送信の有無は未確定です。R5で新しい通信監査や遮断実験は行っていません。通常起動ではOutlook予定を自動取得し、約5分ごとに更新します。Teams／メールを開く明示操作では宛先や文面が外部アプリ・サービスへ渡る場合があります。

## 第三者ライセンスとリポジトリ

ZIPの `licenses/THIRD_PARTY_NOTICES.txt` に許諾・帰属表示と関連ファイル、`licenses/covered-source` に必要なMPL対象コンポーネントのソースを収録しています。Microsoft Runtime条件は `MICROSOFT_RUNTIME_TERMS.txt` にあります。第三者資料はR4から同一内容を継承しています。

このリポジトリは配布案内・利用条件のみです。GitHubが自動生成するSource codeアーカイブにもアプリ本体ソースや内部資料は含みません。ZIP内のSHA256SUMSは展開ファイル用、Release AssetのSHA256SUMSはZIPそのものの確認用です。R3・R4の既存Releaseは維持しています。
