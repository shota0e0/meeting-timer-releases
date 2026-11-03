# Meeting Timer R4 — Windows Portable

Windows 11 x64向けの、インストール不要の会議・面談・タスク用タイマーです。Ownerの個人利用を想定したPre-releaseを、Ownerの指示で公開しています。誰でも閲覧・ダウンロードできます。会社やMicrosoftの公式製品ではありません。

## ダウンロード

ダウンロード・利用前に [利用条件](TERMS.md) と [Microsoft Runtimeの利用条件](MICROSOFT_RUNTIME_TERMS.txt) を確認し、同意する場合に利用してください。OSS成分の権利は各ライセンスに従います。

- [R4 WindowsポータブルZIP](https://github.com/shota0e0/meeting-timer-releases/releases/download/v0.5.1-r4/MeetingTimer-R4-Windows-Portable.zip)
- [R4 ZIPのSHA256SUMS.txt](https://github.com/shota0e0/meeting-timer-releases/releases/download/v0.5.1-r4/SHA256SUMS.txt)
- [R4 Releaseページ・変更点](https://github.com/shota0e0/meeting-timer-releases/releases/tag/v0.5.1-r4)
- [以前のR3 Release](https://github.com/shota0e0/meeting-timer-releases/releases/tag/v0.5.1-r3)

ZIP：3,500,981 bytes  
SHA-256：`86709610B6D7690ACF4E6EBE2E4745A67F33943C22F1ABC59952BB86C81EF238`

内包 `MeetingTimer-R4.exe`：9,799,680 bytes  
SHA-256：`ADBDF1BAB8BB8C836B7AE394C0E81544978EBF3049ADE5417B4224919FB3F8A9`

検証済みの同一R4候補パッケージを、このPre-releaseで公開しています。ZIP内の「非公開候補」「正式公開は行っていません」などは梱包時点の記録です。ZIPを再ビルド・再梱包していません。利用手順・既知の制限はZIP内のREADME/START_HERE/RELEASE_NOTESをご確認ください。R3の公開成果物は維持しています。

## R4の変更

- タスク削除をアプリ内の確認画面へ変更し、小型ウィンドウでも操作可能にしました。
- タスクを未完了の期限順、期限なし、完了済みの順で表示します。
- 同じ会議の再通知を重複登録せず、「確認した」1回で現在の通知と再通知予約を解除します。元会議不明の旧予約は個別保持です。
- ホームに優先順の未完了「自分の仕事」を最大2件表示します。
- 明示的な通常⇔ミニ切替では対象イベント1回だけAcrylicを維持し、背景の追従を改善します。通常起動とdemoの双方で有効です。移動・位置保存・250msの静止待ち・通知・タイマー・既存データ互換は維持します。

Outlook Classicの予定読み取り、次の会議までのカウントダウン、会議前通知、面談・ピッチ・ストップウォッチ、タスク・依頼管理、最前面ピン・透明度調整を利用できます。Teams/メールの文面を自動送信しません。

## 起動と条件

Windows 11 x64とMicrosoft Edge WebView2 Runtimeが必要です。Outlook連携には設定済みのOutlook Classicが必要で、新しいOutlookは対象外です。Runtimeインストーラーは同梱していません。

既存版をトレイの「Exit」で完全終了し、ZIPを別フォルダーへ「すべて展開」して `MeetingTimer-R4.exe` を開きます。通常の保存先は `%LOCALAPPDATA%\MeetingTimer` で、既存版と共通です。旧版とデータの控えを保存して試用してください。「×」はトレイへ隠す操作です。

EXEは未署名です。SmartScreen/Smart App Control等で警告・実行拒否が出る場合があります。端末の管理方針に従ってください。保護機能を解除する案内はありません。

## 通信と制限

**外部通信ゼロのアプリではありません。** 隔離した合成デモの監視でも、このアプリに帰属するWebView2 NetworkServiceの外部TCP/443接続を確認しました。接続先のドメイン・目的・通信内容、予定情報の意図しない送信の有無は未確定です。会議データの漏えいを示す証拠と同一視していません。CSPやローカル保存の説明は、WebView2内部・Windows/Outlook等の通信がないことを保証しません。

通常起動ではOutlook予定を自動取得し、その後約5分ごとに再取得します。Outlook側の通信は今回の合成デモ監視の対象外です。Teams/メールを開く明示操作では、宛先や文面が外部アプリ・サービスへ渡ります。

白い角・外周残像は今回修正していません。スリープ/ロック/完全終了中の通知、任意DPI/複数画面/すべてのOutlook構成を保証しません。新EXEでは既存フロントエンド＋R4、Rust34、Windows CIの効果ON/OFF各78＋31を確認し、Windows 11の通常/demo UI切替も隔離条件で検証しました。通常モードの実Outlook取得成功と会社PCでの最終操作感は、この新EXEでは未検証です。

## 第三者ライセンスとリポジトリ

ZIPの `licenses/THIRD_PARTY_NOTICES.txt` に許諾・帰属表示と関連ファイルを収録しています。必要なMPLコンポーネントのソースも同梱し、Microsoft Runtime条件は `MICROSOFT_RUNTIME_TERMS.txt` にあります。

このリポジトリは配布案内・利用条件のみです。GitHubの自動生成Source codeアーカイブにもアプリ本体ソース・内部資料は含みません。ZIP内のSHA256SUMSは展開ファイル用、Release Assetの外部SHA256SUMSはZIPそのものの確認用です。
