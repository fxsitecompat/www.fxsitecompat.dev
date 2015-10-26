---
title: "`Date.prototype.toLocaleFormat` が廃止されます"
date: "2015-10-26T00:39:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=818634": "Bug 818634 - Remove support for Date.prototype.toLocaleFormat"
---
[`Date.prototype.toLocaleFormat`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleFormat) メソッドは、標準化されなかったため、削除されます。ECMAScript 2015 (ES6) は、日付を様々な言語で簡単に出力するために使用できる [`toLocaleDateString`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString) メソッドを代わりに提供しています。
