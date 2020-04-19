---
title: "`showModalDialog()` が廃止予定となりました"
date: "2013-12-09T02:32:17-05:00"
categories: ["dom"]
tags: []
releases: ["28", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=933040"
      title: "Bug 933040 – Warn for showModalDialog uses"
---
Internet Explorer 由来の [`window.showModalDialog`](https://developer.mozilla.org/docs/Web/API/window.showModalDialog) メソッドが、非推奨、廃止予定となりました。代わりに [`window.open`](https://developer.mozilla.org/docs/Web/API/window.open) メソッドを使ってください。

**更新**: Firefox 46 以降、Firefox が *e10s* と呼ばれるマルチプロセスモードで実行されている場合、[このメソッドは無効化されます](https://www.fxsitecompat.dev/ja/docs/2015/showmodaldialog-has-been-disabled-in-multi-process-firefox/)。

**更新**: *e10s* が初期設定で有効化されたことに伴い、このメソッドは [Firefox 48](https://www.fxsitecompat.dev/ja/docs/2016/window-showmodaldialog-has-been-removed/) 以降では使用できなくなりました。
