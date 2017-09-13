---
title: "`window.content` が削除されました"
date: "2017-09-13T07:19:00-04:00"
categories: ["dom"]
tags: []
versions: ["57"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=864845"
      title: "Bug 864845 - Make window.content chrome-only"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Tmbs-wFwHzo/discussion"
      title: "Intent to unship: Visibility of window.content to untrusted code"
---
非標準の [`window.content`](https://developer.mozilla.org/ja/docs/Web/API/Window/content) オブジェクトは Firefox 57 以降ウェブコンテンツから使用できなくなりました。このオブジェクトは [`window.top`](https://developer.mozilla.org/ja/docs/Web/API/Window/top) あるいは多くの場合単純に [`window`](https://developer.mozilla.org/ja/docs/Web/API/Window) のエイリアスに過ぎないため有用ではありませんが、[Firefox 29](https://www.fxsitecompat.com/ja/docs/2014/window-content-controllers-pkcs11-and-loadstatus-have-been-removed/) で一度削除されたものの後方互換性を保つため再度追加された [`window.controllers`] (https://developer.mozilla.org/ja/docs/Web/API/Window/controllers) のように、ウェブ上ではブラウザー判別目的で誤用されている可能性があります。ウェブ開発者は常にこうした非標準機能の使用を避けるべきです。
