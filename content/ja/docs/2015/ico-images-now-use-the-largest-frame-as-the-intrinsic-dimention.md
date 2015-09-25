---
title: "ICO 画像の実サイズが最大フレームに変わりました"
date: "2015-09-25T03:09:00-04:00"
categories: ["misc"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1201796": "Bug 1201796 - Add downscale-during-decode support for the ICO decoder"
---
これまで、複数のフレームを持つ ICO 形式画像 (favicon) のサイズはその最小フレームに基づいていました。これは通常 16×16px の favicon です。Firefox 44 以降では、最大フレームが画像の実サイズとして使われるようになりました。

この変更がタブやブックマークといったブラウザの UI に悪影響を与えることはないはずですが、`<img>` 要素、CSS `background-image` その他のプロパティを使って Web ページに埋め込まれている ICO 画像は、`width` と `height` が指定されていない限り異なるサイズで表示される可能性があります。
