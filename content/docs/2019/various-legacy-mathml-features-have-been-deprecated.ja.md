---
title: "様々な古い MathML 機能が廃止予定となりました"
date: "2019-10-07T08:03:00-04:00"
categories: ["misc"]
tags: []
versions: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548522"
      title: "Bug 1548522 - Remove support for the menclose's \"radical\" notation"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548530"
      title: "Bug 1548530 - Remove support for numalign/denomalign/align attributes"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1575870"
      title: "Bug 1575870 - Remove support for XLink on MathML elements"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1587570"
      title: "Bug 1587570 - Remove support for the subscriptshift and superscriptshift attributes"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1587572"
      title: "Bug 1587572 - Remove support for the mfrac@bevelled attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vwAkuZIEhnY/discussion"
      title: "Intent to unship: MathML menclose notation \"radical\""
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JnJVGTmIwPE/discussion"
      title: "Intent to unship: MathML alignment attributes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/70NFnet82cU/discussion"
      title: "Intend to deprecate: XLink attributes on MathML elements"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/CAqw0Nxw6Pg/discussion"
      title: "Intent to deprecate: MathML subscriptshift and superscriptshift attributes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/9pEvlYn-Xyw/discussion"
      title: "Intent to deprecate: MathML bevelled attribute"
---
[Firefox 70](https://www.fxsitecompat.dev/ja/docs/2019/various-legacy-mathml-features-have-been-deprecated-or-removed/) と同様に、現行の MathML Core (将来の MathML 4) 仕様に合わせ、Firefox 71 で MathML 実装が更新されました。以下の機能は廃止予定とされたため、Firefox Nightly では無効化され、将来的に削除されます。

* [`<munderover>`](https://developer.mozilla.org/docs/Web/MathML/Element/munderover)、[`<munder>`](https://developer.mozilla.org/docs/Web/MathML/Element/munder)、[`<mover>`](https://developer.mozilla.org/docs/Web/MathML/Element/mover) 要素上の `align` 属性
* [`<mfrac>`](https://developer.mozilla.org/docs/Web/MathML/Element/mfrac) 要素上の `bevelled`、`denomalign`、`numalign` 属性
* [`<menclose>`](https://developer.mozilla.org/docs/Web/MathML/Element/menclose) 要素上の `notation` 属性向け `radical` 値。[`<msqrt>`](https://developer.mozilla.org/docs/Web/MathML/Element/msqrt) で代用してください
* [`<msubsup>`](https://developer.mozilla.org/docs/Web/MathML/Element/msubsup)、[`<msub>`](https://developer.mozilla.org/docs/Web/MathML/Element/msub)、[`<msup>`](https://developer.mozilla.org/docs/Web/MathML/Element/msup) 要素上の `subscriptshift`、`superscriptshift` 両属性
* MathML 要素上の [XLink](https://developer.mozilla.org/docs/Glossary/XLink) 属性: `xlink:actuate`、`xlink:href`、`xlink:show`、`xlink:type`。`xlink:href` の代わりに `href` 属性が使用可能です
