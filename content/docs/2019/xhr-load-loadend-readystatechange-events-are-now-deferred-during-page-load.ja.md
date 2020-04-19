---
title: "ページ読み込み中に XHR `load`、`loadend`、`readystatechange` イベントが先送りされるようになりました"
date: "2019-06-09T03:18:00-04:00"
categories: ["dom", "networking"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1538364"
      title: "Bug 1538364 - Consider firing the load/loadend/final readyState events for XHR later during page load (after page load event if possible)"
---
Firefox 68 以降、ページ読み込み中に開始された `XMLHttpRequest` の最終イベントは、空き時間が得られるか読み込みが完了するまで先送りされるようになります。これらのイベントには、`readyState` プロパティが `4` になった後で呼び出される `load`、`loadend`、`readystatechange` が含まれます。

[Firefox 66](https://www.fxsitecompat.dev/en-CA/docs/2019/settimeout-and-setinterval-are-now-deferred-during-page-load/) で `setTimeout()` に対して行われた変更と同じく、この変更は *Gmail* のような複雑なウェブアプリケーションのパフォーマンス向上を意図したものですが、初期化コードが適切に設計されていない場合、予期せぬ競合状態が起きる可能性があります。

**更新**: [Firefox 69](https://www.fxsitecompat.dev/ja/docs/2019/resolving-promise-returned-by-fetch-is-now-deferred-during-page-load/) で `fetch()` にも同様の変更が行われました。
