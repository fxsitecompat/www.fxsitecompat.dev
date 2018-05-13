---
title: "`CSSStyleDeclaration.getPropertyCSSValue()` が廃止予定となりました"
date: "2018-03-16T18:09:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=474655"
      title: "Bug 474655 - warn when nsIDOMCSSStyleDeclaration::GetPropertyCSSValue is called"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1448415"
      title: "Bug 1448415 - Hide getPropertyCSSValue on Nightly."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1461092"
      title: "Bug 1461092 - Unship GetPropertyCSSValue in beta."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/qu5JekiuSfw/discussion"
      title: "Intent to unship: CSSStyleDeclaration.getPropertyCSSValue"
---
`CSSStyleDeclaration` インターフェイス上の [`getPropertyCSSValue`](https://developer.mozilla.org/docs/Web/API/CSSStyleDeclaration/getPropertyCSSValue) メソッド対応が廃止予定となり、近い将来削除されることとなりました。2003 年以降 [旧式扱いとなっている](https://lists.w3.org/Archives/Public/www-style/2003Oct/0347.html) このメソッドに対して、Firefox 61 以降ではコンソールに警告が表示されます。Google Chrome は既に 2014 年の時点で [対応を廃止](https://groups.google.com/a/chromium.org/d/topic/blink-dev/3VmxWFzcyJc/discussion) しています。[`getPropertyValue`](https://developer.mozilla.org/docs/Web/API/CSSStyleDeclaration/getPropertyValue) メソッドを代わりに使用してください。

**更新**: このメソッドは Firefox 61 以降 Nightly チャンネルでは無効化されました。

**更新 2**: このメソッドは Firefox 61 以降 Firefox Beta および Developer Edition でも無効化されました。

**更新 3**: このメソッドは [Firefox 62 で完全に削除されました](https://www.fxsitecompat.com/ja/docs/2018/cssstyledeclaration-getpropertycssvalue-has-been-removed/)。
