---
title: "`ProgressEvent.initProgressEvent` が Web ワーカー内で使用できなくなりました"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
versions: "24"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=870466": "Bug 870466 – Remove initProgressEvent from workers too"
---
廃止された `ProgressEvent.initProgressEvent` メソッドが [Web ワーカー](https://developer.mozilla.org/ja/docs/Web/Guide/Performance/Using_web_workers) 内で使用できなくなりました。一般的な用法としてのこのメソッドは [Firefox 22](http://www.fxsitecompat.com/ja/versions/22/) で削除されています。
