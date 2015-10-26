---
title: "古い Proxy API が削除されます"
date: "2015-10-26T15:20:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=892903": "Bug 892903 - Remove Proxy.create and Proxy.createFunction"
---
[Firefox 18 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2012/proxy-api-has-been-updated-for-the-new-spec/)、`Proxy.create`、`Proxy.createFunction` メソッドを含む非標準の [古い Proxy API](https://developer.mozilla.org/ja/docs/Archive/Web/Old_Proxy_API) は、近い将来削除されます。[標準化された Proxy API](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Proxy) を代わりに使用してください。
