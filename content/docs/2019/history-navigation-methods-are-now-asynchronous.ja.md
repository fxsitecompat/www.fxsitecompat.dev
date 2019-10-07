---
title: "履歴遷移メソッドが非同期となりました"
date: "2019-10-07T10:50:00-04:00"
categories: ["html"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1563587"
      title: "Bug 1563587 - Make history navigations asynchronous"
---
Firefox 70 以降、[`history.back`](https://developer.mozilla.org/docs/Web/API/History/back)、[`history.forward`](https://developer.mozilla.org/docs/Web/API/History/forward)、[`history.go`](https://developer.mozilla.org/docs/Web/API/History/go) メソッドが、Google Chrome や Apple Safari のように非同期動作となります。[バグのコメント](https://bugzilla.mozilla.org/show_bug.cgi?id=1563587#c26) で指摘されている通り、この変更は (ブラウザー判別と) まだ Microsoft Edge でも見られる同期動作に依存しているサイトに影響を与える可能性があります。[`popstate`](https://developer.mozilla.org/docs/Web/API/Window/popstate_event) イベントを監視することで、履歴遷移が完了したタイミングを知ることができます。
