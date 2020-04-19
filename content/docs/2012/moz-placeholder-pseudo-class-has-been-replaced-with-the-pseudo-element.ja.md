---
title: "`:-moz-placeholder` 疑似クラスが疑似要素に置き換えられました"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
versions: ["19", "24-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=737786"
      title: "Bug 737786 – Switch from :-moz-placeholder to ::-moz-placeholder (pseudo-class to pseudo-element)"
---
[`placeholder`](https://developer.mozilla.org/docs/HTML/HTML5/Forms_in_HTML5#placeholder_.E5.B1.9E.E6.80.A7) 属性付きのフォーム要素にマッチする [`:-moz-placeholder`](https://developer.mozilla.org/docs/CSS/:-moz-placeholder) 疑似クラスが削除され、代わりに [`::-moz-placeholder`](https://developer.mozilla.org/docs/CSS/::-moz-placeholder) 疑似要素が追加されました。WebKit の実装は元々疑似要素となっており、今回の変更は標準化へ向けた作業の一環です。
