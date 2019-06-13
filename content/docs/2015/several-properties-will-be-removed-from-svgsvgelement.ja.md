---
title: "`SVGSVGElement` からいくつかのプロパティが削除されます"
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
aliases:
    - "/ja/docs/2015/getelementbyid-and-several-properties-will-be-removed-from-svgsvgelement/"
---
[`SVGSVGElement`](https://developer.mozilla.org/docs/Web/API/SVGSVGElement) インターフェイスから、<del>`getElementById` メソッドと、</del>`useCurrentView`、`pixelUnitToMillimeterX`、`pixelUnitToMillimeterY`、`screenPixelToMillimeterX`、`screenPixelToMillimeterY` プロパティが削除されます。

また、[`SVGTests`](https://developer.mozilla.org/docs/Web/API/SVGTests) インターフェイスからは `hasExtension` メソッドが、`SVGGraphicsElement` インターフェイスからは `nearestViewportElement`、`farthestViewportElement` プロパティが、それぞれ削除されます。

**更新**: `getElementById` メソッドは最新の SVG 仕様で復活したため、Firefox から削除される予定はなくなりました。

**更新 2**: `pixelUnitToMillimeterX` と関連プロパティは [Firefox 61 で削除されました](https://www.fxsitecompat.dev/ja/docs/2018/pixelunittomillimeterx-and-similar-properties-have-been-removed-from-svgsvgelement/)。

**更新 3**: `hasExtension` メソッドは [Firefox 68 で削除されました](https://www.fxsitecompat.dev/ja/docs/2019/hasextension-has-been-removed-from-some-svg-interfaces/)。
