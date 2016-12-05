---
title: "`<template>` 内の `<img>` がドキュメントへ追加された際に読み込まれません"
date: "2016-12-04T21:15:00-05:00"
categories: ["dom"]
tags: []
versions: ["50"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1317901"
      title: "Bug 1317901 - Cloned images from <template> do not load."
---
[`<template>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/template) 内で定義されている画像が、その `<img>` 要素がテンプレートコンテンツから複製されアクティブなドキュメントのどこかへ追加された時点で正しく読み込まれないというリグレッションが Firefox 50 で発生しました。それらの読み込まれなかった `<img>` には、もし指定されていれば代替テキストが代わりに表示されます。このバグは Firefox 50.1.0 で修正されます。
