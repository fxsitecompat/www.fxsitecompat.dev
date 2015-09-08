---
title: "未知の SVG 要素は `SVGElement` となります"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: "22"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=840417": "Bug 840417 – Unknown SVG Elements should be SVGElement, not SVGUnknownElement"
---
未知の SVG 要素が [`SVGUnknownElement`](https://developer.mozilla.org/ja/docs/Web/API/SVGUnknownElement) の代わりに [`SVGElement`](https://developer.mozilla.org/ja/docs/Web/API/SVGElement) となります。
