---
title: "`Object.__proto__` セッターの使用は避けるべきです"
date: "2014-03-21T04:50:04-04:00"
categories: ["javascript"]
tags: []
versions: ["30"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=948227"
      title: "Bug 948227 – Make the Object.prototype.__proto__ setter warn about perf impact when used, and suggest alternatives"
---
[`Object.__proto__`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/proto) あるいは [`Object.setPrototypeOf`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/setPrototypeOf) を使ったオブジェクトのプロトタイプ変更は、その操作が非常に遅いため、絶対に推奨されません。Internet Explorer 11 は相互運用性のためとして `Object.__proto__` の対応を追加しましたが、このプロパティは廃止予定となっており使われるべきではありません。Firefox 30 とそれ以降のバージョンでは、JavaScript の厳格な警告が有効になっている場合、`Object.__proto__` セッターの使用について警告を表示します。ドキュメントに書かれているとおり、目的のプロトタイプでオブジェクトを作成するには、[`Object.create`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/create) メソッドを代わりに使用してください。
