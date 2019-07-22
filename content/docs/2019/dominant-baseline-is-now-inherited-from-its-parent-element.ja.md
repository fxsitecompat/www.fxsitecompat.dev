---
title: "`dominant-baseline` が親要素から継承するようになりました"
date: "2019-07-21T20:10:00-04:00"
categories: ["css", "svg"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1353164"
      title: "Bug 1353164 - dominant-baseline will become inherited in SVG 2 (and CSS Inline 3)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JjSHhxIn1Wk/discussion"
      title: "Intent to change: dominant-baseline to inherit"
---
[`dominant-baseline`](https://developer.mozilla.org/docs/Web/SVG/Attribute/dominant-baseline) 属性は SVG 1.1 では継承しないものとされていましたが、SVG 2 では継承を行うようになっており、この属性は CSS 3 の `dominant-baseline` プロパティとして定義されています。Firefox 70 は現行の仕様に準拠するようこの継承の変更を行いました。
