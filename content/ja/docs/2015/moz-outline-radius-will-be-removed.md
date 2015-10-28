---
title: "`-moz-outline-radius` が削除されます"
date: "2015-10-27T18:02:00-07:00"
categories: ["css"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=315209": "Bug 315209 - outline should follow shape of border-radius (remove -moz-outline-radius)"
---
非標準の [`-moz-outline-radius`](https://developer.mozilla.org/ja/docs/Web/CSS/-moz-outline-radius)、[`-moz-outline-radius-topright`](https://developer.mozilla.org/ja/docs/Web/CSS/-moz-outline-radius-topright)、[`-moz-outline-radius-topleft`](https://developer.mozilla.org/ja/docs/Web/CSS/-moz-outline-radius-topleft)、[`-moz-outline-radius-bottomright`](https://developer.mozilla.org/ja/docs/Web/CSS/-moz-outline-radius-bottomright)、[`-moz-outline-radius-bottomleft`](https://developer.mozilla.org/ja/docs/Web/CSS/-moz-outline-radius-bottomleft) CSS プロパティは、仕様に含まれていないため、将来的に削除されます。[`outline`](https://developer.mozilla.org/ja/docs/Web/CSS/outline) は [`border-radius`](https://developer.mozilla.org/ja/docs/Web/CSS/border-radius) の形に従うべきです。
