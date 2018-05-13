---
title: "接頭辞付き拡張機能が廃止予定となりました"
date: "2013-10-08T20:15:35-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["27"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=924176"
      title: "Bug 924176 – Warn on prefixed WebGL extensions usage (deprecated)"
---
`MOZ_` 接頭辞付きの WebGL [拡張機能文字列](https://developer.mozilla.org/docs/Web/WebGL/Using_Extensions) が廃止予定となりました。これらの対応は将来的に削除されます。接頭辞なし拡張機能文字列で代用してください。

* **更新**: 接頭辞付きエイリアスは [Firefox 58](https://www.fxsitecompat.com/ja/docs/2017/prefixed-webgl-extensions-are-no-longer-supported/) で削除されました。
