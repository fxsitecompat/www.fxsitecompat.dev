---
title: "接頭辞付き `cursor` タイプは削除されます"
date: "2015-10-27T18:38:00-07:00"
categories: ["css"]
tags: []
releases: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=879119"
      title: "Bug 879119 - Drop support for -moz-prefixes from cursor: zoom-in | zoom-out | grab | grabbing"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JhnttZThqts/discussion"
      title: "Intent to unship: -moz-prefixed CSS cursor:zoom-in, zoom-out, grab, grabbing"
---
接頭辞付き CSS [`cursor`](https://developer.mozilla.org/docs/Web/CSS/cursor) プロパティの値、`-moz-zoom-in`、`-moz-zoom-out`、`-moz-grab`、`-moz-grabbing` は、将来的に削除されます。[Firefox 24](https://www.fxsitecompat.dev/ja/docs/2013/cursor-moz-zoom-in-and-moz-zoom-out-have-been-unprefixed/) で `zoom-in` と `zoom-out`、[Firefox 27](https://www.fxsitecompat.dev/ja/docs/2013/moz-grab-and-moz-grabbing-have-been-unprefixed/) で `grab` と `grabbing` の接頭辞が外れています。
