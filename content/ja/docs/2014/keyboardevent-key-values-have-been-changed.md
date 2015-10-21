---
title: "`KeyboardEvent.key` の値が変更されました"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
versions: ["29"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=912858": "Bug 912858 – Implement KeyboardEvent.key for printable keys (except dead key handling)"
---
[`KeyboardEvent.key`](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent.key) の実装が最新の DOM3 Events 仕様に合わせて更新され、それに伴ってキーの値が変更されました。例えば、`"Spacebar"` は `" "` に、`"Add"` は `"+"` になります。また、印刷可能な一般的なキーは `"MozPrintableKey"` の代わりに実際の文字を返すようになりました。詳しくは [ドキュメント](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent.key) を参照してください。

なお、従来の [`KeyboardEvent.charCode`](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent.charCode)、[`KeyboardEvent.keyCode`](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent.keyCode)、[`KeyboardEvent.which`](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent.which) プロパティは廃止予定となっており、仕様と実装が安定次第、開発者は `KeyboardEvent.key` を使うことを検討してください。
