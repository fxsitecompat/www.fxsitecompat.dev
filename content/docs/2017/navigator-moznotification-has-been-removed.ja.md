---
title: "`navigator.mozNotification` が削除されました"
date: "2017-12-09T00:36:00-05:00"
categories: ["dom"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=952453"
      title: "Bug 952453 - Remove mozNotification (DesktopNotification) API"
aliases:
    - "/ja/docs/2015/navigator-moznotification-will-be-removed/"
---
Android 版 Firefox のみで使用でき、Firefox 22 以降廃止予定となっていた非標準の [`navigator.mozNotification`](https://developer.mozilla.org/docs/Web/API/Navigator/mozNotification) オブジェクトは、Firefox 59 で削除されました。代わりに標準の [Notifications API](https://developer.mozilla.org/docs/Web/API/Notifications_API) を使用してください。
