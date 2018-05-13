---
title: "`String.prototype.contains` が `includes` に改名されました"
date: "2015-04-27T13:17:23-04:00"
categories: ["javascript"]
tags: []
versions: ["40"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1102219"
      title: "Bug 1102219 - Rename String.prototype.contains to String.prototype.includes"
---
ECMAScript 6 と Firefox 18 で導入された `String.prototype.contains` メソッドは、無視できないサイト互換性問題を生じさせていました。特に影響を受けていた [*MooTools*](https://bugzilla.mozilla.org/show_bug.cgi?id=789036) ライブラリは既に修正されていますが、同様に互換性問題で `contains` から改名された [`Array.prototype.includes`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/includes) との整合性を保つため、このメソッドは [`String.prototype.includes`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes) に改名されました。Firefox の実装も仕様に合わせる形で更新されました。廃止予定となった `contains` メソッドはまだ `includes` のエイリアスとして残されていますが、近い将来 [削除されます](https://www.fxsitecompat.com/ja/docs/2015/string-prototype-contains-will-be-removed/)。
