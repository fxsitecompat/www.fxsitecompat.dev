---
title: "トップレベルウィンドウ上のデータ URL 遷移はブロックされるようになります"
date: "2017-09-20T22:02:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1331351"
      title: "Bug 1331351 - Consider blocking top level window data: URIs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1380959"
      title: "Bug 1380959 - Block toplevel data: URI navigations in Nightly and early Beta"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1398692"
      title: "Bug 1398692 - Potentially allow navigations to toplevel data: PDFs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1396798"
      title: "Bug 1396798 - Don't block top level data: URIs when loading an image"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1401895"
      title: "Bug 1401895 - Block top-level navigations to data: URIs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1403641"
      title: "Bug 1403641 - Download behaviour for data: URL seems different in FF57 compared to 55"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1403814"
      title: "Bug 1403814 - Block toplevel data: URI navigations only if openend in the browser"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1403870"
      title: "Bug 1403870 - Potentially allow navigations to data:application/json"
---
小さなデータファイルをウェブページへ埋め込めるようにする `data:` スキーマ接頭辞付きの [データ URL](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URIs) は、ブラウザー内に偽の内容を表示しつつ正規のアドレス文字列を含めることができてしまうため、フィッシング攻撃に悪用されることがしばしばあります。

こうしたセキュリティリスクを緩和するため、Firefox はトップレベルブラウザーウィンドウ内でデータ URL を開く恐れのあるページ遷移試行を近々ブロックする予定です。この変更は、バージョン 57 の時点で既に Nightly と Developer Edition を含む早期 Beta チャンネルで行われており、以下のようなシナリオに影響します。

* ページ上の URL が手動あるいはプログラムでクリックされた場合
* ページが `location.href`、`location.assign()` あるいは `location.replace()` でデータ URL を読み込もうとした場合
* ページが `window.open()` で新しいタブにデータ URL を読み込もうとした場合
* フレームコンテンツがトップレベルウィンドウもしくは新しいタブでデータ URL を読み込もうとした場合

SVG を除く画像と PDF ファイルは除外されており、それらのデータ URL 遷移は常に許可されます。

一方、以下のような操作は影響を受けません。

* ユーザーがアドレスバーにデータ URL を手入力してコンテンツを読み込もうとした場合
* ページが `<frame>` あるいは `<iframe>` にデータ URL を読み込もうとした場合
* ページが画像その他の素材にデータ URL を使用した場合

**更新**: Firefox 58 Nightly と早期 Beta チャンネルで実装が更新され、JSON ファイルも除外されるようになり、またダウンロードを実行させるデータファイルはブロックされなくなりました。
