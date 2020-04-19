---
title: "`String` 検索メソッドから非標準 `flags` 引数が削除されました"
date: "2016-05-10T10:34:00-04:00"
categories: ["javascript"]
tags: []
versions: ["49", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1108382"
      title: "Bug 1108382 - Remove non-standard flag argument from String.prototype.{search,match,replace}"
aliases:
    - "/ja/docs/2015/non-standard-flags-argument-will-be-removed-from-string-search-methods/"
---
[Firefox 39 以降廃止予定となり](https://www.fxsitecompat.dev/ja/docs/2015/non-standard-flags-argument-of-string-methods-has-been-deprecated/)、[Firefox 47 以降非リリースビルドで無効化されていた](https://www.fxsitecompat.dev/ja/docs/2016/non-standard-flags-argument-of-string-methods-has-been-disabled-in-non-release-builds/)、[`String.prototype.search`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/search)、[`match`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/match)、[`replace`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/replace) 各メソッドの `flags` 引数は、完全に削除されました。
