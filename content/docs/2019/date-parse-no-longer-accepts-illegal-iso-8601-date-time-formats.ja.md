---
title: "`Date.parse()` が不正な ISO 8601 日時形式を受け付けなくなりました"
date: "2019-06-10T00:44:00-04:00"
categories: ["javascript"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1500748"
      title: "Bug 1500748 - Date.parse accepts illegal non-zero-padded ISO8601 format"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1550949"
      title: "Bug 1550949 - Disallow time-only version of ISO8601"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1551893"
      title: "Bug 1551893 - Disallow non-zero-padded time element in Date.parse if time part marker T exists"
---
Firefox で `Date.parse` 静的メソッドがいくつかの不正な ISO 8601 日時形式を問題なく解析していたことが分かりました。Firefox 68 で実装が修正され、こうした値は今後 `NaN` となります。

* `2018-1-7T00:00Z` (日付の頭にゼロが欠落、正しくは `2018-01-07T00:00Z`)
* `2019-05-15T1:1:1` (時刻の頭にゼロが欠落、正しくは `2019-05-15T01:01:01`)
* `T00:00:00Z` (日付なし)
