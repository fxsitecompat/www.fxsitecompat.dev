---
title: "ほとんどの Firefox 固有の `-moz-appearance` 値が削除されました"
date: "2018-10-23T10:25:00-04:00"
categories: ["css"]
tags: []
versions: ["64", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496720"
      title: "Bug 1496720 - [css-compat] Unship -moz/webkit-appearance values not supported by other UAs / spec"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/odBz2i8xnno/discussion"
      title: "Intent to unship: most -moz-appearance values not supported by other UAs / spec"
---
他のブラウザーが対応しておらず仕様で標準化もされていない [`-moz-appearance`](https://developer.mozilla.org/docs/Web/CSS/appearance) CSS プロパティ値の大半が Firefox 64 で削除されました。これらは主に、既に廃止予定となった [XUL](https://developer.mozilla.org/docs/Mozilla/Tech/XUL) で記述されている Firefox のユーザーインターフェイス内で使われることを想定したものでした。Firefox 63 以降 `-webkit-appearance` プロパティが `-moz-appearance` のエイリアスとして実装されていることから、今回の削除は `-webkit-appearance` にも影響します。

[削除された値](https://hg.mozilla.org/try/diff/05e54dac9610/layout/style/test/test_non_content_accessible_values.html) には `radio-container`、`window`、`menulist-text` が含まれ、Mozilla 開発者によればこれらが [最もよく使われていた値](https://bugzilla.mozilla.org/show_bug.cgi?id=1496720#c14) でした。[残りの値](https://compat.spec.whatwg.org/#css-non-aliased) には `none` が含まれ、これはよくネイティブフォームウィジェットの既定スタイルを無効化するために用いられます。
