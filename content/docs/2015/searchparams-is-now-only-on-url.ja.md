---
title: "`searchParams` が `URL` 専用となりました"
date: "2015-11-28T19:24:00-08:00"
categories: ["dom"]
tags: []
releases: ["45", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1213815"
      title: "Bug 1213815 - searchParams is just on URL"
---
[`URLUtils`](https://developer.mozilla.org/docs/Web/API/URLUtils) インターフェイスが削除され、[`searchParams`](https://developer.mozilla.org/docs/Web/API/URLUtils/searchParams) プロパティが [`Location`](https://developer.mozilla.org/docs/Web/API/Location)、[`WorkerLocation`](https://developer.mozilla.org/docs/Web/API/WorkerLocation)、[`HTMLAnchorElement`](https://developer.mozilla.org/docs/Web/API/HTMLAnchorElement)、[`HTMLAreaElement`](https://developer.mozilla.org/docs/Web/API/HTMLAreaElement) インターフェイス上で利用できなくなりました。つまり、このプロパティは今後 [`URL`](https://developer.mozilla.org/docs/Web/API/URL) インターフェイス上でのみ利用可能となります。
