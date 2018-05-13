---
title: "`HTMLInputElement.width` と `height` が、`type` が `image` 以外の場合に `0` を返すようになりました"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: ["26"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=905240"
      title: "Bug 905240 – HTMLInputElement.{width,height} getter should return 0 for type!=\'image\'"
---
従来、[`<input>`](https://developer.mozilla.org/docs/Web/HTML/Element/input) の `width`、`height` 両プロパティは、その要素のサイズを返していました。仕様に準拠するため、それらのプロパティは、`type` 属性が `image` でない場合には `0` を返すようになりました。
