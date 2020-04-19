---
title: "`Object.watch()` が廃止予定となりました"
date: "2017-08-21T16:27:00-04:00"
categories: ["javascript"]
tags: []
versions: ["57", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=934669"
      title: "Bug 934669 - Deprecate Object.prototype.{,un}watch, and make them warn when used"
aliases:
    - "/ja/docs/2015/object-prototype-watch-will-be-removed/"
    - "/ja/docs/2017/object-prototype-watch-will-be-removed/"
    - "/ja/docs/2017/object-prototype-watch-has-been-deprecated/"
---
非標準の [`Object.prototype.watch`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/watch)、[`unwatch`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/unwatch) メソッドは廃止予定となり、近い将来削除されることとなりました。Firefox 57 以降、他のどのブラウザーも対応していないこれらのメソッドに対する警告がコンソールに表示されます。標準の [`Proxy`] (https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) あるいは [`Reflect`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Reflect) オブジェクトを代わりに使用してください。

以下の例は `Object.prototype.watch` を `Proxy` で単純に置き換えたものです。

```js
const o = { a: 1 };

// 非推奨
o.watch('a', (prop, oldval, newval) => {
  console.log(`o.${prop} は ${oldval} から ${newval} へ変更されました`);
  return newval;
});

o.a = 2; // o.a は 1 から 2 へ変更されました

// 推奨
const p = new Proxy(o, {
  set: (obj, prop, newval) => {
    const oldval = obj[prop];
    obj[prop] = newval;
    console.log(`p.${prop} は ${oldval} から ${newval} へ変更されました`);
    return true;
  }
});

p.a = 3; // p.a は 2 から 3 へ変更されました
```

**更新**: これらのメソッドは [Firefox 58](https://www.fxsitecompat.dev/ja/docs/2017/object-prototype-watch-has-been-removed/) で削除されました。
