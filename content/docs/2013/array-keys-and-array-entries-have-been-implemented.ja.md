---
title: "`Array.keys` と `Array.entries` が実装されました"
date: "2013-12-09T02:32:17-05:00"
categories: ["javascript"]
tags: []
versions: ["28"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=894658"
      title: "Bug 894658 – Implement ES6 Array.prototype.{keys, entries}"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=958095"
      title: "Bug 958095 – Array.prototype.keys() breaks web apps, e.g. dagre-d3"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=987762"
      title: "Bug 987762 – Firefox 28.0 javascript xhr raw response object (from json API) has a property \'entries\' which is a [native code] function"
---
[ECMAScript 6 対応](https://developer.mozilla.org/ja/docs/Web/JavaScript/ECMAScript_6_support_in_Mozilla) の一環として、[`Array.keys`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/keys)、[`Array.entries`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/entries) メソッドが実装されました。これにより、[`Array.prototype`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/prototype) を独自メソッドで拡張している一部 JavaScript ライブラリが動作しなくなる可能性があります。少なくとも 2 つのアプリにリグレッションが見つかっており、そのうちの 1 つに影響する *dagre-d3* JavaScript ライブラリは Aurora 開発サイクル中に修正されました。
