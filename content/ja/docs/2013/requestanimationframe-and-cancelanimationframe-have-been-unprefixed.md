---
title: "`requestAnimationFrame` と `cancelAnimationFrame` の接頭辞が外れました"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
versions: ["23"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=704063"
      title: "Bug 704063 – Add unprefixed requestAnimationFrame"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=876282"
      title: "Bug 876282 – Add unprefixed cancelAnimationFrame"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=753453"
      title: "Bug 753453 – requestAnimationFrame callback should return DOMHighResTimeStamp"
---
`mozRequestAnimationFrame` の接頭辞なしバージョンとなる [`requestAnimationFrame`](https://developer.mozilla.org/ja/docs/Web/API/window.requestAnimationFrame) が追加されました。この接頭辞なしメソッドはコールバック関数に [`DOMHighResTimeStamp`](https://developer.mozilla.org/ja/docs/Web/API/DOMHighResTimeStamp) を渡します。これはマイクロ秒精度を持ち、[`performance.now`](https://developer.mozilla.org/ja/docs/Web/API/window.performance.now) と比較可能です。

一方、将来的に廃止される接頭辞付き関数は、これまで通りエポック秒ベースの [`DOMTimeStamp`](https://developer.mozilla.org/ja/docs/Web/API/DOMTimeStamp) をコールバック関数に渡します。渡された値はミリ秒精度を持ち、[`mozAnimationStartTime`](https://developer.mozilla.org/ja/docs/Web/API/window.mozAnimationStartTime) と比較可能です。

接頭辞なしの [`cancelAnimationFrame`](https://developer.mozilla.org/ja/docs/Web/API/window.cancelAnimationFrame) メソッドも追加されました。これは接頭辞付き `mozCancelAnimationFrame` メソッドと同じ挙動となります。これらの `moz` 接頭辞付きメソッドは将来削除されます。

**更新**: これらの接頭辞付きメソッドは [Firefox 42 で削除されました](https://www.fxsitecompat.com/ja/docs/2015/mozrequestanimationframe-and-related-apis-have-been-removed/)。
