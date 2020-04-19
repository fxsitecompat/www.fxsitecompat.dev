---
title: "`WebAssembly.Module` の IndexedDB シリアライズ対応が廃止されました"
date: "2018-08-16T10:25:00-04:00"
categories: ["misc"]
tags: []
versions: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1469395"
      title: "Bug 1469395 - Remove WebAssembly.Module IndexedDB serialization support"
---
[コンパイルされた WebAssembly モジュールを IndexedDB にキャッシュする](https://dzone.com/articles/webassembly-caching-to-html5-indexeddb) ことを可能にしていた [`WebAssembly.Module`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WebAssembly/Module) の実験的な IndexedDB シリアライズ対応が、複数の懸念が表明されたことから、最新の WebAssembly 仕様に従って Firefox 63 で削除されました。この機能は Firefox と Microsoft Edge にしか実装されていないことから、互換性リスクは低いはずです。代わりに [通常の HTTP キャッシュ](https://developer.mozilla.org/docs/Web/HTTP/Caching) か [Cache API](https://developer.mozilla.org/docs/Web/API/Cache) を使用してください。
