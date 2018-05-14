---
title: "`XMLHttpRequest`、`FileReader`、`WebSocket`、`EventSource` オブジェクトの `on*` プロパティの値にイベントリスナーオブジェクトを設定できなくなります"
date: "2012-12-29T03:53:26-05:00"
categories: ["dom"]
tags: []
versions: ["18"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=687332"
      title: "Bug 687332 – Move various onfoo event listeners off of DOM objects and into event listener managers"
---
この変更により、`xhr.onreadystatechange = { handleEvent: function() { ... } }` のように `handleEvent` プロパティを持つオブジェクトの形式を取るハンドラーが動作しなくなります。対象となるのは `XMLHttpRequest`、`WebSocket`、`FileReader`、`EventSource` オブジェクトで、従来から動作していない、要素、ドキュメント、`window` オブジェクトと同様になります。Firefox (Gecko) では今後、そうしたコードは `xhr.onreadystatechange = null` と同じに扱われ、実行されずエラーも生じません。これは標準準拠と相互運用性向上ための措置で、Internet Explorer や Opera と同じ挙動になります。Google Chrome などの WebKit ブラウザーはまだこのような形式に対応しています。

なお、`xhr.onreadystatechange = function() { ... }` は引き続き動作しますが、一般的には [`addEventListener`](https://developer.mozilla.org/docs/DOM/element.addEventListener) を代わりに使うことが推奨されます。
