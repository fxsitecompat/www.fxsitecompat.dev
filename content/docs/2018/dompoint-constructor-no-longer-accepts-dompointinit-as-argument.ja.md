---
title: "`DOMPoint` コンストラクターが `DOMPointInit` を引数として取らなくなりました"
date: "2018-05-23T22:20:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1186265"
      title: "Bug 1186265 - Remove DOMPoint{,ReadOnly}(DOMPointInit) constructor, implement DOMPoint{,ReadOnly}.fromPoint"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jwmkVmU4DNM/discussion"
      title: "Intent to ship: DOMPoint interface from its latest spec"
---
Firefox 62 で [`DOMPoint`](https://developer.mozilla.org/docs/Web/API/DOMPoint)、[`DOMPointReadOnly`](https://developer.mozilla.org/docs/Web/API/DOMPointReadOnly) インターフェイスの実装が現行の Geometry Interfaces Module ドラフト仕様に合わせて更新されました。

それらの [コンストラクター](https://developer.mozilla.org/docs/Web/API/DOMPoint/DOMPoint) は、`x` 座標、`y` 座標、`z`座標、`w` 視点を含む `DOMPointInit` ディクショナリーを受け付けなくなりました。それらの値はそのコンストラクターの別々の引数として指定する必要があります。あるいは、`DOMPointInit` ディクショナリーを引数として取る新しい `DOMPoint.fromPoint`、`DOMPointReadOnly.fromPoint` 静的メソッドを使うこともできます。

```js
// 非推奨
let dp = new DOMPoint({ x, y, z, w });

// 推奨
let dp = new DOMPoint(x, y, z, w);
// もしくは
let dp = DOMPoint.fromPoint({ x, y, z, w });
```
