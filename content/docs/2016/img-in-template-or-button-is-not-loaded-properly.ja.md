---
title: "`<template>` や `<button>` 内の `<img>` が正しく読み込まれません"
date: "2016-12-04T21:15:00-05:00"
categories: ["dom"]
tags: []
versions: ["50"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1317901"
      title: "Bug 1317901 - Cloned images from <template> do not load."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1318889"
      title: "Bug 1318889 - SVG inside <img> is not displayed in Firefox 50"
aliases:
    - "/ja/docs/2016/img-in-template-will-not-be-loaded-when-added-to-document/"
---
[`<template>`](https://developer.mozilla.org/docs/Web/HTML/Element/template) 内で定義されている画像が、その `<img>` 要素がテンプレートコンテンツから複製されアクティブなドキュメントのどこかへ追加された時点で正しく読み込まれないというリグレッションが Firefox 50 で発生しました。同じリグレッションが原因で、`<button>` 内の `<img>` も読み込まれません。それらの読み込まれなかった `<img>` には、もし指定されていれば代替テキストが代わりに表示されます。このバグは Firefox 50.1.0 で修正されました。
