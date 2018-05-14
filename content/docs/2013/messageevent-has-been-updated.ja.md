---
title: "`MessageEvent` が更新されました"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: ["26"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=848294"
      title: "Bug 848294 – Update MessageEvent to be compatible with the spec"
---
[`MessageEvent`](https://developer.mozilla.org/docs/Web/API/MessageEvent) インターフェイスが最新仕様準拠のため更新されました。インターフェイスがコンストラクターになったため、`initMessageEvent` メソッドは削除されました。

**更新**: `initMessageEvent` メソッドは、仕様に戻されたため、[Firefox 44 で再度追加されました](https://bugzilla.mozilla.org/show_bug.cgi?id=949376)。
