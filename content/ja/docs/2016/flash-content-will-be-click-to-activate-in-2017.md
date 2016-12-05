---
title: "Flash コンテンツは 2017 年中に「クリックして有効化」となります"
date: "2016-12-04T21:10:00-05:00"
categories: ["plugins"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1317856"
      title: "Bug 1317856 - Make Flash plugin click-to-play (aka \"Ask to Activate\")"
    - url: "https://www.mozilla.jp/blog/entry/10554/"
      title: "Firefox 内での Adobe Flash 使用量を削減します"
---
Firefox で現在進行中の [NPAPI プラグイン廃止](https://www.fxsitecompat.com/ja/categories/plugins/) の一環として、Flash コンテンツは 2017 年中のいずれかの時点において初期設定で「クリックして有効化」となります。この変更は、[`SharedArrayBuffer`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/SharedArrayBuffer)、[WebAssembly](https://hacks.mozilla.org/category/webassembly/)、[WebGL 2.0](https://developer.mozilla.org/ja/docs/Web/API/WebGL2RenderingContext) といったさらに高度な標準技術がいくつか実装され、一般に使用できるようになった時点で行われます。最良のユーザー体験を提供するため、ウェブコンテンツ提供者は Flash 依存をやめるための明確な計画を立てるべきです。

なお、Flash 以外のプラグイン対応は [Firefox 52](https://www.fxsitecompat.com/ja/docs/2016/plug-in-support-has-been-dropped-other-than-flash/) で既に削除されています。
