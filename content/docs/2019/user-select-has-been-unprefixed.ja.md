---
title: "`user-select` の接頭辞が外れました"
date: "2019-06-15T19:33:00-04:00"
categories: ["css"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1492739"
      title: "Bug 1492739 - Consider unprefixing -moz-user-select"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/XfKl9Jt7ZQ8/discussion"
      title: "Intent to implement and ship: Unprefix -moz-user-select, unship mozilla-specific values."
---
[Firefox 65](https://www.fxsitecompat.dev/ja/docs/2018/non-standard-moz-user-select-values-have-been-removed/) で `-moz-none` を除く非標準の値が削除されたのに続いて、Firefox 69 で `user-select` CSS プロパティの接頭辞が外れました。接頭辞付き `-moz-user-select` プロパティへの対応は将来的に廃止される可能性があります。
