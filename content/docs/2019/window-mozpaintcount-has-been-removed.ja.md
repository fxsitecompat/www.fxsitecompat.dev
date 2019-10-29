---
title: "`window.mozPaintCount` が削除されました"
date: "2019-10-29T07:50:00-04:00"
categories: ["dom"]
tags: []
versions: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1591968"
      title: "Bug 1591968 - Consider removing window.mozPaintCount."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/sZbx3Q2hIpA/discussion"
      title: "Intent to unship: window.mozPaintCount."
---
非標準の [`window.mozPaintCount`](https://developer.mozilla.org/docs/Web/API/Window/mozPaintCount) プロパティが Firefox 72 で廃止されました。この API は他のどのブラウザーにも実装されていないため、ブラウザー判別目的で使われていない限り互換性リスクは非常に低いはずです。
