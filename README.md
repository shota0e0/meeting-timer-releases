# Meeting Timer R3 — Windows Portable

Windows 11 x64向けの、インストール不要の会議・面談・タスク用タイマーです。Ownerの個人利用を想定したPre-releaseを、Ownerの指示でPublicに置いています。誰でも閲覧・ダウンロードできます。会社やMicrosoftの公式製品ではありません。

## ダウンロード

ダウンロード・利用前に [利用条件](TERMS.md) と [Microsoft Runtimeの利用条件](MICROSOFT_RUNTIME_TERMS.txt) を確認し、同意する場合に利用してください。オープンソース成分の権利は各ライセンスに従います。

- [WindowsポータブルZIPをダウンロード](https://github.com/shota0e0/meeting-timer-releases/releases/download/v0.5.1-r3/MeetingTimer-R3-Windows-Portable.zip)
- [外部チェックサム SHA256SUMS.txt](https://github.com/shota0e0/meeting-timer-releases/releases/download/v0.5.1-r3/SHA256SUMS.txt)
- [Releaseページ](https://github.com/shota0e0/meeting-timer-releases/releases/tag/v0.5.1-r3)

ZIP：3,655,637 bytes  
SHA-256：`D9D861ACC82E79A0D2956936A8346B5F4D9D7A1DF6FFDF566F7E3AA373867D7C`

内包 `MeetingTimer-R3.exe`：9,790,464 bytes  
SHA-256：`556B57342EEE2BDF7C2D8AA22B592728516737271313D9831A0FF3F781196216`

この版はR3の同一ソースから、正規に導入したVisual Studio Community 2022で新しくビルドしたものです。仕様・機能・デザインは変更していません。新EXEでフロントエンド8試験群・Rust24件・Windows Server 2022の隔離デモによる背景効果ON/OFF各78チェックを実行しました。旧EXEのOwner実機承認を、新EXEのWindows 11実機検証として転用していません。

## 主な機能

- Outlook Classicの既定予定表を読み取り、次の会議までカウントダウン。
- 会議の15分前・5分前・開始時の通知、確認と5分後の再通知。
- 面談40分・50分／SV面談60分、ピッチ3分・5分・10分、任意の時間、ストップウォッチ。
- 自分のタスク・依頼タスクの登録、期限・確認日・履歴の管理。リマインド文面は手動確認し、自動送信しません。
- 浮遊ウィンドウ、最前面ピン、ミニ表示、背景の不透明度とぼかしの調整。

詳しい操作は [USAGE.md](USAGE.md)、変更点は [RELEASE_NOTES.md](RELEASE_NOTES.md) をご覧ください。

## 必要な環境

Windows 11 x64と、利用可能なMicrosoft Edge WebView2 Runtimeが必要です。Runtimeインストーラーは同梱していません。Outlook連携には設定済みのOutlook Classicが必要です。新しいOutlookはこの連携方式の対象外です。

ZIPを「すべて展開」してから `MeetingTimer-R3.exe` を起動します。EXEは未署名で、SmartScreen／Smart App Control等によって警告・実行拒否が出る場合があります。保護機能を解除する案内はありません。

## 制限とデータ

- Outlookは現在から次の7日間に開始する予定を対象に最大500件処理し、終日予定を除外します。全共有予定表やすべての構成への対応は保証していません。
- スリープ・ロック・完全終了中の通知は保証しません。祝日は営業日計算に含みません。
- Windowsの背景効果、DPI、複数画面等で見え方が変わる場合があります。Alt+Tabやタスクバーのネイティブ表示名が空・代替名になる場合があります。
- 設定・手動予定・タスク・再通知などをPC内へ自動保存します。保存JSONはアプリ独自の暗号化をしていません。
- Teams／メールを開く操作では宛先や文面が登録アプリ・サービスへ渡ります。全情報が絶対にPC外へ出ないという保証はしていません。
- フロントエンド資産などはEXEから回収可能です。アプリ本体のソースを公開repositoryへコミットしたものではありません。

## 第三者ライセンスとrepositoryの範囲

ZIPの `licenses/THIRD_PARTY_NOTICES.txt` に第三者の許諾・帰属表示を収録しています。必要なMPLコンポーネントのソースは `licenses/covered-source/option-ext-0.2.0` に同梱しています。アプリ本体のソースZIPではありません。

このrepositoryは配布案内と利用条件のみです。GitHubが自動生成するSource codeアーカイブも、このrepositoryの文書等をまとめたもので、アプリ本体ソースの配布ではありません。ZIPの内部チェックサムは解凍後のファイル確認用、Release Assetの外部チェックサムはZIPそのものの確認用です。
