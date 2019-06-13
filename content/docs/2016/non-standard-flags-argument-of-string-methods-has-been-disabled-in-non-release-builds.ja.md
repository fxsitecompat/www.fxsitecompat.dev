---
title: "`String` メソッドの非標準 `flags` 引数が非リリースビルドで無効化されました"
date: "2016-02-08T05:13:00-05:00"
categories: ["javascript"]
tags: []
versions: ["47"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1245801"
      title: "Bug 1245801 - Disable non-standard flag argument of String.prototype.{search,match,replace} in non-release build."
---
[Firefox 39 以降廃止予定となっている](https://www.fxsitecompat.dev/ja/docs/2015/non-standard-flags-argument-of-string-methods-has-been-deprecated/)、[`String.prototype.search`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/search)、[`match`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/match)、[`replace`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/replace) 各メソッドの非標準 `flags` 引数が、Firefox Nightly および Developer Edition で無効化されました。この引数は [近い将来完全に削除される](https://www.fxsitecompat.dev/ja/docs/2015/non-standard-flags-argument-will-be-removed-from-string-search-methods/) ため、今後使わないでください。

**更新**: `flags` 引数は Firefox 49 で完全に削除されました。
