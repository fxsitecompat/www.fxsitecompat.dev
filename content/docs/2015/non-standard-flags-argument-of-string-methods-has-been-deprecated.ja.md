---
title: "`String` メソッドの非標準 `flags` 引数が廃止予定となりました"
date: "2015-03-17T14:02:59-04:00"
categories: ["javascript"]
tags: []
versions: ["39"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1142351"
      title: "Bug 1142351 - Add console warnings for non-standard flag argument of String.prototype.{search,match,replace}."
---
[`String.prototype.search`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/search)、[`match`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/match)、[`replace`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/replace) メソッドの非標準 `flags` 引数が廃止予定となり、近い将来削除されることとなりました。コード内でこの引数が使われていた場合、今後 [ウェブコンソール](https://developer.mozilla.org/ja/docs/Tools/Web_Console) に警告が出力されます。

**更新**: Firefox 47 以降の Firefox Nightly および Developer Edition では、この引数は [無効化されています](https://www.fxsitecompat.com/ja/docs/2016/non-standard-flags-argument-of-string-methods-has-been-disabled-in-non-release-builds/)。
