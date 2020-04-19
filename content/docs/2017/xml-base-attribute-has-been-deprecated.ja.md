---
title: "`xml:base` 属性が廃止予定となりました"
date: "2017-02-21T20:16:00-05:00"
categories: ["misc"]
tags: []
releases: ["53", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=903372"
      title: "Bug 903372 - Remove support for xml:base"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1340926"
      title: "Bug 1340926 - Add telemetry for xml:base attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/1JDnJWefe1E/discussion"
      title: "Intent to unship: xml:base attribute"
---
HTML の [`<base>`](https://developer.mozilla.org/docs/Web/HTML/Element/base) 要素と似た [`xml:base`](https://www.w3.org/TR/xmlbase/) 属性が廃止予定となり、近い将来削除されることとなりました。これは何年も前に仕様から削除されており、現時点で他のどのブラウザーも対応していません。

**更新**: この属性対応は [Firefox 66](https://www.fxsitecompat.dev/ja/docs/2018/xml-base-attribute-is-no-longer-supported/) で削除されました。
