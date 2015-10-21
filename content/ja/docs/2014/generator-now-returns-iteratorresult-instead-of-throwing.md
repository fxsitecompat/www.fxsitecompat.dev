---
title: "ジェネレータが例外を投げる代わりに `IteratorResult` を返すようになりました"
date: "2014-02-07T11:57:09-05:00"
categories: ["javascript"]
tags: []
versions: ["29"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=958951": "Bug 958951 – Return IteratorResult object for completed generators instead of throwing"
---
ECMAScript 6 準拠の [ジェネレータ (yield)](http://wiki.ecmascript.org/doku.php?id=harmony:generators) 構文が [Firefox 26](https://developer.mozilla.org/ja/Firefox/Releases/26) で導入されました。この実装が最新仕様に合わせて更新され、完了したジェネレータ式が [`TypeError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/TypeError) を投げる代わりに `{ value: undefined, done: true }` のような `IteratorResult` オブジェクトを返すようになりました。 この挙動は [Firefox 27](https://www.fxsitecompat.com/ja/docs/2013/iterator-implementation-has-been-updated-to-the-latest-spec/) で実装が更新された [`Array`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array)、[`Map`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Map)、[`Set`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Set) インタフェースのイテレータと一致します。
