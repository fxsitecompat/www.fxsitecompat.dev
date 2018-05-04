---
title: "`File.lastModifiedDate` が廃止されました"
date: "2018-05-04T13:53:00-04:00"
categories: ["dom"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1458883"
      title: "Bug 1458883 - Get rid of File.lastModifiedDate"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/l-WY9qvfUNg/discussion"
      title: "Intent to unship: File.lastModifiedDate"
---
[Firefox 49 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2016/file-lastmodifieddate-has-been-deprecated/) 非標準の [`File.prototype.lastModifiedDate`](https://developer.mozilla.org/ja/docs/Web/API/File/lastModifiedDate) プロパティが Firefox 61 で削除されました。Mozilla の Telemetry によれば、これは現在 0.01% のページで使用されています。代わりに標準の [`lastModified`](https://developer.mozilla.org/ja/docs/Web/API/File/lastModified) プロパティを使ってください。
