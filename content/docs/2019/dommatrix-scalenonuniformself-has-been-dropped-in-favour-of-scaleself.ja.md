---
title: "`DOMMatrix.scaleNonUniformSelf()` が `scaleSelf()` に置き換えられる形で廃止されました"
date: "2019-07-06T21:58:00-04:00"
categories: ["dom"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1560119"
      title: "Bug 1560119 - Remove DOMMatrix.prototype.scaleNonUniformSelf()"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/r4B80kbt3FA/discussion"
      title: "Intent to unship: DOMMatrix.prototoype.scaleNonUniformSelf()"
---
Firefox 69 で `DOMMatrix` インターフェイスから `scaleNonUniformSelf` メソッドが削除されました。遡ること 2016 年に Geometry Interfaces 仕様がこのメソッドを `scaleSelf` に改名したたためです。今後はこのより新しいメソッドを使用してください。
