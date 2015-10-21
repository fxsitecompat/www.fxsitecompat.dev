---
title: "ICO 画像の実サイズとして最大リソースが採用されるようになりました"
date: "2015-09-25T03:09:00-04:00"
categories: ["misc"]
tags: []
versions: ["43"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1201796": "Bug 1201796 - Add downscale-during-decode support for the ICO decoder"
aliases:
    - "/docs/2015/ico-images-now-use-the-largest-frame-as-the-intrinsic-dimention/"
    - "/docs/2015/ico-images-now-use-the-largest-frame-as-the-intrinsic-dimension/"
---
これまで、複数のリソースを持つ ICO 形式画像 (favicon) のサイズはその最小リソースに基づいていました。これは通常 16×16px です。Firefox 43 以降では、最大リソースが画像の実サイズとして使われるようになりました。

この変更がタブやブックマークといったブラウザの UI に悪影響を与えることはないはずですが、`<img>` 要素、CSS `background-image` その他のプロパティを使って Web ページに埋め込まれている ICO 画像は、`width` と `height` が指定されていない限り異なるサイズで表示される可能性があります。
