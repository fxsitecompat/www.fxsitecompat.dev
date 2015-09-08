---
title: "`DataContainerEvent`、`BrowserFeedWriter`、`EventListenerInfo`、`XPathNamespace` が削除されました"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: "31"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=980134": "Bug 980134 – Hide DataContainerEvent from content"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=983845": "Bug 983845 – Stop exposing BrowserFeedWriter to the Web"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=991690": "Bug 991690 – Remove the classinfo from EventListenerInfo"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=998738": "Bug 998738 – Consider removing nsIDOMXPathNamespace (and window.XPathNamespace)"
---
グローバルオブジェクトを標準化する現在進行中の取り組みの一環として、[`window`](https://developer.mozilla.org/ja/docs/Web/API/window) からいくつかのインタフェースが削除されました。Firefox 独自の `DataContainerEvent` については、代わりに標準の [`CustomEvent`](https://developer.mozilla.org/ja/docs/Web/API/CustomEvent) を使用してください。`BrowserFeedWriter` は Web コンテンツに公開されるべきではない Firefox 独自のインタフェースでした。`EventListenerInfo` もグローバルオブジェクトとすることが意図されていなかった非標準のインタフェースでした。`XPathNamespace` インタフェースは DOM3 XPath 仕様の一部でしたが実装されていませんでした。
