---
title: "`pixelUnitToMillimeterX` と関連プロパティが `SVGSVGElement` から削除されました"
date: "2018-04-22T17:47:00-04:00"
categories: ["dom", "svg"]
tags: []
versions: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133172"
      title: "Bug 1133172 - remove SVGSVGElement.{pixel,screenPixel}UnitToMillimeter{X,Y}"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/-Vhlz6uEVOA/discussion"
      title: " Intent to unship: SVGSVGElement.{pixel, screenPixel}UnitToMillimeter{X, Y} "
---
`pixelUnitToMillimeterX`、`pixelUnitToMillimeterY`、`screenPixelToMillimeterX`、`screenPixelToMillimeterY` プロパティが [`SVGSVGElement`](https://developer.mozilla.org/docs/Web/API/SVGSVGElement) インターフェイスから削除されました。これらは SVG 1.1 仕様で定義されていましたが、使用例がないことから SVG 2 では削除されています。2015 年 12 月公開の [Google Chrome 47](https://www.chromestatus.com/feature/5478103916740608) で既に削除されていることから、互換性リスクは低いはずです。
