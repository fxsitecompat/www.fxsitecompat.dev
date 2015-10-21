---
title: "`MozConnection` インタフェースがグローバルオブジェクトでなくなりました"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=960945": "Bug 960945 – MozConnection should be NoInterfaceObject"
---
現在は `MozConnection` として接頭辞付きの [`Connection`](https://developer.mozilla.org/ja/docs/Web/API/Connection) インタフェースが、[`window`](https://developer.mozilla.org/ja/docs/Web/API/window) 上にグローバルオブジェクトとして公開されなくなりました。[Network Information API](https://developer.mozilla.org/ja/docs/Web/API/Network_Information_API) を活用するには [`navigator.mozConnection`](https://developer.mozilla.org/ja/docs/Web/API/navigator.mozConnection) を使ってください。
