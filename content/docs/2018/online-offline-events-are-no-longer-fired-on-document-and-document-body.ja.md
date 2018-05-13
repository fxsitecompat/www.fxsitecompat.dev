---
title: "`online`/`offline` イベントが `document` と `document.body` 上で発生しなくなりました"
date: "2018-05-08T18:25:00-04:00"
categories: ["dom", "html"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1457166"
      title: "Bug 1457166 - Figure out what's the right target of the online / offline events."
---
従来、[`online` および `offline` イベント](https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events) は `document.body` 上で発生し、`document` と `window` へ遡上していましたが、これは現行の HTML 仕様によれば誤りでした。Firefox 61 でこの非標準の挙動が修正され、それらのイベントは `window` 上でのみ発生するようになりました。なお、`<body>` 要素上の `ononline` および `onoffline` 属性は有効であり、引き続き使用可能です。

```js
// 非推奨
document.body.addEventListener('online', ...);
document.body.addEventListener('offline', ...);
document.addEventListener('online', ...);
document.addEventListener('offline', ...);

// 推奨
window.addEventListener('online', ...);
window.addEventListener('offline', ...);
```
