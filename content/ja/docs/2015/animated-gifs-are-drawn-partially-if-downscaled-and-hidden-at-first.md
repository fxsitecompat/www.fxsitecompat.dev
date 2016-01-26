---
title: "アニメーション GIF が当初縮小され隠されていた場合に一部しか描画されません"
date: "2015-12-18T18:27:00-05:00"
categories: ["misc"]
tags: []
versions: ["43", "44", "45", "46", "47"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1233403": "Bug 1233403 - Animated GIFs are partially drawn if those are hidden at first"
aliases:
    - "/docs/2015/animated-gifs-are-drawn-partially-if-hidden-at-first/"
---
アニメーション GIF 画像が、ページ読み込み時に縮小表示され、また CSS で隠されていた場合、完全に描画されないというリグレッションが Firefox 43 で発生しました。Mozilla の開発者が解決策に取り組んでいます。
