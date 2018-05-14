---
title: "`window` オブジェクト上のインデックス付きプロパティ (`iframe` など) が列挙可能になりました"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: ["21"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=823228"
      title: "Bug 823228 - Move indexed properties from nsWindowSH::GetProperty to the outer window proxy"
---
従来、DOM 内の [`<iframe>`](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) を [`window`](https://developer.mozilla.org/docs/Web/API/window) オブジェクト上で列挙することはできませんでした。この挙動が仕様に準拠するよう修正され、`Object.keys(window)` でそれらのフレームが返されるようになりました。ドキュメントへの `iframe` の追加によって `window` オブジェクト上の列挙可能なキーが変更されることになるため、グローバルリーク判別のようなことを行っている場合、今回の変更点には注意する必要があるでしょう。
