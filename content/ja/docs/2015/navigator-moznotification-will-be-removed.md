---
title: "`navigator.mozNotification` が削除されます"
date: "2015-10-27T23:36:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=952453": "Bug 952453 - Remove mozNotification API"
---
Android 版 Firefox のみで使用でき、Firefox 22 以降廃止予定となっている非標準の [`navigator.mozNotification`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/mozNotification) オブジェクトは、将来的に削除されます。代わりに標準の [Notifications API](https://developer.mozilla.org/ja/docs/Web/API/Notifications_API) を使用してください。
