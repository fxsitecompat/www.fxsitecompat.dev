---
title: "レスポンシブなページ上でタッチとマウスイベントの間の遅延が廃止されました"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30", "31-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=941995"
      title: "Bug 941995 – Remove 300ms touch > mouse events delay for double-tap zoom on \"responsive\" pages"
---
[Firefox for Android](https://developer.mozilla.org/Firefox_for_Android) と [Firefox OS](https://developer.mozilla.org/Firefox_OS) はいずれもダブルタップによる拡大表示に対応しており、このジェスチャーを判定し有効化するため、タッチイベント ([`touchend`](https://developer.mozilla.org/docs/Web/Reference/Events/touchend)) とマウスイベント ([`click`](https://developer.mozilla.org/docs/Web/Reference/Events/click)) の間には 300 ミリ秒の遅延が設定されています。アプリケーションの応答性を高めるため、[viewport `<meta>` タグ](https://developer.mozilla.org/docs/Mozilla/Mobile/Viewport_meta_tag) で `width=device-width` (あるいは `device-width` よりも小さい値) か `user-scalable=no` が指定されている拡大不可能な [レスポンシブデザイン](https://developer.mozilla.org/docs/Web_Development/Mobile/Responsive_design) のページでは、この遅延が廃止されました。Google Chrome 32 も同様に遅延を廃止しています。詳しくは [HTML5 Rocks の記事](https://developers.google.com/web/updates/2013/12/300ms-tap-delay-gone-away) を参照してください。
