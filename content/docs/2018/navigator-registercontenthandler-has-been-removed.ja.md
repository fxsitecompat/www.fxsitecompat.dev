---
title: "`navigator.registerContentHandler()` が削除されました"
date: "2018-05-09T22:43:00-04:00"
categories: ["dom"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460481"
      title: "Bug 1460481 - Disable registerContentHandler() in stable"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jeTDLz38_RE/discussion"
      title: "Intent to unship: navigator.registerContentHandler()"
---
[Firefox 59](https://www.fxsitecompat.com/ja/docs/2018/navigator-registercontenthandler-has-been-deprecated/) 以降廃止予定となっていた [`navigator.registerContentHandler`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/registerContentHandler) メソッドが Firefox 62 で削除されました。これは HTML 仕様で標準化されていたものの、他のどのブラウザーもこの機能に対応しておらず、Firefox の実装も標準に準拠していませんでした。ウェブフィードの人気が低下していることから、削除に伴うリスクは少ないはずです。
