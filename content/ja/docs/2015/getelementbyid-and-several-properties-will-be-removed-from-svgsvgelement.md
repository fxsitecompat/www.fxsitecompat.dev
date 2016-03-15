---
title: "
`SVGSVGElement` から `getElementById` といくつかのプロパティが削除されます"
date: "2015-10-28T01:11:00-07:00"
categories: ["svg"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133173"
      title: "Bug 1133173 - remove SVGSVGElement.getElementById"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1174097"
      title: "Bug 1174097 - remove SVGSVGElement.useCurrentView"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133175"
      title: "Bug 1133175 - remove SVGTests.hasExtension"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133172"
      title: "Bug 1133172 - remove SVGSVGElement.{pixel,screenPixel}UnitToMillimeter{X,Y}"
---
[`SVGSVGElement`](https://developer.mozilla.org/ja/docs/Web/API/SVGSVGElement) インタフェースから、`getElementById` メソッドと、`useCurrentView`、`pixelUnitToMillimeterX`、`pixelUnitToMillimeterY`、`screenPixelToMillimeterX`、`screenPixelToMillimeterY` プロパティが削除されます。

また、[`SVGTests`](https://developer.mozilla.org/ja/docs/Web/API/SVGTests) インタフェースからは `hasExtension` メソッドが、`SVGGraphicsElement` インタフェースからは `nearestViewportElement`、`farthestViewportElement` プロパティが、それぞれ削除されます。
