---
title: "`ProgressEvent.initProgressEvent()` が Web Worker 内で使用できなくなりました"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
versions: ["24"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=870466"
      title: "Bug 870466 – Remove initProgressEvent from workers too"
---
廃止された `ProgressEvent.initProgressEvent` メソッドが [Web Worker](https://developer.mozilla.org/docs/Web/Guide/Performance/Using_web_workers) 内で使用できなくなりました。一般的な用法としてのこのメソッドは [Firefox 22 で削除されています](https://www.fxsitecompat.com/ja/docs/2013/progressevent-initprogressevent-has-been-removed/)。
