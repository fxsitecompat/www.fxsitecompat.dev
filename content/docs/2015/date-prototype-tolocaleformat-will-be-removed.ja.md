---
title: "`Date.prototype.toLocaleFormat` が廃止されます"
date: "2015-10-26T00:39:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=818634"
      title: "Bug 818634 - Remove support for Date.prototype.toLocaleFormat"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1299900"
      title: "Bug 1299900 - Warn when Date.prototype.toLocaleFormat is used"
---
[`Date.prototype.toLocaleFormat`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleFormat) メソッドは、標準化されなかったため、削除されます。ECMAScript 2015 (ES6) は、日付を様々な言語で簡単に出力するために使用できる [`toLocaleDateString`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString) メソッドを代わりに提供しています。

**更新**: [Firefox 55](https://www.fxsitecompat.com/ja/docs/2017/date-prototype-tolocaleformat-has-been-deprecated/) 以降、この廃止予定メソッドが使われていた場合、ウェブコンソールが警告を表示します。
