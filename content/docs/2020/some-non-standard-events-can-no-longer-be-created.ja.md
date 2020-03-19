---
title: "一部の非標準イベントが作成できなくなりました"
date: "2020-02-10T22:03:00-05:00"
categories: ["dom"]
tags: []
versions: ["74"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1610819"
      title: "Bug 1610819 - Remove support for creating some non-standard event types"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623223"
      title: "Bug 1623223 - CreateEvent regression"
---
Firefox 74 で [`document.createEvent()`](https://developer.mozilla.org/docs/Web/API/Document/createEvent) を用いたいくつかの非標準イベント作成への対応が打ち切られました。これらのイベントタイプには以下のものが含まれます。

* `KeyEvents` (標準代替イベント: `KeyboardEvent`)
* `MouseScrollEvents`
* `ScrollAreaEvent`
* `TimeEvent`

**更新**: 1 つの小さなサイトがこの変更の影響を受けています。
