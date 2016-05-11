---
title: "`<altGlyph>` 対応が打ち切られました"
date: "2016-05-10T19:51:00-04:00"
categories: ["svg"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1260032"
      title: "Bug 1260032 - drop support for altGlyph"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/LcN2jd9gGiM/discussion"
      title: "Intent to unship support for altGlyph"
---
[`<altGlyph>`](https://developer.mozilla.org/ja/docs/Web/SVG/Element/altGlyph)、[`<altGlyphDef>`](https://developer.mozilla.org/ja/docs/Web/SVG/Element/altGlyphDef)、[`<altGlyphItem>`](https://developer.mozilla.org/ja/docs/Web/SVG/Element/altGlyphItem) の各要素は SVG2 仕様から削除されたため、Firefox での対応も打ち切られました。`<altGlyph>` は代わりに使用できる [`<tspan>`](https://developer.mozilla.org/ja/docs/Web/SVG/Element/tspan) のエイリアスとなっていました。
