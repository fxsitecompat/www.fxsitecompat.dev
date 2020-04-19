---
title: "`bgsound`、`multicol`、`image` のタグ名を持つ HTML 要素が `HTMLSpanElement` インターフェイスを使用しなくなりました"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
releases: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=844127"
      title: "Bug 844127 – Stop using the HTMLSpanElement interface for bgsound, multicol, image"
---
従来、これらのタグ名のいずれかで HTML 要素を生成すると [`HTMLSpanElement`](https://developer.mozilla.org/docs/Web/API/HTMLSpanElement) が生成されていました。今後は、仕様に従い、[`<bgsound>`](https://developer.mozilla.org/docs/Web/HTML/Element/bgsound) と [`<multicol>`](https://developer.mozilla.org/docs/Web/HTML/Element/multicol) は [`HTMLUnknownElement`](https://developer.mozilla.org/docs/Web/API/HTMLUnknownElement)、[`<image>`](https://developer.mozilla.org/docs/Web/HTML/Element/image) は [`HTMLElement`](https://developer.mozilla.org/docs/Web/API/HTMLElement) となります。
