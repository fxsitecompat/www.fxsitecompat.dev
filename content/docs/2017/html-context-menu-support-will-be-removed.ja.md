---
title: "HTML コンテキストメニュー対応が廃止されます"
date: "2017-07-17T14:06:00-04:00"
categories: ["html"]
tags: []
releases: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1372276"
      title: "Bug 1372276 - Remove HTML context menu (<menu> and <menuitem> tag) support"
---
Firefox 8 で導入された [HTML5 コンテキストメニュー](https://hacks.mozilla.org/2011/11/html5-context-menus-in-firefox-screencast-and-code/) への対応は近々削除されます。他のブラウザーベンダーが関心を示さなかったため、この機能は既に HTML 仕様から削除されました。現在 Firefox が [`<menu>`](https://developer.mozilla.org/docs/Web/HTML/Element/menu)、[`<menuitem>`](https://developer.mozilla.org/docs/Web/HTML/Element/menuitem) 要素や [`contextmenu`](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/contextmenu) グローバル属性を実装している唯一のブラウザーとなっています。

必要であれば、*Google Drive* など一部のリッチウェブアプリケーションに見られるように、独自のコンテキストメニューを代わりに作成できます。[WAI-ARIA](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 標準が [アクセシブルなメニュー](https://www.w3.org/WAI/GL/wiki/Using_ARIA_menus) を作成する方法を提供しており、これを使用することを強くお勧めします。
