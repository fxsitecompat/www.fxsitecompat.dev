---
title: "ページ読み込み中に `fetch()` によって返された `Promise` の解決が先送りされるようになりました"
date: "2019-06-15T21:58:00-04:00"
categories: ["dom", "networking"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1538516"
      title: "Bug 1538516 - Resolve the Promise returned by fetch() later during page loads"
---
Firefox 69 以降、ページ読み込み中に `fetch()` によって返された `Promise` は、空き時間が得られるか読み込みが完了するまで解決されなくなります。[`setTimeout()`](https://www.fxsitecompat.dev/ja/docs/2019/settimeout-and-setinterval-are-now-deferred-during-page-load/) と [`XMLHttpRequest`](https://www.fxsitecompat.dev/ja/docs/2019/xhr-load-loadend-readystatechange-events-are-now-deferred-during-page-load/) に対して最近行われた変更と同じく、この変更はページ読み込み速度の改善を意図したものですが、初期化コードが適切に設計されていない場合、予期せぬ競合状態が起きる可能性があります。あなたのサイトが該当する場合はテストを行うようにしてください。
