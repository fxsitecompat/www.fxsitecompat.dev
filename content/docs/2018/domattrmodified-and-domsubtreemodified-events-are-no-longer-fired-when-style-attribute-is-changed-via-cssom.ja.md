---
title: "CSSOM を通じた `style` 属性の変更時に `DOMAttrModified` と `DOMSubtreeModified` イベントが発生しなくなります"
date: "2018-05-23T21:22:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["62", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460295"
      title: "Bug 1460295 - unresponsive visiting login page on eqbank.ca"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/YD4jeL00HHU/discussion"
      title: "Intent to unship: DOMAttrModified and DOMSubtreeModified event for changes via CSSOM"
---
Firefox は、[`style`](https://developer.mozilla.org/docs/Web/API/HTMLElement/style) プロパティなど CSSOM を通じて要素の `style` 属性に対して行われた変更について、`DOMAttrModified` と `DOMSubtreeModified` の [変異イベント](https://developer.mozilla.org/docs/Web/Guide/Events/Mutation_events) を発生させないようにしました。

この変更は、入れ子になった `DOMSubtreeModified` イベントが無限ループに陥る場合があるというサイトパフォーマンスの問題を解決するために行われました。そうした問題は `DOMAttrModified` イベントが実装されていない Chrome や Safari では起こりません。

代わりとなる [変異オブザーバー](https://developer.mozilla.org/docs/Web/API/MutationObserver) はこの変更の影響を受けません。

なお、DOM3 UI Events 仕様では変異イベントは廃止予定とされており、そのため将来的にブラウザーから対応が削除されます。いずれにしても変異オブザーバーを代わりに使用してください。
