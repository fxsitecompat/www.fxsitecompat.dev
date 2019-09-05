---
title: "様々な古い MathML 機能が廃止予定となったか削除されました"
date: "2019-09-05T01:34:00-04:00"
categories: ["misc"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548524"
      title: "Bug 1548524 - Remove attributes deprecated from MathML3"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548527"
      title: "Bug 1548527 - Remove \"small\" \"normal\" \"big\" values of mathsize"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548529"
      title: "Bug 1548529 - Remove values \"thin\", \"thick\", \"medium\" values of mfrac@linethickness"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1573438"
      title: "Bug 1573438 - Remove <math>'s mode attribute"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1574749"
      title: "Bug 1574749 - Remove support for nonzero unitless lengths"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1574750"
      title: "Bug 1574750 - Remove support for MathML length values thinmathspace, mediummathspace, thickmathspace, etc"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1575542"
      title: "Bug 1575542 - Add counter and warnings for deprecated MathML lengths"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1575596"
      title: "Bug 1575596 - MathML Lengths: Do not accept numbers ending with a dot"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/kl5c87mBlO0/discussion"
      title: "Intent to unship: Deprecated MathML style attributes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/kyB34PjYXek/discussion"
      title: "Intent to deprecate: named values the mathsize attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/G91-vBeC3Rw/discussion"
      title: "Intent to deprecate: named values for <mfrac>'s linethickness attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/lZUF2Z9jOh4/discussion"
      title: "Intent to unship: <math>'s mode attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/-yV6wb3klSA/discussion"
      title: "Intent to unship: nonzero unitless MathML lengths"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/yEMdIOo4i-0/discussion"
      title: "Intent to deprecate: mathspace names for MathML lengths"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wIjm9JjVHNg/discussion"
      title: "Intent to unship: Legacy MathML syntax for numbers"
aliases:
    - "/ja/docs/2019/mode-attribute-on-math-has-been-removed/"
---
現行の MathML Core (将来の MathML 4) 仕様へ準拠する作業に進捗があり、Firefox 70 で MathML 実装が更新されました。

以下の機能は WebKit にも実装されていますが、廃止予定とされたため、Firefox Nightly では無効化され、将来的に削除されます。

* [`<mfrac>`](https://developer.mozilla.org/docs/Web/MathML/Element/mfrac) 要素上の `linethickness` 属性向け名前付き値: `thin`、`medium`、`thick`
* [`<mtext>`](https://developer.mozilla.org/docs/Web/MathML/Element/mtext) やその他の要素上の `mathsize` 属性向け名前付き値: `small`、`normal`、`big`.
* 名前付き長さ値: `veryverythinmathspace`、`verythinmathspace`、`thinmathspace`、`mediummathspace`、`thickmathspace`、`verythickmathspace`、`veryverythickmathspace`、`negativeveryverythinmathspace`、`negativeverythinmathspace`、`negativethinmathspace`、`negativemediummathspace`、`negativethickmathspace`、`negativeverythickmathspace`、`negativeverythickmathspace`。必要に応じて [この計算式](https://github.com/mathml-refresh/mathml/issues/75#issuecomment-523016332) を参照してください
* スタイル属性: `background`、`color`、`fontfamily`、`fontsize`、`fontstyle`、`fontweight`。これらは Firefox 20 以降廃止予定となっています。代わりに `mathbackground`、`mathcolor`、`mathsize`、`mathvariant` を使ってください

以下の機能は削除されました。

* [`<math>`](https://developer.mozilla.org/docs/Web/MathML/Element/math) 要素上の `mode` 属性。Firefox にしか実装されておらず、`display` 属性に置き換えられる形で Firefox 20 以降廃止予定となっていました。古いドキュメント向けに [ポリフィル](https://github.com/mathml-refresh/mathml/issues/5#issuecomment-521525157) が公開されています。
* ゼロ以外の単位なし長さ値、例えば 500% として解釈される `5` など。Firefox 20 以降廃止予定となっていました
* ドットで終わる長さ値、例えば `2.` や `34.px` など
