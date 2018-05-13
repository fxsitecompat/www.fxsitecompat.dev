---
title: "`HTMLCollection` が空白の文字列名に一致しなくなりました"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
versions: ["32"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=891952"
      title: "Bug 891952 – Update empty string handling in named getters to spec changes"
---
従来、`document.forms[0][""]` のような [`HTMLCollection`](https://developer.mozilla.org/docs/Web/API/HTMLCollection) オブジェクトの空白名プロパティは、`name` が付いていない 1 番目の子要素を返していました。この挙動は更新された仕様に合わせて変更され、`undefined` を返すようになりました。
