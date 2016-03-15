---
title: "`String.prototype.contains` が廃止されます"
date: "2015-10-26T00:25:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1103588"
      title: "Bug 1103588 - Remove String.prototype.contains"
---
[Firefox 40 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2015/string-prototype-contains-has-been-renamed-to-includes/) `String.prototype.contains` メソッドへの対応が近い将来削除されます。サイト互換性問題のため、このメソッドは [`includes`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/includes) に改名されました。
