---
title: "`<altGlyph>` 対応が打ち切られました"
date: "2016-05-10T19:51:00-04:00"
categories: ["svg"]
tags: []
releases: ["49", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1260032"
      title: "Bug 1260032 - drop support for altGlyph"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/LcN2jd9gGiM/discussion"
      title: "Intent to unship support for altGlyph"
supported_tools:
  firefox_extension: true
---
[`<altGlyph>`](https://developer.mozilla.org/docs/Web/SVG/Element/altGlyph) 要素は SVG2 仕様から削除されたため、Firefox での対応も打ち切られました。この要素は代わりに使用できる [`<tspan>`](https://developer.mozilla.org/docs/Web/SVG/Element/tspan) のエイリアスとなっていました。
