---
title: "`String` 検索メソッドから非標準 `flags` 引数が削除されます"
date: "2015-10-26T17:26:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1108382"
      title: "Bug 1108382 - Remove non-standard flag argument from String.prototype.{search,match,replace}"
---
[Firefox 39 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2015/non-standard-flags-argument-of-string-methods-has-been-deprecated/)、[`String.prototype.search`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/search)、[`match`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/match)、[`replace`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/replace) 各メソッドの `flags` 引数は、近い将来削除されます。

**更新**: Firefox 47 以降の Firefox Nightly および Developer Edition では、この引数は [無効化されています](https://www.fxsitecompat.com/ja/docs/2016/non-standard-flags-argument-of-string-methods-has-been-disabled-in-non-release-builds/)。
