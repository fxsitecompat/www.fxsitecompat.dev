---
title: "古い非標準ドラッグイベントが削除されます"
date: "2015-10-25T17:02:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1162050": "Bug 1162050 - Remove draggesture and dragdrop events"
    "https://groups.google.com/d/topic/mozilla.dev.platform/thqN2Umpea0/discussion": "Intent to remove: support for old drag events"
---
後方互換性のために残されていた非標準のドラッグ関連イベントが近い将来削除されることになりました。`draggesture`、`dragdrop` イベントはそれぞれ標準の [`dragstart`](https://developer.mozilla.org/ja/docs/Web/Events/dragstart)、[`drop`](https://developer.mozilla.org/ja/docs/Web/Events/drop) イベントに置き換えられます。`dragexit` は、まったく同じ標準イベントがないため残されますが、多くの場合 [`dragleave`](https://developer.mozilla.org/ja/docs/Web/Events/dragleave) と [`dragend`](https://developer.mozilla.org/ja/docs/Web/Events/dragend) で代用できるでしょう。
