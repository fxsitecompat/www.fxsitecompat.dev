---
title: "`const` や `let` で定義された変数は `window` 上のプロパティにならなくなりました"
date: "2015-10-13T20:37:00-04:00"
categories: ["javascript"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=589199": "Bug 589199 - Add an extra scope chain object for top-level script execution, encountered just before the global object, containing top-level |let| declaration bindings"
---
ECMAScript 2015 (ES6) 準拠の一環として、[`const`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/const)、[`let`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/let) 命令文の挙動が仕様に合わせて変更されました。

従来これらの命令文で定義された変数は、[`var`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/var) で定義された変数と同様に、グローバルオブジェクト ([`window`](https://developer.mozilla.org/ja/docs/Web/API/Window) もしくはグローバルスコープ内の [`this`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/this)) 上のプロパティとしてアクセス可能でした。これは今後動作しなくなるため、`let x = 1; alert(window.x);` と `const y = 1; alert(window.y);` はいずれも `undefined` となります。一方 `var z = 1; alert(window.z);` では引き続き `1` が出力されます。この問題の最も簡単な回避策は、`const` や `let` の代わりに `var` を使うことです。
