---
title: "`WebAssembly.Module` の IndexedDB デシリアライズ対応が廃止されました"
date: "2019-08-13T16:15:00-04:00"
categories: ["misc"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1561876"
      title: "Bug 1561876 - Remove support for de-serializing WebAssembly.Modules in IDB"
---
[`WebAssembly.Module`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WebAssembly/Module) の実験的な IndexedDB デシリアライズ対応が Firefox 70 で削除されました。シリアライズ対応は既に [Firefox 63](https://www.fxsitecompat.dev/ja/docs/2018/indexeddb-serialization-support-has-been-removed-from-webassembly-module/) で削除されています。
