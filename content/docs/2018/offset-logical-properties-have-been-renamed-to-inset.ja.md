---
title: "`offset-*` 論理プロパティが `inset-*` に改名されました"
date: "2018-08-15T02:08:00-04:00"
categories: ["css"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1464782"
      title: "Bug 1464782 - [css-logical] rename offset-* properties to inset-block-start, inset-block-end, inset-inline-start and inset-inline-end"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1471838"
      title: "Bug 1471838 - Turn layout.css.offset-logical-properties.enabled off by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/mG6Wpz5C2PM/discussion"
      title: "Intent to deprecate and remove: offset-* logical properties."
---
最新の CSS Logical Properties and Values 仕様に従い、Firefox 63 で以下の論理プロパティが改名されました。これらは今のところ Firefox にしか実装されておらず、まだ広く使われていないことから、この変更は移行期間なしに行われました。

* [`offset-block-start`](https://developer.mozilla.org/docs/Web/CSS/offset-block-start) → `inset-block-start`
* [`offset-block-end`](https://developer.mozilla.org/docs/Web/CSS/offset-block-end) → `inset-block-end`
* [`offset-inline-start`](https://developer.mozilla.org/docs/Web/CSS/offset-inline-start) → `inset-inline-start`
* [`offset-inline-end`](https://developer.mozilla.org/docs/Web/CSS/offset-inline-end) → `inset-inline-end`
