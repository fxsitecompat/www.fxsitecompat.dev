---
title: "`searchParams` が `URL` 専用となりました"
date: "2015-11-28T19:24:00-08:00"
categories: ["dom"]
tags: []
versions: ["45"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1213815": "Bug 1213815 - searchParams is just on URL"
---
[`URLUtils`](https://developer.mozilla.org/ja/docs/Web/API/URLUtils) インタフェースが削除され、[`searchParams`](https://developer.mozilla.org/ja/docs/Web/API/URLUtils/searchParams) プロパティが [`Location`](https://developer.mozilla.org/ja/docs/Web/API/Location)、[`WorkerLocation`](https://developer.mozilla.org/ja/docs/Web/API/WorkerLocation)、[`HTMLAnchorElement`](https://developer.mozilla.org/ja/docs/Web/API/HTMLAnchorElement)、[`HTMLAreaElement`](https://developer.mozilla.org/ja/docs/Web/API/HTMLAreaElement) インタフェース上で利用できなくなりました。つまり、このプロパティは今後 [`URL`](https://developer.mozilla.org/ja/docs/Web/API/URL) インタフェース上でのみ利用可能となります。
