---
title: "
`SVGSVGElement` から `getElementById` といくつかのプロパティが削除されます"
date: "2015-10-28T01:11:00-07:00"
categories: ["svg"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1133173": "Bug 1133173 - remove SVGSVGElement.getElementById"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1174097": "Bug 1174097 - remove SVGSVGElement.useCurrentView"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1133175": "Bug 1133175 - remove SVGTests.hasExtension"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1133172": "Bug 1133172 - remove SVGSVGElement.{pixel,screenPixel}UnitToMillimeter{X,Y}"
---
[`SVGSVGElement`](https://developer.mozilla.org/ja/docs/Web/API/SVGSVGElement) インタフェースから、`getElementById` メソッドと、`useCurrentView`、`pixelUnitToMillimeterX`、`pixelUnitToMillimeterY`、`screenPixelToMillimeterX`、`screenPixelToMillimeterY` プロパティが削除されます。

また、[`SVGTests`](https://developer.mozilla.org/ja/docs/Web/API/SVGTests) インタフェースからは `hasExtension` メソッドが、`SVGGraphicsElement` インタフェースからは `nearestViewportElement`、`farthestViewportElement` プロパティが、それぞれ削除されます。
