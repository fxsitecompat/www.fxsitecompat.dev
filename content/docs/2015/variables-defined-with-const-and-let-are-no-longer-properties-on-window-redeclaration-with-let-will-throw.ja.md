---
title: "`const` や `let` で定義された変数は `window` 上のプロパティとならなくなり、`let` による再宣言は例外が投げられます"
date: "2015-10-13T20:37:00-04:00"
categories: ["javascript"]
tags: []
versions: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=589199"
      title: "Bug 589199 - Add an extra scope chain object for top-level script execution, encountered just before the global object, containing top-level |let| declaration bindings"
aliases:
    - "/ja/docs/2015/variables-defined-with-const-and-let-are-no-longer-properties-on-window/"
---
ECMAScript 2015 (ES6) 準拠の一環として、[`const`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/const)、[`let`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let) 命令文の挙動が仕様に合わせて変更されました。

従来これらの命令文で定義されたグローバル変数は、[`var`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/var) で定義されたグローバル変数と同様に、グローバルオブジェクト ([`window`](https://developer.mozilla.org/docs/Web/API/Window) もしくはグローバルスコープ内の [`this`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/this)) 上のプロパティとしてアクセス可能でした。これは今後動作しなくなるため、`let x = 1; alert(window.x);` と `const y = 1; alert(window.y);` はいずれも `undefined` となります。一方 `var z = 1; alert(window.z);` では引き続き `1` が出力されます。この問題の最も簡単な回避策は、`const` や `let` の代わりに `var` を使うことです。

同時に、`let` によるグローバル変数の再宣言も禁止され、以下のコードサンプルは動作しなくなります。

```js
<script>
  let a = 1;
  let a = 2; // TypeError が投げられます
</script>
```

```js
<script>
  let a = 1;
</script>
<script>
  let a = 2; // TypeError が投げられます
</script>
```

```js
<script src="other.js"></script>
<script>
  let a = 2; // a が other.js 内で定義されている場合 TypeError が投げられます
</script>
```

また、[`eval`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/eval) メソッドで評価されたコードは、`let` あるいは `const` で定義されたグローバル変数を外部コンテキストへ伝播しなくなり、従って以下のコードも動作しません。

```js
<script>
  eval('let a = 1;');
  alert(a); // ReferenceError が投げられます
</script>
```

なお、`let` 命令文は [明示的な JavaScript バージョンを必要としなくなりました](https://www.fxsitecompat.dev/ja/docs/2015/let-statement-no-longer-requires-explicit-javascript-version/)。

**更新**: Firefox 46 以降、変数の再宣言は、仕様に従って `TypeError` ではなく [`SyntaxError` を投げるようになりました](https://bugzilla.mozilla.org/show_bug.cgi?id=1198833)。
