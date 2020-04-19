---
title: "ページ読み込み中に `setTimeout()` や `setInterval()` が先送りされるようになりました"
date: "2019-02-18T17:08:00-05:00"
categories: ["dom", "networking"]
tags: []
releases: ["66", "68-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270059"
      title: "Bug 1270059 - make setTimeout() low priority during page load"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1524952"
      title: "Bug 1524952 - Low-priority setTimeout() breaks slider on bestbuy.com"
---
Firefox 66 以降、ページ読み込み中に `window.setTimeout` や `window.setInterval` メソッドで追加されたタイマーは低い優先度をつけられ、空き時間が得られるか読み込みが完了するまで先送りされるようになります。

この変更は *Google Docs* のような複雑なウェブアプリケーションのパフォーマンス向上を意図したものですが、初期化コードが適切に設計されていない場合、予期せぬ競合状態が起きる可能性があります。*Best Buy* のサイトで 1 件のリグレッションが報告され、後にサイト側で修正されましたが、Mozilla の開発者によれば、この問題はおそらくリソースアクセス順が変わったことが原因と思われます。

ウェブ上のタイマーはそれほど正確ではないということを忘れずにいましょう。ブラウザーのタブが背面にある場合など、様々な理由で [指定したよりも長く掛かる場合があります](https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/setTimeout#Reasons_for_delays_longer_than_specified)。

**更新**: [Firefox 68](https://www.fxsitecompat.dev/ja/docs/2019/xhr-load-loadend-events-are-now-deferred-during-page-load/) で XHR 最終イベントにも同様の変更が行われました。

**更新 2**: [Firefox 69](https://www.fxsitecompat.dev/ja/docs/2019/resolving-promise-returned-by-fetch-is-now-deferred-during-page-load/) で `fetch()` にも同様の変更が行われました。
