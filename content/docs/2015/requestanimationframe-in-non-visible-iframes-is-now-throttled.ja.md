---
title: "不可視 iframe 内の `requestAnimationFrame` が減速されるようになりました"
date: "2015-08-19T17:11:16-04:00"
categories: ["html"]
tags: []
versions: ["40"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1145439"
      title: "Bug 1145439 - Throttle off-screen iframes to be more efficient"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1195592"
      title: "Bug 1195592 - FF 40.0.2: Disqus comments take much longer to load than prev version."
---
パフォーマンスとバッテリー寿命を向上させるため、ページ上で見えていない [`<iframe>`](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) 内の [`requestAnimationFrame`](https://developer.mozilla.org/docs/Web/API/Window/requestAnimationFrame) が、背面のタブにある場合と同様に、減速されるようになりました。`requestAnimationFrame` を持った隠し iframe のためにコメントの読み込みが非常に遅くなるという問題が *Disqus* に報告され、修正されました。
