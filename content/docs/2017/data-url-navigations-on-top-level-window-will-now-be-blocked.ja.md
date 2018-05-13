---
title: "トップレベルウィンドウ上のデータ URL 遷移はブロックされるようになりました"
date: "2017-11-15T10:31:00-05:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["59"]
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
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1415612"
      title: "Bug 1415612 - Allow all plain text types when navigating top-level data URIs"
    - url: "https://blog.mozilla.org/security/2017/11/27/blocking-top-level-navigations-data-urls-firefox-58/"
      title: "Blocking Top-Level Navigations to data URLs for Firefox 58"
aliases:
    - "/ja/docs/2017/data-url-navigations-on-top-level-window-will-be-blocked/"
---
小さなデータファイルをウェブページへ埋め込めるようにする `data:` スキーマ接頭辞付きの [データ URL](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs) は、ブラウザー内に偽の内容を表示しつつ正規のアドレス文字列を含めることができてしまうため、フィッシング攻撃に悪用されることがしばしばあります。

こうしたセキュリティリスクを緩和するため、Firefox はトップレベルブラウザーウィンドウ内でデータ URL を開く恐れのあるページ遷移試行を近々ブロックする予定です。この変更は以下のようなシナリオに影響します。

* ページ上の URL が手動あるいはプログラムでクリックされた場合
* ページが `location.href`、`location.assign()` あるいは `location.replace()` でデータ URL を読み込もうとした場合
* ページが `window.open()` で新しいタブにデータ URL を読み込もうとした場合
* フレームコンテンツがトップレベルウィンドウもしくは新しいタブでデータ URL を読み込もうとした場合

SVG を除く画像と、PDF、JSON、プレーンテキストファイルは除外されており、それらのデータ URL 遷移は常に許可されます。

一方、以下のような操作は影響を受けません。

* ユーザーがアドレスバーにデータ URL を手入力してコンテンツを読み込もうとした場合
* ページが `<frame>` あるいは `<iframe>` にデータ URL を読み込もうとした場合
* ページが画像その他の素材にデータ URL を使用した場合
* ページがデータファイルのダウンロードを誘発した場合
