---
title: "イテレータの実装が最新仕様に合わせて更新されました"
date: "2013-10-08T20:15:35-04:00"
categories: ["javascript"]
tags: []
versions: ["27"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=881226"
      title: "Bug 881226 – Change {Array, Map, Set} iterator methods to mach the latest spec"
---
[イテレータプロトコル](https://bugzilla.mozilla.org/show_bug.cgi?id=907077) と [`for...of` ループ](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for...of) の実装が更新され、ECMAScript 6 仕様に準拠しました ([`StopIteration`](https://developer.mozilla.org/ja/docs/SpiderMonkey/JSAPI_Reference/JS_ThrowStopIteration) を使った SpiderMonkey の古いイテレータプロトコルから移行しました)。[`Array`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array)、[`Map`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Map)、[`Set`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Set)、[`String`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String) インタフェースの `iterator` メソッドは `@@iterator` に改名されました。従来、イテレータの `next` メソッドは、その配列の値 (もしくはオブジェクトのキーと値のペア) を返し、反復完了時に `StopIteration` 例外を発生させていました。`next` メソッドは今後 `{ done: false, value: <em>value</em> }` のようなオブジェクトを返し、反復完了時には `{ done: true, value: undefined }` を返します。
