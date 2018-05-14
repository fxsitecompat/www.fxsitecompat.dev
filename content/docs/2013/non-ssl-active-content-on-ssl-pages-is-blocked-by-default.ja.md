---
title: "SSL ページ上での非 SSL アクティブコンテンツは初期設定でブロックされます"
date: "2013-04-06T04:52:59-04:00"
categories: ["privacy-security"]
tags: []
versions: ["23"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=834836"
      title: "Bug 834836 – Turn on pref to block mixed active content"
---
[Firefox 18](https://www.fxsitecompat.com/ja/docs/2012/fyi-preferences-to-prevent-non-ssl-contents-on-ssl-pages-from-loading-have-been-added/) で、SSL (`https`) ページ上で非 SSL (`http`) サイトのコンテンツ読み込みをブロックする設定が追加されました。ユーザーのセキュリティを高めるため、これらの設定のうち `security.mixed_content.block_active_content` が初期設定で有効化されました。つまり、安全なページ上で、安全でないスクリプト、スタイルシート、プラグインコンテンツ、[`<iframe>`](https://developer.mozilla.org/docs/Web/HTML/Element/iframe)、[`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)、ウェブフォント ([`@font-face`](https://developer.mozilla.org/docs/Web/CSS/@font-face))、[WebSockets](https://developer.mozilla.org/docs/WebSockets) がブロックされ、代わりに通知が表示されるようになります。画像、動画、音声といった「表示系コンテンツ」はブロックされません。詳しくは [Tanvi Vyas のブログ記事](https://blog.mozilla.org/tanvi/2013/04/10/mixed-content-blocking-enabled-in-firefox-23/) を参照してください。

Mozilla では、[主要サイト](https://bugzilla.mozilla.org/showdependencytree.cgi?id=844556) および [独自運営サイト](https://bugzilla.mozilla.org/showdependencytree.cgi?id=843977) で見つかった非 SSL コンテンツ混在問題をトラッキングしています。
