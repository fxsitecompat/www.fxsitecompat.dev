---
title: "`String.match` と `String.replace` が `RegExp.lastIndex` をリセットするようになりました"
date: "2013-10-08T20:15:35-04:00"
categories: ["javascript"]
tags: []
versions: ["27"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=501739"
      title: "Bug 501739 – String match and replace methods do not update global regexp lastIndex per ES3&5"
---
[`String.match`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/match)、[`String.replace`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/replace) 両メソッドが [`RegExp.lastIndex`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/RegExp/lastIndex) に関する仕様準拠問題を解決するためリファクタリングされました。これらのメソッドがグローバル正規表現とともに呼び出されたとき、`lastIndex` が、もし指定されていれば、`0` にリセットされるようになります。
