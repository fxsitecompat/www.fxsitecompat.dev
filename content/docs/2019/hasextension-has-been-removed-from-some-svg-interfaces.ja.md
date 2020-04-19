---
title: "一部の SVG インターフェイスから `hasExtension()` が削除されました"
date: "2019-05-27T23:39:00-04:00"
categories: ["svg"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133175"
      title: "Bug 1133175 - remove SVGTests.hasExtension"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/WLNCdEM1x44/discussion"
      title: "Intent to unship: hasFeature() method on some SVG elements"
---
Firefox 68 で、`SVGAnimationElement`、`SVGGraphicsElement`、`SVGImageElement` といった一部の SVG インターフェイスで実装されている `SVGTests` ミックスインインターフェイスから `hasExtension` メソッドが削除されました。このメソッドは SVG 1.1 仕様で定義されていましたが、その後 SVG 2.0 では削除されていました。また、既に [Google Chrome 47](https://www.chromestatus.com/feature/5473526421127168) で削除されています。
