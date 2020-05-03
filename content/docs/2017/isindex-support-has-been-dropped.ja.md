---
title: "`<isindex>` 対応が廃止されました"
date: "2017-07-13T21:35:00-04:00"
categories: ["html"]
tags: []
releases: ["56", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1266495"
      title: "Bug 1266495 - Consider removing <isindex> from the parser and form submission [tor 18914]"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/DV3YBf7wI3M/discussion"
      title: "Intent to remove: <isindex>"
aliases:
    - "/ja/docs/2016/isindex-support-will-be-removed/"
supported_tools:
  firefox_extension: true
---
時代遅れとなった [`<isindex>`](https://developer.mozilla.org/docs/Web/HTML/Element/isindex) HTML 要素と `<input name="isindex">` への対応が Firefox 56 で削除されました。これは HTML 標準や他のブラウザーからは既に削除されています。
