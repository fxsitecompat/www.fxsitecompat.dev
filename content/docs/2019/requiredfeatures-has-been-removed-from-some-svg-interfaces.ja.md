---
title: "一部の SVG インターフェイスから `requiredFeatures` が削除されました"
date: "2019-07-07T01:48:00-04:00"
categories: ["svg"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1295404"
      title: "Bug 1295404 - remove requiredFeatures from SVGTests"
---
Firefox 69 で、`SVGAnimationElement`、`SVGGraphicsElement`、`SVGImageElement` といった一部の SVG インターフェイスで実装されている `SVGTests` ミックスインインターフェイスから `requiredFeatures` プロパティが削除されました。このプロパティは SVG 1.1 仕様で定義されていましたが、その後 SVG 2.0 では削除されていました。また、既に [Google Chrome 59](https://www.chromestatus.com/feature/5720709590417408) で削除されています。
