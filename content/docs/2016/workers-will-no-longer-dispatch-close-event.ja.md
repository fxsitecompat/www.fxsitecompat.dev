---
title: "ワーカーが `close` イベントを発生させなくなりました"
date: "2016-09-02T03:32:00-04:00"
categories: ["dom"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=790919"
      title: "Bug 790919 - Don't dispatch close event, and remove onclose"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/mqKBGePe4-s/discussion"
      title: "Intent to unship: WorkerGlobalScope.onclose"
---
[`WorkerGlobalScope.onclose`](https://developer.mozilla.org/docs/Web/API/WorkerGlobalScope/onclose) プロパティが、ずっと前に仕様から外されているため削除され、そのためウェブワーカーが [`close`](https://developer.mozilla.org/docs/Web/Events/close) イベントを発生させなくなりました。他にこれを実装しているブラウザーはないため、互換性への影響は軽微なはずです。
