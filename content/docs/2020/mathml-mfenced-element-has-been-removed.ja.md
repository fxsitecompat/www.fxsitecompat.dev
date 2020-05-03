---
title: "MathML `<mfenced>` 要素が廃止されました"
date: "2020-01-05T17:02:00-05:00"
categories: ["misc"]
tags: []
releases: ["73"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1603773"
      title: "Bug 1603773 - Disable the MathML mfenced element by default in all builds"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/SJFrpa-UmQk/discussion"
      title: "Intent to unship: MathML mfenced element"
supported_tools:
  firefox_extension: true
---
[Firefox 71](https://www.fxsitecompat.dev/ja/docs/2019/various-legacy-mathml-features-have-been-deprecated/) 以降廃止予定となっていた MathML [`<mfenced>`](https://developer.mozilla.org/docs/Web/MathML/Element/mfenced) 要素が Firefox 73 で廃止されました。[`<mrow>`](https://developer.mozilla.org/docs/Web/MathML/Element/mrow) と [`<mo>`](https://developer.mozilla.org/docs/Web/MathML/Element/mo) 要素で代用してください。
