---
title: "`CSSStyleDeclaration.getPropertyCSSValue()` と関連インターフェイスが削除されました"
date: "2018-05-08T16:01:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1408301"
      title: "Bug 1408301 - unship CSSStyleDeclaration::getPropertyCSSValue"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1459871"
      title: "Bug 1459871 - Remove other getPropertyCssValue-related interfaces."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/qu5JekiuSfw/discussion"
      title: "Intent to unship: CSSStyleDeclaration.getPropertyCSSValue"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/3BAUfGbtWC4/discussion"
      title: "Intent to unship: getPropertyCSSValue-related interfaces Rect, RGBColor, CSSValue, CSSPrimitiveValue and CSSValueList"
aliases:
    - "/ja/docs/2018/cssstyledeclaration-getpropertycssvalue-has-been-removed/"
---
[Firefox 61](https://www.fxsitecompat.dev/ja/docs/2018/cssstyledeclaration-getpropertycssvalue-has-been-deprecated/) で廃止予定となっていた `CSSStyleDeclaration` インターフェイス上の古い [`getPropertyCSSValue`](https://developer.mozilla.org/docs/Web/API/CSSStyleDeclaration/getPropertyCSSValue) メソッドへの対応が、Firefox 62 で削除されました。標準の [`getPropertyValue`](https://developer.mozilla.org/docs/Web/API/CSSStyleDeclaration/getPropertyValue) メソッドを代わりに使ってください。Google Chrome は 2014 年の時点で既に [対応を廃止](https://groups.google.com/a/chromium.org/d/topic/blink-dev/3VmxWFzcyJc/discussion) していることから、現時点で互換性リスクは非常に低いはずです。

**更新**: 次の関連インターフェイスも併せて削除されました: [`CSSPrimitiveValue`](https://developer.mozilla.org/docs/Web/API/CSSPrimitiveValue)、[`CSSValue`](https://developer.mozilla.org/docs/Web/API/CSSValue)、[`CSSValueList`](https://developer.mozilla.org/docs/Web/API/CSSValueList)、`Rect`、`RGBColor`
