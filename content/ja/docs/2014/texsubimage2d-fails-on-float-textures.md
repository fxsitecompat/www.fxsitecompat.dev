---
title: "`texSubImage2D` が浮動小数点テクスチャ上でエラーとなります"
date: "2014-02-07T11:57:09-05:00"
categories: ["webgl"]
tags: ["regression"]
versions: "29"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1003607": "Bug 1003607 – Header animation at acko.net is broken in FF 29 and above."
---
[`WebGLRenderingContext`](https://developer.mozilla.org/ja/docs/Web/API/WebGLRenderingContext) インタフェース上の `texSubImage2D` メソッドが、`OES_texture_float` 拡張機能で作成された浮動小数点テクスチャの更新に使われた場合にうまくいかず、「format or type doesn't match the existing texture」といったエラーを投げます。この問題は Firefox 31 で修正されました。
