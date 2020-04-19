---
title: "透過 RGBA カラー値が `transparent` キーワードへ変換されなくなりました"
date: "2017-02-21T18:30:00-05:00"
categories: ["css", "dom"]
tags: []
releases: ["54", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1339394"
      title: "Bug 1339394 - Don't serialize transparent colors to \"transparent\" keyword in various cases"
---
Firefox は従来、[`HTMLElement.prototype.style`](https://developer.mozilla.org/docs/Web/API/HTMLElement/style) プロパティで取得可能な [指定値](https://developer.mozilla.org/docs/Web/CSS/specified_value) に関して、`rgba(0, 0, 0, 0)` を `transparent` キーワードへ誤って変換 (シリアライズ) していました。また、[`window.getComputedStyle`](https://developer.mozilla.org/docs/Web/API/Window/getComputedStyle) メソッドによって返される [解決値](https://developer.mozilla.org/docs/Web/CSS/resolved_value) に関しては、ゼロアルファチャンネルを持つあらゆるカラー値が `transparent` へ変換されていました。

こうした実装は仕様や他のブラウザーの挙動と一致しないため、このバグは Firefox 54 で修正されました。
