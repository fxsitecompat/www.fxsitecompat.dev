---
title: "古い非標準ドラッグイベントが削除されました"
date: "2016-07-13T14:30:00-04:00"
categories: ["dom"]
tags: []
versions: ["50", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1162050"
      title: "Bug 1162050 - Remove draggesture and dragdrop events"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/thqN2Umpea0/discussion"
      title: "Intent to remove: support for old drag events"
aliases:
    - "/ja/docs/2015/legacy-non-standard-drag-events-will-be-removed/"
---
後方互換性のために残されていた非標準ドラッグ関連イベントへの対応が Firefox 50 で削除されました。`draggesture`、`dragdrop` イベントはそれぞれ標準の [`dragstart`](https://developer.mozilla.org/docs/Web/Events/dragstart)、[`drop`](https://developer.mozilla.org/docs/Web/Events/drop) イベントに置き換えてください。一方、[`dragexit`](https://developer.mozilla.org/docs/Web/Events/dragexit) イベントは標準化されたため、それに関して心配する必要はなくなりました。

**更新**: この変更は *NFL.com* や *TweetDeck* などいくつかのサイトに影響しているようです。
