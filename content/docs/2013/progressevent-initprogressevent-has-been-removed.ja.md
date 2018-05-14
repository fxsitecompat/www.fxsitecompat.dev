---
title: "`ProgressEvent.initProgressEvent` が削除されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=843489"
      title: "Bug 843489 – [Progress Events] Remove support for ProgressEvent.initProgressEvent() and Document.createEvent(\"ProgressEvent\")"
---
[`ProgressEvent.initProgressEvent`](https://developer.mozilla.org/docs/Web/API/ProgressEvent.initProgressEvent) メソッドは、仕様から削除されたため、使用できなくなりました。`document.createEvent("ProgressEvent")` の対応も削除されました。
