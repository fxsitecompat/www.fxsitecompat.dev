---
title: "`window._content`、`controllers`、`pkcs11`、`LoadStatus` が削除されました"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
versions: ["29"]
statuses: "reverted"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=946564"
      title: "Bug 946564 – Make window._content chromeonly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=794943"
      title: "Bug 794943 – Remove nsISecurityCheckedComponent"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=964964"
      title: "Bug 964964 – Try to remove window.pkcs11"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=949292"
      title: "Bug 949292 – Stop exposing LoadStatus on the global object"
---
グローバルオブジェクトを標準化する現在進行中の取り組みの一環として、[`window`](https://developer.mozilla.org/docs/Web/API/window) からいくつかのプロパティが削除されました。`_content` プロパティは [`window.content`](https://developer.mozilla.org/docs/Web/API/window.content) と重複しており、ウェブコンテンツから使用できなくなりました。[`window.pkcs11`](https://developer.mozilla.org/docs/Web/API/window.pkcs11) プロパティはセキュリティ上の理由から Firefox 3.0.14 以降 `null` を返していました。非標準の [`controllers`](https://developer.mozilla.org/docs/Web/API/window.controllers) プロパティと `LoadStatus` インターフェイスも `window` 上で参照できなくなりました。
