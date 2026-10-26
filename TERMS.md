# 利用条件とMicrosoft成分について

この案内と、リンク先・ZIP同梱の各ライセンスを読み、適用される条件に同意する場合にのみダウンロード・利用してください。条件に同意できない場合は利用しないでください。

## 対象を分けた取扱い

このアプリは会社やMicrosoftの公式製品ではありません。Public repositoryからダウンロードできる状態で提供しますが、アプリ本体のソースを公開するものではなく、アプリやMicrosoftのコードについて無制限の改変・再配布権を与えるものではありません。

ZIPに含まれるMIT、Apache、BSD、Unicode、MPL等の第三者成分の権利は、それぞれのライセンスに従います。本書はオープンソース成分に認められたソース入手・改変・再配布その他の権利を取り消したり制限したりしません。必要なMPLコンポーネントのソースはZIP内 `licenses/covered-source/option-ext-0.2.0` にあります。

## Microsoftの再配布可能コード

Microsoft Visual C++ Runtimeに由来する成分については、[Microsoft Runtimeの利用条件全文](MICROSOFT_RUNTIME_TERMS.txt) と、適用されるMicrosoftの条件に同意して利用する必要があります。少なくとも次の保護を当該Microsoft成分に適用します。

- 許諾された範囲で使用し、技術的制限を回避せず、違法な利用をしないこと。
- Microsoftや供給者の権利表示を削除・変更しないこと。
- 逆コンパイル・逆アセンブル・ソース取得等は、適用法または該当オープンソースの条件が認める場合を除き行わないこと。オープンソースの例外を本書で制限しません。
- Microsoftの商標を、Microsoftが本アプリを提供・推奨していると誤認させる形で使わないこと。
- この案内によって、ランタイムを単独提供したり、Microsoft成分を第三者へ再配布したりする追加権限を得るものではないこと。別途の再配布には、その権限と適用条件の充足が必要です。
- 適用される輸出規制を守ること。保証・責任制限・法定の消費者権利は、Microsoft原文と適用法に従うこと。

Microsoft成分の利用者・再配布者には、適用される原文条件と同等以上に当該コードを保護する条件への同意を求めます。上の要約だけで原文を置き換えるものではありません。この案内自体は、開発者や再配布者のMicrosoftライセンス資格を新たに付与するものでもありません。

WebView2 SDK LoaderにはZIP内 `licenses/microsoft-webview2/LICENSE.txt` と `NOTICE.txt` の条件があります。Visual C++ Runtimeの条件を、別の許諾で提供されるWebView2 Loaderやオープンソース成分へ一律に拡張しません。WebView2 RuntimeインストーラーはこのZIPに含みません。

## 原文と表示方法

`MICROSOFT_RUNTIME_TERMS.txt` はMicrosoft公式DOCXの本文paragraph文字列を順序どおり抽出したもので、翻訳や実質的な編集はしていません。文書のレイアウト・番号を含む原文は、[公式Visual C++ Runtime利用条件DOCX](https://visualstudio.microsoft.com/wp-content/uploads/2021/09/Visual-C-Runtime-2015-2022-License-1.docx) を参照してください。

開発者の再配布条件については、[Visual Studio Community 2022公式条件](https://visualstudio.microsoft.com/wp-content/uploads/2021/11/Visual-Studio-2022-Community-License-EN.docx) のDistributable Code等、適用される原文条件に従います。Runtime利用条件だけを開発者の再配布権の証明とは扱いません。
