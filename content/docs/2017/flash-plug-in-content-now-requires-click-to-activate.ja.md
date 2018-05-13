---
title: "Flash プラグインコンテンツは有効化のためクリックが必要となりました"
date: "2017-05-17T22:06:00-05:00"
categories: ["plugins"]
tags: []
versions: ["55"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1317856"
      title: "Bug 1317856 - Make Flash plugin click-to-play (aka \"Ask to Activate\")"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1365714"
      title: "Bug 1365714 - Release Flash plugin Click-to-Play (aka \"Ask to Activate\")"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1390703"
      title: "Bug 1390703 - Bump Flash Click-to-Play rollout to 25% on release"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1390705"
      title: "Bug 1390705 - Bump Flash Click-to-Play rollout to 100% on release"
    - url: "https://www.mozilla.jp/blog/entry/10554/"
      title: "Firefox 内での Adobe Flash 使用量を削減します"
aliases:
    - "/ja/docs/2016/flash-content-will-be-click-to-activate-in-2017/"
---
Firefox で現在進行中の [NPAPI プラグイン廃止](https://www.fxsitecompat.com/ja/categories/plugins/) の一環として、Flash コンテンツは Firefox Nightly の初期設定で「クリックして有効化」となりました。この変更は、[`SharedArrayBuffer`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/SharedArrayBuffer)、[WebAssembly](https://developer.mozilla.org/docs/WebAssembly)、[WebGL 2.0](https://developer.mozilla.org/docs/Web/API/WebGL2RenderingContext) といった高度な標準技術がいくつか実装され、一般に使用できるようになったことを踏まえて行われました。

今のところ、Firefox 55 の Beta、Release 両チャンネルのユーザーへ段階的にこの変更を展開していく予定です。ウェブコンテンツ提供者は、最良のユーザー体験を提供するため、Flash 依存をやめるための明確な計画を立てるべきです。

**更新**: この変更は 9 月 20 日時点ですべての Firefox 55 ユーザーへ展開されました。
