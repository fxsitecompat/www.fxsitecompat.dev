---
title: "`FileReaderSync` が Service Worker 内で使用できなくなりました"
date: "2018-05-08T19:17:00-04:00"
categories: ["dom"]
tags: []
versions: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1405552"
      title: "Bug 1405552 - Do not expose FileReaderSync to serviceworkers, to match the spec."
---
Firefox 61 以降、現行の File API 仕様に従い、[`FileReaderSync`](https://developer.mozilla.org/docs/Web/API/FileReaderSync) API は専用および共有 Worker 内のみで使用可能となり、Service Worker 内では使用不可となりました。非同期の [`FileReader`](https://developer.mozilla.org/docs/Web/API/FileReader) API を代わりに使ってください。
