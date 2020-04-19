---
title: "`id` 付き画像が `window` プロパティとして現れなくなりました"
date: "2015-10-21T00:53:00-07:00"
categories: ["dom"]
tags: []
versions: ["42", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=959992"
      title: "Bug 959992 - Firefox 26 creates enumerable properties on window for ids of <img> tags"
aliases:
    - "/ja/docs/2015/imgs-with-id-no-longer-appear-as-window-properties/"
---
Firefox 26 以降、`id` 属性を持つ [`<img>`](https://developer.mozilla.org/docs/Web/HTML/Element/img) 要素は HTML 仕様に従って [`window`](https://developer.mozilla.org/docs/Web/API/Window) オブジェクト上の加算プロパティとして現れていました。そのため、例えば `<img id="logo">` は `window.logo` プロパティを通じてアクセス可能でした。その後仕様が変更され、Safari や Chrome と同じ以前の挙動に戻されました。Firefox 42 の実装もそれに従って更新されたため、そうした画像は `window` 上に現れなくなりました。
