# Meeting Timer R3 | Windows Portable v0.5.1

タグ `v0.5.1-r3`／Pre-release。

Windows 11 x64向けのインストール不要版です。Outlook Classic予定読み取り、次会議までのカウントダウン・会議前通知、面談／ピッチ用タイマー、自分／依頼タスク管理、浮遊ウィンドウ・最前面表示に対応します。

ダウンロード・利用前に [利用条件](https://github.com/shota0e0/meeting-timer-releases/blob/v0.5.1-r3/TERMS.md) と [Microsoft Runtime条件](https://github.com/shota0e0/meeting-timer-releases/blob/v0.5.1-r3/MICROSOFT_RUNTIME_TERMS.txt) を確認し、同意する場合に利用してください。OSS成分の権利は各ライセンスに従います。


Owner個人の自作アプリのPublic Pre-releaseです。会社やMicrosoftの公式製品ではありません。

## R3の変更

- 起動直後に左上へ薄く残る標準ウィンドウタイトルへの対策として、ネイティブのタイトル文字列をウィンドウ生成時から空にしました。
- 最前面の菱形を細線のピンへ統一しました。ONはミント色、OFFはグレーで、状態の説明と従来のクリック領域を維持しています。
- R2で対策した標準ボタンの重複表示への制御を維持しています。

Outlook Classic予定取得、会議カウントダウン・通知、面談／ピッチタイマー、タスク・保存データ、ドラッグ、グラス効果・透明度・既存レイアウトは、この限定修正で別方式へ作り直していません。

## 今回の同一ソース再ビルド

R3の同じ39ソースと固定依存関係から、Visual Studio Community 2022を正規導入したWindows Server 2022で新しくビルドしました。仕様・機能・デザインの変更はありません。既存EXEとは別バイナリで、旧版の実機承認を引き継いだとは扱いません。

この新EXEで既存フロントエンド8試験群・Rust24件・隔離デモの背景効果ON/OFF各78チェックが成功しました。Windows 11実機の見た目や実予定取得を今回再検証したものではありません。

EXE：9,790,464 bytes  
SHA-256：`556B57342EEE2BDF7C2D8AA22B592728516737271313D9831A0FF3F781196216`

同梱文書・許諾・NOTICE・必要な第三者ソースを継承しています。実データ・ユーザープロファイル・内部記録・アプリ本体ソースは同梱していません。利用は [利用条件](https://github.com/shota0e0/meeting-timer-releases/blob/v0.5.1-r3/TERMS.md) とMicrosoft Runtime条件を確認して行ってください。

## 既知の制限

- Windows 11 x64と利用可能なWebView2 Runtimeが必要です。Runtimeインストーラーは同梱しません。
- Outlook連携は設定済みのOutlook Classicの既定予定表が対象です。新しいOutlook、全共有予定表、あらゆるプロファイル構成への対応を保証しません。
- 終了中・スリープ中・ロック中の通知は保証しません。祝日を含む営業日判定はありません。
- ぼかしや透明感はWindows環境によって異なります。Alt+Tab／タスクバーのネイティブ表示名は空・代替名になる場合があります。
- EXEは未署名です。SmartScreen／Smart App Control等による警告・実行拒否が起こる場合があります。端末の既存の方針に従ってください。
- EXEには依存コード由来のビルド時のパス文字列や検証用資産が含まれる場合があります。


ZIP：3,655,637 bytes / SHA-256 `D9D861ACC82E79A0D2956936A8346B5F4D9D7A1DF6FFDF566F7E3AA373867D7C`。AssetsはWindows ZIPと外部SHA256SUMS.txtです。
