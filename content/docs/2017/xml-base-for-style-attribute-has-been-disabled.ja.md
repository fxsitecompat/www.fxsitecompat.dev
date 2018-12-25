---
title: "`style` 属性向け `xml:base` が無効化されました"
date: "2017-03-26T02:51:00-04:00"
categories: ["css", "misc"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1349024"
      title: "Bug 1349024 - Turn off xml:base for style attribute by default on aurora and nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1350521"
      title: "Bug 1350521 - Turn off xml:base for style attribute by default for all channels"
    - url: "https://groups.google.com/d/topic/mozilla.compatibility/z2syZhkI1-U/discussion"
      title: "Intent to Deprecate: xml:base for CSS style attributes"
---
以下の例が示すような CSS `style` 属性向けの [`xml:base`](https://www.w3.org/TR/xmlbase/) 対応が、Firefox 55 の初期設定で無効化されました。[Firefox 53 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2017/xml-base-attribute-has-been-deprecated/) `xml:base` 属性には他のどのブラウザーも対応していないことから、互換性リスクは非常に低いはずです。

```html
<div xml:base="https://example.com/"
     style="background:url(picture.jpg)"></div>
```

**更新**: この属性対応は [Firefox 66](https://www.fxsitecompat.com/ja/docs/2018/xml-base-attribute-is-no-longer-supported/) で完全に削除されました。
